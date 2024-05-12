# Smart Key 
## This project based on yolo v7.

## All Key 
```
F308
F318
F314
F312A
F310B
F312B
F311A
F309
F310A
F313
F311B
```

## Execute
```shell=
python detect4key5.py --weights key.pt --source runs/source/sample1.jpg 
```

## After detect 
You can get key number with regex

```php=
   public function index()
   {
	  #執行批次檔,位於./public/run.bat
	  exec("run.bat", $output, $retval);
	  
	  #組合成字串
	  $output_string = implode(" ",$output);
	  
	  #利用正規表示法提取所要的關鍵字
	  preg_match('/##(F\d{3}[A|B]?)##/', $output_string, $output_array);
	   
	  #抓group即為答案
	  echo $output_array[1] ;
    
   }
```
/public/run.bat
```bash=
python D:\project\wuStudio\lhu\vending\yolo_v7\yolov7\detect4key.py --weights D:\project\wuStudio\lhu\vending\yolo_v7\yolov7\key.pt --source D:/project/wuStudio/lhu/vending/yolo_v7/yolov7/runs/source/512730.jpg
```

## Ref. 
[Php Regex](https://www.phpliveregex.com/)