PlayVimeo
=========

Using VimeoHeler to generate direct vimeo url.

EX:
----
<pre>
<code>
- (void)viewDidLoad
{
    [super viewDidLoad];
    vimeoHelper = [[VimeoHelper alloc] init];
    [vimeoHelper getVimeoRedirectUrlWithUrl:@"http://vimeo.com/52760742" delegate:(id<VimeoDelegate>)self];
}

- (void)finishedGetVimeoURL:(NSString *)url
{
    _moviePlayerController = [[MPMoviePlayerViewController alloc] initWithContentURL:[NSURL URLWithString:url]];
    [self presentViewController:_moviePlayerController animated:NO completion:nil];
}
</code>
</pre>
