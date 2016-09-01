### SwiftError###
-----------------
>Error:`because the related view doesn't have a superview`:
	
	没有把"addSubview"写在"addConstraints"前面，没有添加到父视图哪来的约束。  

>Error:`Optional(Error Domain=NSURLErrorDomain Code=-1017 "cannot parse response" UserInfo=0x7f9ff30d3910 {NSUnderlyingError=0x7f9ff0c50e80 "The operation couldn’t be completed. (kCFErrorDomainCFNetwork error -1017.)"...`

	拼接[URL]:http://hostname/?arg0=1&arg1=10 使用let encoding = Alamofire.ParameterEncoding.JSON;
	参数形式：var parameters = ["arg0":1, "arg1":10] 使用let encoding = Alamofire.ParameterEncoding.URL;
	
>Error:``
	