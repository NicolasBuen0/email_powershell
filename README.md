# email_powershell

$SMTPInfo = New-Object Net.Mail.SmtpClient('smtp.gmail.com', 587); 
$SMTPInfo.EnableSsl = $true;
$SMTPInfo.Credentials = New-Object System.Net.NetworkCredential('your_email@gmail.com', 'password');
$ReportEmail = New-Object System.Net.Mail.MailMessage; 
$ReportEmail.From = 'gmail@gmail.com';
$ReportEmail.Subject = 'Só um teste boy';
$ReportEmail.Body = 'só um teste : ';
$ReportEmail.Attachments.Add('C:\teste.jpg'); 
$SMTPInfo.Send($ReportEmail)
