# networktool
网络工具

```
#pragma mark - 网络请求的方法 - ✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨✨

/**
 Get 请求

 @param urlString 请求的地址
 @param isCache 是否需要缓存
 @param parameters 请求的参数
 @param successBlock 请求成功的回调
 @param failureBlock 请求失败的回调
 @return URLSessionTask
 */
+ (URLSessionTask *)GetRequestWithUrlString:(NSString *)urlString
                                        isCache:(BOOL)isCache
                                     parameters:(NSDictionary *)parameters
                                   successBlock:(ResponseSuccess)successBlock
                                   failureBlock:(ResponseFailure)failureBlock;


/**
 Post 请求

 @param urlString 请求的地址
 @param isCache 是否需要缓存
 @param parameters 请求的参数
 @param successBlock 请求成功的回调
 @param failureBlock 请求失败的回调
 @return URLSessionTask
 */
+ (URLSessionTask *)PostRequestWithUrlString:(NSString *)urlString
                                      isCache:(BOOL)isCache
                                   parameters:(NSDictionary *)parameters
                                 successBlock:(ResponseSuccess)successBlock
                                 failureBlock:(ResponseFailure)failureBlock;


/**
 上传多张图片

 @param urlString 请求的地址
 @param parameters 请求的参数
 @param imageArray 上传的图片数组
 @param fileNameArray 上传的图片数组对应的名字
 @param successBlock 上传成功的回调
 @param failureBlock 上传失败的回调
 @param progress 上传进度
 @return URLSessionTask
 */
+ (URLSessionTask *)UploadMultipleImageWithUrlString:(NSString *)urlString
                                            parameters:(NSDictionary *)parameters
                                            imageArray:(NSArray *)imageArray
                                         fileNameArray:(NSArray *)fileNameArray
                                          successBlock:(ResponseSuccess)successBlock
                                          failureBlock:(ResponseFailure)failureBlock
                                        upLoadProgress:(UploadProgress)progress;


/**
 文件下载

 @param urlString 请求的地址
 @param parameters 请求的参数
 @param savePath 下载文件保存路径
 @param successBlock 下载文件成功的回调
 @param failureBlock 下载文件失败的回调
 @param progress 下载文件的进度显示
 @return URLSessionTask
 */
+ (URLSessionTask *)DownloadFileWithUrlString:(NSString *)urlString
                                     parameters:(NSDictionary *)parameters
                                       savaPath:(NSString *)savePath
                                   successBlock:(ResponseSuccess)successBlock
                                   failureBlock:(ResponseFailure)failureBlock
                               downLoadProgress:(DownloadProgress)progress;



/*
 *   网络状态监测
 */
+ (void)startNetWorkMonitoringWithBlock:(NetworkStatusBlock)networkStatus;


/*
 *   自定义请求头
 */
+ (void)setValue:(NSString *)value forHTTPHeaderKey:(NSString *)HTTPHeaderKey;


/*
 *   取消指定Url的网路的请求
 */
+ (void)cancelRequestWithUrl:(NSString *)url;


/*
 *   取消所有的网路的请求
 */
+ (void)cancelAllRequest;

```
