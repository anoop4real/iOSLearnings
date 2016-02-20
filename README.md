# iOSLearnings
Things which I learned from practice and from others about iOS/tvOS

###Display HTML in tvOS - Swift

	    @IBOutlet weak var myText:UITextView!

    override func viewDidLoad() {
        super.viewDidLoad()

        let staticHTMLContent:String = "<ol><li><span style='font-family:courier;font-size:18px; color:#E88834;'>Test 1.</span></li><li><span style='color:red;'>TEST2</span></li><li><b>TEST3</b></li><li><i>This text is italic</i>"
        let attributedString:NSAttributedString
        do {

            attributedString = try NSAttributedString(data: staticHTMLContent.dataUsingEncoding(NSUTF8StringEncoding)!, options: [NSDocumentTypeDocumentAttribute : NSHTMLTextDocumentType], documentAttributes: nil)
            myText.attributedText = attributedString
        } catch _ {
            
        }
        
        // Do any additional setup after loading the view.
    }
