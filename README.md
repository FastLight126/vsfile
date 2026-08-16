# 微思文件管理器
微思文件管理器，只有一个PHP脚本的在线文件管理器

# 使用方法
1. 按照简易说明修改初始参数，上传vsfile.php到服务器上即可
2. 程序开头CUSTOM_CONFIG_FILE，若配置了该选项，则文件管理器会使用独立的配置文件，与主程序完全脱离，未配置此项，主程序自身末尾就是配置文件
3. SessionName和主密码是否提前配置好并不重要，如果未配置，管理器会在第一次运行时自动配置好
4. 最简单的用法，配置好用户名、密码（明文），不配置salt（默认也没有salt），运行一次，进入登录界面，用户名密码（加密），SessionName，主密码就自动配置好了

# 配置文件说明
========== 配置文件说明 ==========

1. 配置文件是标准JSON格式，修改时请注意不要破坏标准JSON的结构和语法。
2. users是用户列表，其中密码是带盐加密形式。
3. 程序内置简易设置初始密码的方法，只需要将对应用户的password字段修改为想改的密码，并将salt字段清空即可，程序在加载时会自动替换为带盐加密形式。
4. 设置totp字段即为启用该账户的2FA验证，字段值为TOTP密钥，清空该字段为不启用2FA。
5. totp_time_fix字段为TOTP时间偏移量，一般设为1，时间误差比较大的可以设置大些，1表示±30秒，2表示±60秒，以此类推。

========== 配置檔案說明 ==========

1. 配置檔案是標準JSON格式，修改時請注意不要破壞標準JSON的結構和語法。
2. users是用戶列表，其中密碼是帶鹽加密形式。
3. 程式內建簡易設定初始密碼的方法，只需要將對應用戶的password欄位修改為想改的密碼，並將salt欄位清空即可，程式在載入時會自動替換為帶鹽加密形式。
4. 設定totp欄位即為啟用該帳戶的2FA驗證，欄位值為TOTP密鑰，清空該欄位為不啟用2FA。
5. totp_time_fix字段為TOTP時間偏移量，一般設為1。時間誤差較大的可以設置大些，1表示±30秒，2表示±60秒，以此類推。

========== Configuration File Instructions ==========

1. The configuration file is in standard JSON format. Please be careful not to break the structure and syntax of the standard JSON when modifying it.
2. The "users" field is the user list, where passwords are in a salted and encrypted format.
3. The program has a built-in simple way to set an initial password. Simply change the "password" field for the corresponding user to the desired password and clear the "salt" field. The program will automatically replace it with the salted encryption format upon loading.
4. Setting the "totp" field enables 2FA verification for that account. The field value is the TOTP secret key. Clearing this field disables 2FA.
5. The "totp_time_fix" field is the TOTP time offset. It is generally set to 1, and can be set higher for larger time deviations. 1 represents ±30 seconds, 2 represents ±60 seconds, and so on.

========== تعليمات ملف التكوين ==========

1. ملف التكوين بصيغة JSON القياسية. يرجى الحرص على عدم إتلاف بنية وقواعد JSON القياسية عند التعديل.
2. "users" هي قائمة المستخدمين، حيث تكون كلمات المرور بصيغة مشفرة مع الملح.
3. يحتوي البرنامج على طريقة مبسطة مضمنة لتعيين كلمة مرور أولية. ما عليك سوى تغيير حقل "password" للمستخدم المقابل إلى كلمة المرور المطلوبة وإفراغ حقل "salt". عند التحميل، سيستبدل البرنامج تلقائيًا بالنمط المشفر مع الملح.
4. تعيين حقل "totp" يفعّل التحقق بخطوتين لهذا الحساب. قيمة الحقل هي المفتاح السري TOTP. وإفراغ هذا الحقل يعطل 2FA.
5. حقل "totp_time_fix" هو الإزاحة الزمنية الخاصة بـ TOTP. يُحدد عادةً على 1، ويمكن ضبطه على قيمة أعلى إذا كان خطأ الوقت أكبر. 1 يمثل ±30 ثانية، و2 يمثل ±60 ثانية، وهكذا.

========== Konfigurationsdatei-Anleitung ==========

1. Die Konfigurationsdatei ist im Standard-JSON-Format. Bitte beachten Sie beim Ändern, die Struktur und Syntax des Standard-JSON nicht zu beschädigen.
2. "users" ist die Benutzerliste, wobei die Passwörter in einer mit Salt verschlüsselten Form gespeichert sind.
3. Das Programm enthält eine einfache eingebaute Methode zum Setzen eines Initialpassworts. Ändern Sie einfach das Feld "password" des entsprechenden Benutzers auf das gewünschte Passwort und leeren Sie das Feld "salt". Beim Laden wird das Programm automatisch durch die mit Salt verschlüsselte Form ersetzen.
4. Wenn Sie das Feld "totp" setzen, wird die 2FA-Verifikation für dieses Konto aktiviert. Der Feldwert ist der TOTP-Geheimschlüssel. Wenn Sie dieses Feld leeren, ist 2FA deaktiviert.
5. Das Feld "totp_time_fix" ist der TOTP-Zeitversatz. Es wird normalerweise auf 1 gesetzt und kann bei größeren Zeitabweichungen höher eingestellt werden. 1 steht für ±30 Sekunden, 2 für ±60 Sekunden usw.

========== Instructions du fichier de configuration ==========

1. Le fichier de configuration est au format JSON standard. Veuillez veiller à ne pas casser la structure et la syntaxe du JSON standard lors de la modification.
2. "users" est la liste des utilisateurs, où les mots de passe sont au format chiffré avec sel.
3. Le programme intègre une méthode simple pour définir un mot de passe initial. Il suffit de modifier le champ "password" de l'utilisateur correspondant au mot de passe souhaité et de vider le champ "salt". Au chargement, le programme remplacera automatiquement le champ par le format chiffré avec sel.
4. Définir le champ "totp" active la vérification 2FA pour ce compte. La valeur du champ est la clé secrète TOTP. Vider ce champ désactive la 2FA.
5. Le champ "totp_time_fix" est le décalage temporel TOTP. Il est généralement défini à 1, et peut être réglé à une valeur plus élevée en cas d'écart de temps plus important. 1 représente ±30 secondes, 2 représente ±60 secondes, et ainsi de suite.

========== कॉन्फ़िगरेशन फ़ाइल निर्देश ==========

1. कॉन्फ़िगरेशन फ़ाइल मानक JSON प्रारूप में है। संशोधित करते समय कृपया मानक JSON की संरचना और वाक्य-विन्यास को न तोड़े।
2. "users" उपयोगकर्ताओं की सूची है, जहाँ पासवर्ड नमक-सहित एन्क्रिप्टेड प्रारूप में होते हैं।
3. प्रोग्राम में प्रारंभिक पासवर्ड सेट करने की एक सरल अंतर्निहित विधि है। संबंधित उपयोगकर्ता के "password" फ़ील्ड को इच्छित पासवर्ड में बदलें और "salt" फ़ील्ड को खाली छोड़ दें। लोड होने पर प्रोग्राम स्वचालित रूप से नमक-सहित एन्क्रिप्टेड प्रारूप में बदल देगा।
4. "totp" फ़ील्ड सेट करने से उस खाते के लिए 2FA सत्यापन सक्षम हो जाता है। फ़ील्ड का मान TOTP गुप्त कुंजी है। इस फ़ील्ड को खाली करने से 2FA अक्षम हो जाता है।
5. "totp_time_fix" फ़ील्ड TOTP समय ऑफ़सेट है। आम तौर पर इसे 1 पर सेट किया जाता है, और यदि समय की त्रुटि अधिक हो तो इसे अधिक मान पर भी सेट किया जा सकता है। 1 का अर्थ ±30 सेकंड, 2 का अर्थ ±60 सेकंड, और आगे भी यही क्रम जारी रहता है।

========== Istruzioni per il file di configurazione ==========

1. Il file di configurazione è in formato JSON standard. Quando lo modifichi, fai attenzione a non compromettere la struttura e la sintassi del JSON standard.
2. "users" è l'elenco degli utenti, dove le password sono in formato crittografato con salt.
3. Il programma include un metodo semplice integrato per impostare una password iniziale. Basta modificare il campo "password" dell'utente corrispondente con la password desiderata e svuotare il campo "salt". All'avvio, il programma sostituirà automaticamente il valore con il formato crittografato con salt.
4. Impostare il campo "totp" abilita la verifica 2FA per quell'account. Il valore del campo è la chiave segreta TOTP. Svuotare questo campo disattiva la 2FA.
5. Il campo "totp_time_fix" è l'offset temporale TOTP. Di solito viene impostato a 1 e può essere regolato a un valore maggiore se l'errore di tempo è più grande. 1 rappresenta ±30 secondi, 2 rappresenta ±60 secondi e così via.

========== 設定ファイルの説明 ==========

1. 設定ファイルは標準JSON形式です。修正時は標準JSONの構造と構文を破壊しないように注意してください。
2. 「users」はユーザーリストで、パスワードはソルト付き暗号化形式です。
3. プログラムには簡易的な初期パスワード設定方法が組み込まれています。該当ユーザーの「password」フィールドを変更したいパスワードにし、「salt」フィールドを空にすると、プログラム読み込み時に自動的にソルト付き暗号化形式に置き換えます。
4. 「totp」フィールドを設定すると、そのアカウントの2FA認証が有効になります。フィールド値はTOTP秘密鍵です。このフィールドを空にすると2FAは無効になります。
5. 「totp_time_fix」フィールドはTOTPの時間オフセットであり、通常は1に設定されます。時間誤差が大きい場合はより大きな値を設定できます。1は±30秒、2は±60秒を表し、以降同様に続きます。

========== 구성 파일 안내 ==========

1. 구성 파일은 표준 JSON 형식입니다. 수정할 때는 표준 JSON의 구조와 문법을 손상시키지 않도록 주의하세요.
2. "users"는 사용자 목록이며, 비밀번호는 salt가 포함된 암호화 형식입니다.
3. 프로그램에는 초기 비밀번호를 설정하는 간단한 내장 방법이 있습니다. 해당 사용자의 "password" 필드를 원하는 비밀번호로 변경하고 "salt" 필드를 비우면, 로딩 시 프로그램이 자동으로 salt가 포함된 암호화 형식으로 교체합니다.
4. "totp" 필드를 설정하면 해당 계정의 2FA 인증이 활성화됩니다. 필드 값은 TOTP 비밀 키입니다. 이 필드를 비우면 2FA가 비활성화됩니다.
5. "totp_time_fix" 필드는 TOTP 시간 오프셋입니다. 일반적으로 1로 설정하며, 시간 오차가 더 큰 경우 더 큰 값으로 설정할 수 있습니다. 1은 ±30초, 2는 ±60초를 뜻하며, 이후도 같은 방식입니다.

========== Instruções do arquivo de configuração ==========

1. O arquivo de configuração está em formato JSON padrão. Ao modificá-lo, tenha cuidado para não quebrar a estrutura e a sintaxe do JSON padrão.
2. "users" é a lista de usuários, onde as senhas estão em formato criptografado com salt.
3. O programa inclui um método simples integrado para definir uma senha inicial. Basta alterar o campo "password" do usuário correspondente para a senha desejada e limpar o campo "salt". Ao carregar, o programa substituirá automaticamente o valor pelo formato criptografado com salt.
4. Definir o campo "totp" habilita a verificação 2FA para essa conta. O valor do campo é a chave secreta TOTP. Limpar este campo desativa a 2FA.
5. O campo "totp_time_fix" é o deslocamento de tempo TOTP. Geralmente é definido como 1 e pode ser ajustado para um valor maior se o erro de tempo for maior. 1 representa ±30 segundos, 2 representa ±60 segundos e assim por diante.

========== Инструкции по файлу конфигурации ==========

1. Файл конфигурации находится в стандартном формате JSON. При изменении не нарушайте структуру и синтаксис стандартного JSON.
2. "users" — это список пользователей, где пароли находятся в зашифрованном виде с солью.
3. В программе есть простой встроенный способ задать начальный пароль. Просто измените поле "password" соответствующего пользователя на нужный пароль и очистите поле "salt". При загрузке программа автоматически заменит его на формат с солью.
4. Установка поля "totp" включает 2FA-проверку для этого аккаунта. Значение поля — секретный ключ TOTP. Очистка этого поля отключает 2FA.
5. Поле "totp_time_fix" — это временной сдвиг TOTP. Обычно оно устанавливается в 1, а при больших ошибках времени может быть увеличено. 1 означает ±30 секунд, 2 — ±60 секунд и так далее.

========== Instrucciones del archivo de configuración ==========

1. El archivo de configuración está en formato JSON estándar. Al modificarlo, tenga cuidado de no romper la estructura ni la sintaxis del JSON estándar.
2. "users" es la lista de usuarios, donde las contraseñas están en formato cifrado con sal.
3. El programa incluye un método simple para establecer una contraseña inicial. Simplemente cambie el campo "password" del usuario correspondiente a la contraseña deseada y vacíe el campo "salt". Al cargar, el programa reemplazará automáticamente el valor por el formato cifrado con sal.
4. Establecer el campo "totp" habilita la verificación 2FA para esa cuenta. El valor del campo es la clave secreta TOTP. Vaciar este campo deshabilita la 2FA.
5. El campo "totp_time_fix" es el desplazamiento de tiempo TOTP. Normalmente se establece en 1 y puede ajustarse a un valor mayor si el error de tiempo es más grande. 1 representa ±30 segundos, 2 representa ±60 segundos, y así sucesivamente.

========== Yapılandırma dosyası talimatları ==========

1. Yapılandırma dosyası standart JSON formatındadır. Değiştirirken standart JSON yapısını ve sözdizimini bozmamaya dikkat edin.
2. "users", kullanıcıların listesidir; parolalar tuzla şifrelenmiş biçimdedir.
3. Programda başlangıç parolasını ayarlamak için basit yerleşik bir yöntem vardır. İlgili kullanıcının "password" alanını istediğiniz parolaya değiştirin ve "salt" alanını boşaltın. Yükleme sırasında program otomatik olarak tuzla şifrelenmiş formata dönüştürecektir.
4. "totp" alanını ayarlamak, bu hesap için 2FA doğrulamasını etkinleştirir. Alanın değeri TOTP gizli anahtarıdır. Bu alanı boşaltmak 2FA'yı devre dışı bırakır.
5. "totp_time_fix" alanı TOTP zaman kaydırma değeridir. Genellikle 1 olarak ayarlanır ve zaman hatası daha büyükse daha yüksek bir değere ayarlanabilir. 1 ±30 saniye, 2 ±60 saniye anlamına gelir ve buna benzer şekilde devam eder.

# 免责声明
该软件是免费开源软件，本人/本公司不对使用该软件产生的任何问题承担任何责任。
除简体中文语言包外，其他语言包均为AI翻译，提示词已写明不可以含有任何翻译不准确、不完整、语法错误、错别字、歧义、语义不清晰的文案，不可以含有任何政治敏感、色情、暴力、恐怖、反动、违法，歧视等不良信息，但我看不懂，我不对翻译结果负责。如果有翻译的不恰当的地方，请告知我，我会及时修正。

# 注意事项
上传限制目前仅按照扩展名限制，支持黑名单、白名单，白名单优先级高于黑名单，暂未做mime类型检测，安全性请自行评估。
本地测试环境未PHP7.3.4，我开发的时候尽量会兼容低版本PHP，如果有发现不支持的PHP版本，请及时告知，我视情况向下兼容或干脆去掉某些版本的支持。

# 引用的开源组件
[vscode-icon](https://github.com/vscode-icons/vscode-icons)
[CodeMirror](https://codemirror.net/5)
[FiraCode](https://github.com/tonsky/FiraCode/blob/master/LICENSE)
[Zepto](https://zeptojs.com/)

# 纯真IP库
我正在使用免费的纯真社区版IP库。纯真(CZ88.NET)自2005年起一直为广大社区用户提供社区版IP地址库，只要获得纯真的授权就能免费使用，并不断获取后续更新的版本。
纯真除了免费的社区版IP库外，还提供数据更加准确、服务更加周全的商业版IP地址查询数据。纯真围绕IP地址，基于 网络空间拓扑测绘 + 移动位置大数据 方案，对IP地址定位、IP网络风险、IP使用场景、IP网络类型、秒拨侦测、VPN侦测、代理侦测、爬虫侦测、真人度等均有近20年丰富的数据沉淀。