# xcode-new-characteristics
xcode的新变化，包括xcode8, swift3等

#Xcode8新变化<br>
1.菜单栏window下没有了projects选项，无法删除derive data<br>
可手动命令行删除：rm -rf ~/Library/Developer/Xcode/DerivedData<br>
2.调试选项下，多了一个runtime<br>
<br>
#swift3变化
在Xcode8.0上 Edit->Convert->To Current Swift Syntax，可自动把代码更新成swift2.3或3.0格式<br>
swift2.3之前格式的代码无法在Xcode8.0上编译<br>
1.类或属性修饰词<br>
swift2 public, private<br>
swift3 open, fileprivate<br>
<br>
2.CGRect变化<br>
swift2 CGRect(0, 0, 0, 0)<br>
CGRectMake(0, 0, 0, 0)<br>
swift3 CGRect(x: 0, y: 0, width: 0, height 0)<br>
CGRect(x: 0, y: 0, width: 0, height 0)<br>
类似的还有CGPoint<br>
3.颜色<br>
swift2 UIColor.grayColor()<br>
swift3 UIColor.gray<br>
<br>
4.枚举变化<br>
swift2 <br>
UITableViewStyle.Plain<br>
UIActivityIndicatorViewStyle.Gray<br>
swift3(首字母变为了小写) <br>
UITableViewStyle.plain<br>
UIActivityIndicatorViewStyle.gray<br>
<br>
5.隐藏<br>
swift2 tableview?.hidden = true<br>
swift3 tableview?.isHidden = true<br>
<br>
6.方法调用的改变<br>
swift2<br>
dataSource.isKindOfClass(NSArray.self)<br>
modeArray.addObjectsFromArray(dataSource as [AnyObject])<br>
swift3<br>
dataSource.isKind(of: NSArray.self)<br>
modelArray.addObjects(from: dataSource as [AnyObject])<br>
<br>
7.代理方法的改变<br>
以UITableView为例<br>
swift2<br>
public func tableView(tableView: UITableView, willDisplayCell cell: UITableViewCell, forRowAtIndexPath indexPath: NSIndexPath)<br>
swift3<br>
open func tableView(_ tableView: UITableView, willDisplayCell cell: UITableViewCell, forRowAtIndexPath indexPath: IndexPath)<br>
类似的还有NSError使用Error类型代替，等<br>
8.协议的改变<br>
optional方法的变化<br>
swift2<br>
optional func requestFirstPage() -> Void<br>
swift3<br>
@objc optional func requestFirstPage() -> Void<br>
<br>
9.action的改变<br>
swift2<br>
backBtn.addTarget(self, action: "backBtnControlEventAction", forControlEvents: .TouchUpInside)<br>
swift3<br>
backBtn.addTarget(self, action: #selector(CTBaseViewController.backBtnControlEventAction), for: .touchUpInside)<br>
<br>
10.coregraphics的变化<br>
swift2<br>
let context: CGContextRef? = UIGraphicsGetCurrentContext()<br>
CGContextSetFillColorWithColor(context, color.CGColor)<br>
CGContextFillRect(context, rect)<br>
swift3<br>
let context: CGContext? = UIGraphicsGetCurrentContext()<br>
context?.setFillColor(color.cgColor)<br>
context?.fill(rect)<br>
<br>
xcode8使用中可能遇到的错误<br>
1.convert to current swift syntax failed could not find test host<br>
http://stackoverflow.com/questions/37847807/xcode-8-beta-convert-to-current-swift-syntax-failed-could-not-find-test-host<br>
2.<br>