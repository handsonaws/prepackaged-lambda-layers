
![Hands-on AWS](https://github.com/handsonaws/common-assets/blob/3245081c723dc7f20982872762fe5cf4daee1b61/images/logotype.png?raw=true "Hands-on AWS")

# Pre-packaged AWS Lambda Layers

Ready-to-use AWS Lambda Layer packages.

## Organization

Python runtime folders

- Python 3.8

Currently available packages

- Pandas 1.4.2
- Requests 2.27.1
- OpenAI 0.27.0

- Python 3.11

Currently available packages

- matplotlib 3.7.1
- numpy 1.25.2
- openai 0.27.4
- pandas 2.0.3

## Steps to Create an AWS Lambda Layer

1. Select the puthon runtime version and library you would like to use, and download the corresponding package (see previous section for the folder structure and listing)

2. Login to AWS Console and navigate to AWS Lambda > Layers

3. Click on 'Create New'

4. Give it an appropriate name and an optional description

5. Select 'upload file' and choose the `python.zip` package that you just downloaded

    💡 *Tip:* Sometimes the upload from local might timeout and fail for heavier packages. Try uploading firts to an S3 bucket location and then choosing 'upload from s3' in Lambda Layers console to overcome this problem.

6. Select the correct runtime version(s). Exmaple: python.3.8

7. Click 'Create'

## Steps to use the new AWS Lambda Layer in your Lambda function

1. Login to AWS Console and navigate to AWS Lambda > Functions

2. Click on 'Create New'

3. Click om Layers > Add New

4. Choose Custom Layer

5. Select the newly created Lambda Layer from the list, and version (1)

6. Click 'Add'

7. Now you can `import <package>` in your lambda function code. Test it out - you should be able to run this without any errors about missing modules.
