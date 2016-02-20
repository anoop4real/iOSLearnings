# iOSLearnings
Things which I learned from practice and from others about iOS/tvOS
* [Apple Guidelines](https://developer.apple.com/app-store/review/guidelines/)
* [Apple Design](https://developer.apple.com/design/)
* [Apple OnDemand ResourceGuide](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/index.html#//apple_ref/doc/uid/TP40015083-CH2-SW1)
* [APP THINNING](https://developer.apple.com/library/prerelease/watchos/documentation/IDEs/Conceptual/AppDistributionGuide/AppThinning/AppThinning.html)
* [Voodo Pad](https://plausible.coop/voodoopad/)
* [Markdown Tutorial](http://markdowntutorial.com/)
* [Icons](https://icons8.com/web-app/new-icons/all)
* [Mock Design Tool](https://ninjamock.com/)
* [SQLite Browser](http://sqlitebrowser.org/)
* [XCode Edit Breakpoints](https://www.bignerdranch.com/blog/xcode-breakpoint-wizardry/)


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
