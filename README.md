# DICA-Yi RAG问答测试材料

## 内容

- `test_result_200_submission.json`：原始JSON的逐字节副本，包含问题、参考答案、系统输出及汇总指标。
- `images/`：60道图像题实际引用的44张不同PNG图片。同一图片可对应多道题。
- `image_manifest.json`：每张图片的相对路径、引用问题编号、文件大小和SHA-256校验值。
- `validation_report.json`：题量、模态、类别、图片匹配和完整性核验结果。
- `UPLOAD_GUIDE.md`：上传和邀请导师查看的步骤。

## 数量与字段

四类任务为药方、出处、上下文、词义，每类50题，其中35道文本题、15道图像题；总计140道文本题和60道图像题。

`id`为题号，`category`为任务类别，`type`为text或image，`question`为用户问题，`reference`为参考答案，`answer`为系统输出。图像题的`image`字段保留原文件名；例如`21.png`应解析为本包中的`images/21.png`。

图片依据JSON文件名从既有图像库提取，校验保证副本一致。



