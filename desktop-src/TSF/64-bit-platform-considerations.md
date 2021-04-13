---
title: Considerazioni su 64 bit
description: Con la crescente disponibilità di Windows a 64 bit, gli utenti prevedono metodi di input, ad esempio tastiere internazionali in diversi linguaggi o IME (Input Method Editor) nelle lingue asiatiche orientali, per funzionare correttamente con applicazioni a 32 bit e 64 bit.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- Framework servizi di testo (TSF), Windows a 64 bit
- TSF (Text Services Framework), Windows a 64 bit
- Servizi di testo, Windows a 64 bit
- Windows a 64 bit
- Framework servizi di testo (TSF), input Method Editor (IME)
- TSF (Text Services Framework), input Method Editor (IME)
- Servizi di testo, input Method Editor (IME)
- Input Method Editor (IME)
- IME (Input Method Editor)
- Framework servizi di testo (TSF), tastiere internazionali
- TSF (Text Services Framework), tastiere internazionali
- Servizi di testo, tastiere internazionali
- tastiere internazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399190"
---
# <a name="64-bit-considerations"></a>Considerazioni su 64 bit

Con la crescente disponibilità di Windows a 64 bit, gli utenti prevedono metodi di input, ad esempio tastiere internazionali in diversi linguaggi o IME (Input Method Editor) nelle lingue asiatiche orientali, per funzionare correttamente con applicazioni a 32 bit e 64 bit. Quando si sviluppano componenti del metodo di input o servizi di testo per Microsoft Windows, è importante considerare Windows a 64 bit come piattaforma di destinazione potenziale per il prodotto.

Poiché gli IME e i servizi di testo (basati sul Framework dei servizi di testo) vengono in genere implementati come librerie a collegamento dinamico (dll), è importante notare che le dll sono compilate in modo specifico per l'utilizzo in ambienti a 32 bit o in ambienti a 64 bit. una DLL compilata per l'utilizzo in ambienti a 32 bit non può essere utilizzata da applicazioni a 64 bit e viceversa.

> [!Note]  
> WOW64 non attenua questa restrizione della DLL specifica del bit. Per informazioni su WOW64, vedere [esecuzione di applicazioni a 32 bit](/windows/desktop/WinProg64/running-32-bit-applications).

 

In questo argomento vengono illustrate importanti considerazioni di progettazione per lo sviluppo di IME e servizi di testo per l'utilizzo in Windows a 64 bit.

## <a name="64-bit-considerations-for-imes"></a>Considerazioni a 64 bit per IME

In questa sezione vengono descritte le considerazioni speciali relative alla compilazione degli IME per l'utilizzo con Windows a 64 bit. Per informazioni sugli IME, vedere [Input Method Editor](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Compilazione di versioni a 32 bit e a 64 bit di un IME

A causa del problema di compatibilità a 32 bit/64 bit precedentemente indicato con le dll, è necessario prendere alcune precauzioni per assicurarsi che gli IME funzionino in modo trasparente con qualsiasi applicazione (32 bit o 64 bit) in esecuzione in Windows a 64 bit. La soluzione consigliata per consentire all'IME di funzionare in modo trasparente con le applicazioni a 32 bit e a 64 bit in una piattaforma a 64 bit consiste nel compilare e installare versioni parallele a 32 bit e a 64 bit della DLL IME. In genere, gli sviluppatori compilano dll parallele da un'unica origine regolando le impostazioni della piattaforma di destinazione nell'ambiente di compilazione. Per ulteriori informazioni sulle applicazioni a 32 bit e a 64 bit per singolo approvvigionamento, vedere [preparazione per Windows a 64 bit](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Installazione side-by-side di editor di metodi di input a 64 bit e a 32 bit

Gli sviluppatori di IME e i servizi di testo devono essere a conoscenza delle considerazioni a 64 bit descritte in questo argomento. Fortunatamente, gli utenti finali di questi servizi non devono preoccuparsi di questi dettagli specifici dell'implementazione. Una funzionalità di Windows a 64 bit è la possibilità di nascondere la necessità di versioni specifiche di 64 bit e 32 per le dll IME dagli utenti finali. Quando entrambe le versioni dell'IME sono correttamente installate in modalità side-by-Side, Windows a 64 bit riconosce la presenza di versioni a 64 bit e 32 bit dell'IME e presenta tali IME specifici all'utente finale come singolo IME *logico* . Quando un utente finale deve usare un IME, Windows a 64 bit sceglie in modo trasparente la versione di IME (32 bit o 64 bit) appropriata per le circostanze specificate.

Per il corretto funzionamento delle installazioni affiancate di IME a 64 bit e a 32 bit, ovvero per rappresentare le due dll specifiche della piattaforma come singolo IME logico per l'utente, è necessario che siano soddisfatte le condizioni seguenti:

-   Gli sviluppatori devono compilare versioni specifiche della piattaforma, una per Windows a 32 bit e una per Windows a 64 bit, della DLL IME.
-   Le dll a 32 bit e a 64 bit devono condividere lo stesso nome file.
-   È necessario seguire i requisiti della directory di installazione. Per ulteriori informazioni, vedere requisiti della directory di installazione.

Le installazioni affiancate di dll IME a 32 bit e a 64 bit condividono la stessa chiave del registro di sistema per l'archiviazione dei dati di configurazione, incluso il nome del file DLL:


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



La funzione [**ImmInstallIME**](/windows/desktop/api/imm/nf-imm-imminstallimea) viene usata per creare questa chiave del registro di sistema. È necessario che il programma di installazione e installazione di un IME chiami questa funzione per registrare l'IME come un layout di tastiera supportato. La funzione **ImmInstallIME** deve essere chiamata una sola volta, sia dalla versione a 32 bit che dalla versione 64 bit della dll IME.

## <a name="mismatched-ime-dlls"></a>Dll IME non corrispondenti

L'installazione solo della versione a 32 bit di un IME in Windows a 64 bit non è né consigliata né supportata. Se un'applicazione a 64 bit tenta di caricare un IME a 32 bit, l'IME si interrompe automaticamente quando l'applicazione tenta di caricare il layout di tastiera associato.

> [!IMPORTANT]
>
> Non viene visualizzato alcun messaggio o finestra di dialogo di avviso quando si verifica un errore di conflitto IME a 32 bit o a un'applicazione a 64 bit.

 

Considerazioni a 64 bit per i servizi di testo

In questa sezione vengono descritte le considerazioni speciali relative alla compilazione di servizi di testo per l'utilizzo in ambienti a 64 bit. Per ulteriori informazioni sui servizi di testo e sul Framework dei servizi di testo, vedere [Text Services Framework](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Compilazione di servizi di testo a 32 bit e a 64 bit

Un servizio di testo viene implementato come oggetto Component Object Model (COM) esposto in una DLL. Di conseguenza, i conflitti DLL a 32 bit/64 bit possono verificarsi con i servizi di testo installati in Windows a 64 bit. Come per gli IME, la soluzione consigliata per consentire al servizio di testo di funzionare in modo trasparente con le applicazioni a 32 bit e a 64 bit su una piattaforma a 64 bit consiste nel compilare e installare versioni parallele a 32 bit e a 64 bit della DLL del servizio di testo.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Installazione side-by-side di servizi di testo a 64 bit e a 32 bit

Per una versione a 32 bit e una versione a 64 bit di un servizio di testo da installare side-by-side e rappresentata all'utente come singolo servizio di testo logico, è necessario che siano soddisfatte le condizioni seguenti:

-   Entrambe le versioni del servizio di testo specificano lo stesso identificatore di classe (CLSID) quando vengono registrate con il sottosistema COM.
-   Entrambe le versioni del servizio di testo vengono registrate in modo indipendente. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di applicazioni com](/windows/desktop/com/registering-com-applications).

Quando un servizio di testo a 32 bit viene registrato con Windows a 64 bit, l'operazione di registrazione viene reindirizzata in modo trasparente alla seguente chiave del registro di sistema:


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Redirector del registro di sistema](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[Registrazione del servizio di testo](text-service-registration.md) ITfInputProcessorProfiles

La versione a 64 bit e la versione a 32 bit di un servizio di testo potrebbero essere in uso simultaneamente. Nei casi in cui entrambe le versioni di un servizio di testo devono modificare gli oggetti condivisi, il coordinamento per gli oggetti condivisi di Access deve essere progettato nel servizio di testo. Ogni servizio di testo è responsabile della gestione di tutti gli oggetti condivisi utilizzati o necessari.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Installazione di soli servizi di testo a 32 bit in Windows a 64 bit

L'installazione solo della versione a 32 bit di un servizio di testo in una piattaforma Windows a 64 bit non è né consigliata né supportata. A causa del mapping di registrazione eseguito su piattaforme Windows a 64 bit, un'applicazione a 64 bit può enumerare i servizi di un servizio di testo a 32 bit tramite l'interfaccia **ITfInputProcessorProfiles** . Tuttavia, se un'applicazione a 64 bit tenta di caricare un servizio di testo a 32 bit, il caricamento non riesce automaticamente.

> [!IMPORTANT]
>
> Non viene visualizzato alcun messaggio o finestra di avviso quando si verifica un errore di conflitto di un servizio di testo a 32 bit o un'applicazione a 64 bit.

 

Altre considerazioni

## <a name="installation-directory-requirements"></a>Requisiti della directory di installazione

In questa sezione vengono descritti i requisiti per la posizione in cui installare i file binari del servizio IME e di testo. Se questi requisiti non vengono seguiti, il servizio di testo o l'IME potrebbe non funzionare correttamente.

**Dll IME**

Nelle piattaforme Windows a 64 bit installare le dll IME a 32 e 64 bit nelle directory seguenti:

-   Installare le dll IME a 32 bit nella directory di sistema SysWOW64. chiamare [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con **CSIDL \_ SYSTEMX86** per recuperare il percorso della directory. In alternativa, se si utilizza [Windows Installer](/windows/desktop/Msi/about-windows-installer), utilizzare la proprietà [**SystemFolder**](/windows/desktop/Msi/systemfolder) .
-   Installare le dll IME a 64 bit nella directory di sistema system32; chiamare [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)o **SHGetFolderPath** con il [ \_ sistema CSIDL](/windows/desktop/shell/csidl) per recuperare il percorso della directory. In alternativa, per Windows Installer, utilizzare la proprietà [**System64Folder**](/windows/desktop/Msi/system64folder) .

**Dll del servizio di testo e file binari correlati**

Nelle piattaforme Windows a 64 bit installare le dll del servizio di testo a 32 e 64 bit, nonché qualsiasi altro file binario correlato al servizio di testo o all'IME, nelle directory seguenti:

-   Installare le dll del servizio di testo a 32 bit e qualsiasi altro file binario a 32 bit in una sottodirectory della directory programmi (x86); chiamare **SHGetFolderPath** con **CSIDL \_ Program \_ FILESX86** per recuperare il percorso della directory. In alternativa, per Windows Installer, utilizzare la proprietà [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) .
-   Installare le dll del servizio di testo a 64 bit e qualsiasi altro file binario a 64 bit in una sottodirectory della directory programmi; chiamare **SHGetFolderPath** con **\_ \_ i file di programma CSIDL** per recuperare il percorso della directory. In alternativa, per Windows Installer, utilizzare la proprietà [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) .

Se non si usa un pacchetto di Windows Installer per installare il servizio IME o di testo, è fortemente consigliato usare un'applicazione di installazione a 64 bit. Il redirector di WOW64 file system potrebbe causare l'installazione dei file nelle directory errate da parte dei programmi di installazione a 32 bit (ad esempio, il reindirizzamento file system WOW64 potrebbe causare l'installazione di file destinati alla directory System32 nella directory SysWOW64). Se è necessario usare un programma di installazione a 32 bit, disabilitare il reindirizzamento del file WOW64 durante il processo di installazione per assicurarsi che il servizio redirector file non provochi un reindirizzamento non intenzionale durante il processo di installazione. Per informazioni sul redirector file system WOW64, vedere [redirector del file System](/windows/desktop/WinProg64/file-system-redirector). Per informazioni su come disabilitare o abilitare il reindirizzamento file system WOW64, vedere [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).

> [!TIP]
>
> Evitare i percorsi di installazione hardcoded. Per altre informazioni, vedere [individuare le directory usando l'interfaccia di programmazione dell'applicazione non Hard-Coded percorsi](/previous-versions//ms675638(v=vs.85))

 

> [!IMPORTANT]
>
> Non installare alcun file di servizio IME o di testo nella directory speciale% WINDIR% \\ IME (per impostazione predefinita, c: \\ Windows \\ IME). Questa directory contiene i file di sistema che supportano i servizi di testo e gli IME. non deve contenere alcun file di servizio di testo o IME di terze parti e il reindirizzamento file system WOW64 non è supportato per questa directory.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Processi Dual Ctfmon.exe eseguiti su piattaforme Windows a 64 bit

Il processo ctfmon.exe gestisce il Framework dei servizi di testo sul desktop e fornisce anche l'interfaccia utente della barra del linguaggio (UI). In Windows a 64 bit, una versione a 32 bit e una versione a 64 bit del ctfmon.exe processo vengono eseguiti simultaneamente. Il processo di ctfmon.exe a 64 bit gestisce i servizi di testo a 64 bit e, allo stesso modo, il processo di ctfmon.exe a 32 bit gestisce i servizi di testo a 32 bit.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Comportamento di visualizzazione per versioni diverse dell'interfaccia utente della barra del linguaggio

In Windows a 64 bit, viene sempre visualizzata solo l'interfaccia utente della barra della lingua associata alla versione a 64 bit di un servizio di testo. Nei casi in cui un'applicazione a 32 bit usi la versione a 32 bit di un servizio di testo, Windows a 64 bit inserisce automaticamente l'interfaccia utente della barra della lingua per il servizio di testo a 64 bit equivalente. In questo modo non è necessario alcun lavoro speciale per i servizi di testo a 32 bit nella versione a 64 bit della barra della lingua.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Considerazioni sul pannello di controllo in Windows a 64 bit

Windows a 64 bit consente di accedere alle versioni a 32 e 64 bit dei servizi di testo e IME tramite il pannello di controllo. Per accedere alle impostazioni del pannello di controllo per versioni specifiche di servizi di testo o IME, esaminare le posizioni seguenti.

-   **Accesso al pannello di controllo per i servizi di testo e gli IME a 32 bit:** Start-> Settings-> pannello di controllo-> visualizzare le icone del pannello di controllo x86
-   **Accesso al pannello di controllo per i servizi di testo e gli IME a 64 bit:** Start-> Settings-> pannello di controllo-> opzioni internazionali e della lingua

In alcune circostanze potrebbe essere possibile che alcune impostazioni siano disponibili solo tramite il pannello di controllo a 32 bit. In questi casi, assicurarsi che gli utenti del servizio di testo o dell'IME siano consapevoli di questo, fornendo la documentazione appropriata o offrendo suggerimenti sull'interfaccia utente nell'interfaccia delle impostazioni a 64 bit.

 

 