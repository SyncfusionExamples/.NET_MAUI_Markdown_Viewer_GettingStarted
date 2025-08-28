# Getting Started with .NET MAUI MarkdownViewer (SfMarkdownViewer)

This guide details the initial setup and basic usage of the [SfMarkdownViewer]() control, offering insight into its ability to render Markdown content with various formatting capabilities across mobile and desktop platforms.

## Initialize the MarkdownViewer Control

1. To initialize the control, import the `Syncfusion.Maui.MarkdownViewer` namespace.
2. Add an [SfMarkdownViewer]() instance to your page.
3. To display Markdown content, assign a string to the `Source` property of the SfMarkdownViewer control. This string can contain standard Markdown syntax such as headings, bold text, lists, and images.

{% tabs %} 
{% highlight xaml %}

    <markdown:SfMarkdownViewer>
        <markdown:SfMarkdownViewer.Source>
            <x:String>
                <![CDATA[
    # What is Markdown Viewer?  
    Markdown View is a UI control in .NET MAUI that allows developers to render Markdown content with full formatting support. It is designed to work efficiently across both mobile and desktop platforms. The viewer supports headings, bold and italic text, lists, tables, images, code blocks, etc.

    # Header 1  
    Used for the main title or top-level heading in a Markdown document. 

    ## Header 2  
    Used to define major sections within your Markdown content.

    ## Table 

    |              | Column 1 | Column 2 | Column 3 |
    |--------------|----------|----------|----------|
    | Row 1        | Content  | Content  | Content  |
    | Row 2        | Content  | Content  | Content  |
    | Row 3        | Content  | Content  | Content  |
                ]]>
            </x:String>
        </markdown:SfMarkdownViewer.Source>
    </markdown:SfMarkdownViewer>

{% endhighlight %}

{% highlight C# %}

    public partial class MainPage : ContentPage
    {
            private const string markdownContent = @"# What is Markdown Viewer?  
    Markdown View is a UI control in .NET MAUI that allows developers to render Markdown content with full formatting support. It is designed to work efficiently across both mobile and desktop platforms. The viewer supports headings, bold and italic text, lists, tables, images, code blocks, etc.

    # Header 1  
    Used for the main title or top-level heading in a Markdown document. 

    ## Header 2  
    Used to define major sections within your Markdown content.

    ## Table 

    |              | Column 1 | Column 2 | Column 3 |
    |--------------|----------|----------|----------|
    | Row 1        | Content  | Content  | Content  |
    | Row 2        | Content  | Content  | Content  |
    | Row 3        | Content  | Content  | Content  |";

        public MainPage()
        {
            InitializeComponent();  
            SfMarkdownViewer markdownViewer = new SfMarkdownViewer();
            markdownViewer.Source = markdownContent;
            Content = markdownViewer;       
        }
    }  

{% endhighlight %}
{% endtabs %}

## Output
[Output]