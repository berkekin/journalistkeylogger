# journalistkeylogger

TR:  Bu kod, bir C# Console uygulaması olarak yazılmış basit bir keylogger örneğidir. Keylogger, bilgisayar kullanıcılarının klavye girişlerini izleyen ve kaydeden bir tür yazılımdır. Bu tür yazılımlar, yasal ve etik açıdan hassas bir konu olduğundan, keylogger kullanımının yasal sınırlarını anlamak ve diğerlerinin gizliliğine saygı göstermek önemlidir.

Şimdi kodun ana bölümlerini daha ayrıntılı bir şekilde inceleyelim:

Namespace ve Kütüphaneler: Kod, System ve System.Runtime.InteropServices gibi çeşitli .NET kütüphanelerini kullanır. Bu kütüphaneler, Windows API'lerine erişmek ve klavye olaylarını izlemek için gerekli olan işlevleri sağlar.

Ana Sınıf ve Başlangıç: Ana sınıf olan Program, keylogger'ın ana mantığını içerir. Main metodu, keylogger'ı başlatır ve bir log dosyası oluşturur. Daha sonra klavye olaylarını dinlemek için bir hook kurar.

Hook Kurma ve Olay İşleme: SetHook metodu, klavye olaylarını dinlemek için gerekli olan hook'u kurar. HookCallback metodu, her klavye olayını yakalar. Bu metod, klavyeden alınan tuş vuruşlarını log dosyasına kaydeder ve özel tuş kombinasyonlarını algılar.

Özel Tuş Kombinasyonları: CheckSpecialKeyCombinations metodu, özel tuş kombinasyonlarını kontrol eder. Örneğin, CTRL+C veya CTRL+V gibi kombinasyonlar algılanır ve log dosyasına kaydedilir.

Diğer Yardımcı Metodlar: Kod, etkin pencerenin başlığını almak için GetActiveWindowTitle metodunu kullanır.

Windows API Kullanımı: Windows API'sine erişmek için çeşitli DllImport nitelikleri kullanılarak dış işlevler çağrılır. Bu işlevler, klavye olaylarını izlemek ve etkin pencerenin başlığını almak gibi görevleri gerçekleştirir.

Bu kodun kullanımı ve uygulanmasıyla ilgili bazı önemli hususlar:

Keylogger kullanımı yasal sınırlar içinde olmalıdır. Başkalarının izni olmadan keylogger kullanmak yasalara aykırı olabilir.
Keylogger'ın kullanımı, kişisel veri gizliliğine saygı göstermeyi gerektirir. Elde edilen bilgilerin yasal ve etik olarak doğru bir şekilde kullanılması önemlidir.
Bu kod, eğitim amaçları için sunulmuştur. Kullanılmadan önce, yerel yasalara ve etik kurallara uygun olarak adapte edilmelidir.


EN: This code is a simple keylogger example written as a C# Console application. A keylogger is a type of software that monitors and records computer users' keyboard input. Because this type of software is a legally and ethically sensitive issue, it is important to understand the legal limits of keylogger use and respect the privacy of others.

Now let's examine the main parts of the code in more detail:

Namespace and Libraries: The code uses various .NET libraries such as System and System.Runtime.InteropServices. These libraries provide the functionality required to access Windows APIs and monitor keyboard events.

Main Class and Startup: The main class, Program, contains the main logic of the keylogger. The main method starts the keylogger and creates a log file. It then sets up a hook to listen for keyboard events.

Hook Establishment and Event Handling: The SetHook method establishes the hook required to listen to keyboard events. The HookCallback method captures every keyboard event. This method records keystrokes received from the keyboard in the log file and detects special key combinations.

Special Key Combinations: The CheckSpecialKeyCombinations method checks for special key combinations. For example, combinations such as CTRL+C or CTRL+V are detected and recorded in the log file.

Other Helper Methods: The code uses the GetActiveWindowTitle method to get the title of the active window.

Windows API Usage: External functions are called using various DllImport attributes to access the Windows API. These functions perform tasks such as monitoring keyboard events and retrieving the title of the active window.

Some important considerations regarding the use and implementation of this code:

Keylogger use must be within legal limits. Using keyloggers without the permission of others may be against the law.
The use of the keylogger requires respect for personal data privacy. It is important that the information obtained is used correctly, legally and ethically.
This code is provided for educational purposes. Before use, it must be adapted in accordance with local laws and ethical rules.
