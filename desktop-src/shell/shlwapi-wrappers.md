---
description: Le tabelle in questo documento elencano le funzioni wrapper di Shlwapi.dll che forniscono funzionalità Unicode limitate a Windows 95, Windows 98 e Windows Millennium Edition (Windows Me).
title: Funzioni wrapper SHLWAPI
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d928228873b893228c7fddc22fc1ca29ca511cd
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549753"
---
# <a name="shlwapi-wrapper-functions"></a>Funzioni wrapper SHLWAPI

\[Queste funzioni sono disponibili tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003. Potrebbero essere modificate o non disponibili nelle versioni successive di Windows.\]

Le tabelle in questo documento elencano le funzioni wrapper di Shlwapi.dll che forniscono funzionalità Unicode limitate a Windows 95, Windows 98 e Windows Millennium Edition (Windows Me).

Windows 95, Windows 98 e Windows Millennium Edition (Windows Me) sono indicati qui come "piattaforme ANSI native". Nelle piattaforme ANSI native, queste funzioni wrapper convertono i parametri della stringa di input Unicode in ANSI e chiamano le versioni ANSI delle funzioni nella colonna Inoltra **a.** Ad esempio, **AppendMenuWrapW** chiama **AppendMenuA**, ovvero la versione ANSI di [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Le altre funzioni seguono lo stesso modello. Tutte le stringhe restituite dalla funzione ANSI vengono convertite in Unicode e restituite all'applicazione chiamante. A parte le eccezioni  riportate nella colonna Osservazioni, la funzione wrapper ha la stessa sintassi e fornisce la stessa funzionalità della funzione nella colonna Inoltra **a.** Per informazioni dettagliate sull'utilizzo, fare riferimento a tale pagina di riferimento.

**Avviso di sicurezza:** Più stringhe Unicode possono essere convertite nella stessa stringa ANSI. Conflitti imprevisti dopo la conversione potrebbero causare un comportamento imprevisto. Ad esempio, se **CreateEventWrapW** viene usato per creare due eventi con nome diverso i cui nomi corrispondono dopo la conversione da Unicode ad ANSI, la seconda chiamata restituirà un handle allo stesso evento della prima chiamata, anche se le stringhe Unicode originali erano diverse.

Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 e sistemi operativi successivi sono indicati qui come "piattaforme Unicode native". Nella maggior parte dei casi, nelle piattaforme Unicode native, queste funzioni wrapper inoltrano semplicemente i parametri della stringa di input alla versione Unicode della funzione nella colonna Inoltra **a.** Ad esempio, **AppendMenuWrapW** inoltra a **AppendMenuW**, che è la versione Unicode di [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Le altre funzioni seguono lo stesso modello. Tutte le stringhe restituite dalla funzione Unicode vengono restituite all'applicazione chiamante. A parte le eccezioni  riportate nella colonna Osservazioni, la funzione wrapper ha la stessa sintassi e fornisce la stessa funzionalità della funzione nella colonna Inoltra **a.** Per informazioni dettagliate sull'utilizzo, fare riferimento a tale pagina di riferimento.

**Avviso di sicurezza:** I problemi di sicurezza noti per le funzioni **nella** colonna Inoltra a si applicano anche alle funzioni wrapper corrispondenti. Per informazioni dettagliate, vedere la documentazione di riferimento per la funzione nella colonna Inoltra **a.**

Le funzioni wrapper in questa tabella sono tutte contenute in Shlwapi.dll. Per chiamarli, è necessario usare il numero ordinale elencato nella tabella.

> [!Note]  
> Queste funzioni wrapper sono disponibili in Windows XP, ma non forniscono alcuna funzionalità wrapper in Windows XP Service Pack 2 (SP2) e versioni successive. Inoltre, non forniscono funzionalità wrapper in Windows Server 2003. È consigliabile usare invece le funzioni elencate nella colonna Inoltra **a.**

 



| Funzione                  | Ordinale | Inoltra a                                             | DLL      | Commenti                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(Menu)](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32 | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32 | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32 | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32 | [(CompareString)](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DragQueryFile)](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**Drawtext**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**Exttextout**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [(GetClassInfo)](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [(g)](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32 | [(g)](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(MenuItemInfo)](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**Getobject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [(g)](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**Getopenfilename**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [(j)](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(Menu)](#menu), [(MenuItemInfo)](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32 | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32 | [(e)](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32 | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage e PostMessage)](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage e PostMessage)](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**Registerclass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(RegisterClass)](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**Regopenkeyex**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**Regqueryvalueex**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(ValueEx)](#regqueryvalueexw), [(RegQueryValueExW)](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**Regsetvalueex**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(ValueEx)](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [(SendMessage)](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**Setwindowlong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [(g)](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [(i)](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [(a)](#shlwapi-wrapper-functions)                                                                                                   |



 

Le funzioni wrapper nella tabella seguente non eseguono alcuna conversione del set di caratteri. Offrono invece un supporto limitato per le funzionalità del sistema operativo non disponibili nelle piattaforme precedenti.



| Funzione                     | Ordinale | Inoltra a                                                                     | DLL      | Commenti                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32 | [(h)](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32 | [(h)](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**DeleteTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue)                                   | KERNEL32 | [(h)](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32 | [(CompareExchange)](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**Queueuserworkitem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32 | [(SetTimerQueueTimer)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Commenti

### <a name="a"></a>(a)

Se è necessaria la conversione di stringhe, tutte le stringhe vengono convertite tramite la tabella codici \_ CP ACP.

Queste funzioni utilizzano caratteri più adatti e non eseguono il controllo predefinito durante la conversione da Unicode ad ANSI. Inoltre, se la stringa non può essere convertita da Unicode ad ANSI, la funzione wrapper passa una stringa **NULL** alla funzione ANSI sottostante. Ciò può verificarsi, ad esempio, quando la memoria è insufficiente. Il passaggio **di una** stringa NULL può causare l'esito negativo di alcune funzioni con un errore di parametro non valido, ma altre funzioni accettano la stringa **NULL** e la trattano come parametro previsto. Ad esempio, si verifica un errore quando la funzione **CreateWindowExWrapW** tenta di convertire il parametro *lpWindowName* in ANSI e [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una finestra con una didascalia vuota. Il wrapper non invia una notifica quando si sono verificati questi problemi.

Microsoft Layer for Unicode (MSLU) verifica la presenza di errori durante la conversione da Unicode ad ANSI e restituisce i valori di errore appropriati. Ad esempio, la funzione wrapper [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) in MSLU restituisce 0 se l'elemento non è stato aggiunto correttamente.

### <a name="b"></a>(b)

Queste funzioni usano un collegamento a caricamento ritardato alla funzione appropriata. Ciò significa che la DLL che contiene la funzione nella colonna "Inoltra a" non viene caricata dal Shlwapi.dll fino a quando non viene chiamata una funzione in tale DLL. Il Microsoft Visual C++ linker supporta questa funzionalità in modo più generale tramite l'opzione /DELAYLOAD.

### <a name="c"></a>(c)

Questa funzione modifica i nomi dei file. Come illustrato in [(a)](#shlwapi-wrapper-functions), le funzioni convertono tutte le stringhe tramite la tabella codici \_ CP ACP. Non verificano se le funzioni di I/O dei file sono state impostate sulla modalità ANSI. Se le funzioni di I/O dei file sono in modalità OEM, le stringhe verranno convertite in e dal set di caratteri errato. Un'applicazione può impostare le funzioni di I/O del file in modalità OEM in modo esplicito chiamando la [**funzione SetFileApisToOEM.**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem)

**Avviso di sicurezza: ** L'uso di queste funzioni wrapper per i nomi di file può compromettere la sicurezza dell'applicazione. Poiché non viene eseguito alcun controllo predefinito e vengono utilizzati caratteri più adatti, i caratteri del nome file possono essere convertiti in modi imprevisti. Ciò potrebbe causare file system attacchi di spoofing. Inoltre, durante la conversione da Unicode ad ANSI può verificarsi una perdita di dati invisibile all'utente.

Mslu non presenta queste limitazioni.

### <a name="d"></a>(d)

Se la stringa disegnata richiede un set di caratteri non disponibile nel tipo di [](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) carattere selezionato nel contesto di dispositivo, queste funzioni wrapper usano la funzionalità di collegamento dei caratteri della libreria [MLang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) per eseguire il rendering di ogni carattere in un tipo di carattere appropriato. A differenza della maggior parte delle altre funzioni wrapper, queste sono funzionali in Microsoft Windows NT 4.0 oltre alle piattaforme ANSI native.

### <a name="e"></a>(e)

Le implementazioni Unicode complete di queste funzioni sono disponibili nelle piattaforme ANSI native. Queste funzioni non chiamano la funzione ANSI correlata.

### <a name="f"></a>(f)

Se la lingua dell'interfaccia utente predefinita dell'utente usa un set di caratteri diverso da quello predefinito del sistema, il sistema tenta di riscrivere i modelli di finestra di dialogo e i controlli di sottoclasse e convertire le voci di menu in owner draw, in modo che le stringhe nella lingua dell'interfaccia utente predefinita dell'utente continuino a essere visualizzate correttamente. Gli unici controlli supportati dalle regole di riscrittura del modello di finestra di dialogo sono i controlli statici, pulsante, casella di riepilogo e casella combinata. Questi controlli sono sottoclassati in modo che la **funzione SendMessageWrapW** possa ottenere la stringa Unicode originale senza essere tradotta tramite il set di caratteri ANSI. A differenza della maggior parte delle altre funzioni wrapper, queste sono funzionali in Microsoft Windows NT 4.0 e nelle piattaforme ANSI native. Vedere le osservazioni nella documentazione della funzione [**MLLoadLibrary**](./callbacks.md) per altre informazioni su come vengono determinate la lingua dell'interfaccia utente predefinita dall'utente e la lingua dell'interfaccia utente predefinita del sistema.

### <a name="g"></a>(g)

Se è necessaria la conversione di stringhe, tutte le stringhe vengono convertite tramite la tabella codici \_ CP ACP.

Quando si esegue la conversione da ANSI a Unicode per l'output, se la stringa restituita non rientra nel buffer fornito, le funzioni wrapper troncano la stringa. Le funzioni che restituiscono il numero di caratteri copiati nel buffer o il numero di caratteri necessari per evitare il troncamento non restituiscono il numero di caratteri Unicode copiati nel buffer fornito o richiesti dal chiamante della funzione wrapper. Restituiscono il numero di caratteri ANSI copiati nel buffer o richiesti dalla funzione ANSI sottostante. Mslu non presenta queste limitazioni.

### <a name="h"></a>(h)

Nei sistemi precedenti a Windows XP, queste funzioni implementano un pool di thread semplificato e una coda timer. In Windows XP e versioni successive, queste funzioni usano il pool di thread di sistema e la coda del timer di sistema. Per le funzioni della coda timer, il *parametro hQueue* deve essere impostato su **NULL** per indicare che l'operazione deve essere eseguita nella coda timer predefinita.

### <a name="i"></a>(i)

Nelle piattaforme Unicode, queste funzioni traslano il messaggio da Unicode ad ANSI se la finestra di destinazione è ANSI. Queste funzioni non eseguono la conversione dei messaggi in piattaforme ANSI native. Pertanto, le applicazioni chiamanti che chiamano questa funzione devono garantire che il messaggio sia in formato Unicode su piattaforme Unicode e in formato ANSI su piattaforme ANSI. Nella chiamata di funzione seguente, ad esempio, *wParam* deve essere un punto di codice Unicode se il programma è in esecuzione in una piattaforma Unicode e deve essere un carattere ANSI se il programma è in esecuzione in una piattaforma ANSI.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

MSLU tiene traccia del set di caratteri della routine della finestra di destinazione e converte il messaggio in base alle esigenze.

### <a name="j"></a>(j)

Nelle piattaforme ANSI queste funzioni restituiscono la lunghezza della stringa ANSI sottostante, non la lunghezza della stringa Unicode convertita. Mslu non presenta queste limitazioni.

### <a name="compareexchange"></a>(CompareExchange)

La sintassi **di SHInterlockedCompareExchange** è leggermente diversa da quella di [**InterlockedCompareExchangePointer,**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer)ma funziona in modo identico.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>(CompareString)

Tenere presente che nelle piattaforme ANSI native entrambe le stringhe vengono convertite in ANSI e confrontate come stringhe ANSI. Se le stringhe Unicode contengono caratteri che non possono essere rappresentati in ANSI, i risultati potrebbero essere imprevisti. Ad esempio, se la tabella codici ANSI predefinita non supporta i caratteri CJK, le stringhe L" \\ x66F0" e L" x6708" verrebbero confrontate come uguali nelle piattaforme ANSI native perché entrambe vengono mappate alla stringa \\ ANSI "?".

### <a name="datetime"></a>(DateTime)

Nella Shlwapi.dll versione 5.0, fornita con Windows 2000, la tabella codici dell'identificatore delle impostazioni locali passato come primo parametro di **GetDateFormatWrapW** e **GetTimeFormatWrapW** deve corrispondere alla tabella codici ANSI corrente. In caso contrario, la stringa restituita potrebbe essere convertita in modo non corretto. Questa limitazione non si applica alle Shlwapi.dll 5.5 o successive. Ciò significa che i sistemi Windows XP e versioni successive non sono soggetti a questa limitazione. Mslu non presenta questa limitazione.

### <a name="dialogboxparam"></a>(DialogBoxParam)

Il *parametro lpTemplateName* per la **funzione DialogBoxParamWrapW** non può essere una stringa. Deve essere un ordinale creato dalla macro [**MAKEINTRESOURCE.**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) La procedura di dialogo specificata dal *parametro lpDialogFunc* riceve messaggi ANSI su piattaforme ANSI native e messaggi Unicode su piattaforme Unicode native. La procedura di dialogo deve essere preparata per gestire entrambi i casi. Mslu non presenta queste limitazioni.

### <a name="exttextout"></a>(ExtTextOut)

Le piattaforme ANSI native implementano la [**funzione ExtTextOutW**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e le piattaforme Unicode native. Lo scopo di **ExtTextOutWrapW** è eseguire il collegamento del tipo di carattere, come descritto in un'osservazione separata.

### <a name="dragqueryfile"></a>(DragQueryFile)

La **funzione DragQueryFileWrapW** non consente di eseguire query sulla lunghezza di un file nell'handle di rilascio passando **NULL** come *parametro lpszFile.* Mslu non presenta queste limitazioni.

### <a name="formatmessage"></a>(FormatMessage)

Nelle piattaforme ANSI native, i formati nella stringa non vengono convertiti da Unicode ad ANSI. Ad esempio, l'esempio di codice seguente è in errore.


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



Questo esempio di codice usa "!s!" . Nelle piattaforme ANSI native, questa stringa viene passata alla versione ANSI della [**funzione FormatMessage.**](/windows/win32/api/winbase/nf-winbase-formatmessage) Di conseguenza, è prevista una stringa ANSI anziché una stringa Unicode. Analogamente, il formato "%2" implica un argomento stringa. Quando viene passato alla funzione ANSI **FormatMessage,** viene interpretato come stringa ANSI anziché come stringa Unicode. La stringa di formato corretta è L"%1!ws! %2!ws!". In questo modo le stringhe vengono stampate correttamente sulle piattaforme ANSI e Unicode.

La funzione non supporta "%0" stringa di formato speciale.

Mslu non presenta queste limitazioni.

### <a name="getclassinfo"></a>(GetClassInfo)

Nelle piattaforme ANSI native, i membri **lpszMenuName** e **lpszClassName** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) non vengono convertiti in Unicode e sono sempre impostati su **NULL.** Inoltre, la routine window restituita nel membro **lpfnWndProc** della struttura **WNDCLASS** non viene convertita in Unicode e fa riferimento a una routine finestra ANSI. Mslu non presenta queste limitazioni.

### <a name="menu"></a>(Menu)

Nella Shlwapi.dll versione 5.0, fornita con Windows 2000, le stringhe delle voci di menu contenenti caratteri di tabulazione (t) potrebbero non \\ essere visualizzate correttamente. Questa limitazione non si applica alle Shlwapi.dll 5.5 o successive. Ciò significa che i sistemi Windows XP e versioni successive non sono soggetti a questa limitazione. Mslu non presenta questa limitazione.

### <a name="menuiteminfo"></a>(MenuItemInfo)

Questa funzione supporta solo la versione microsoft Windows NT 4.0 della [**struttura MENUITEMINFOW.**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) Questa struttura non dispone di **un membro hbmpItem.** Inoltre, la funzione non supporta il flag MIIM \_ BITMAP. Mslu non presenta queste limitazioni.

### <a name="openfilename"></a>(OpenFileName)

Il **membro cbSize** della [**struttura OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve essere impostato su sizeof(OPENFILENAME \_ NT4W).

Il **membro lpstrCustomFilter** della [**struttura OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve essere impostato su **NULL.**

I valori dei **membri nMaxFile** e **nMaxFileTitle** della struttura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) non devono superare MAX \_ PATH.

Se il membro **lpfnHook** della struttura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) non è **NULL,** deve fare riferimento a una routine hook ANSI nelle piattaforme ANSI native e a una routine hook Unicode nelle piattaforme Unicode native.

MsLU non presenta queste limitazioni.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage e PostMessage)

Nelle piattaforme ANSI native non viene eseguita alcuna conversione sul messaggio trasmesso o recuperato. Il messaggio trasmesso/recuperato è ANSI su piattaforme ANSI native e Unicode su piattaforme Unicode native. L'applicazione chiamante deve essere preparata per gestire entrambi i casi. Ad esempio, se il messaggio recuperato è WM \_ CHAR, *wParam* è un codice carattere ANSI nelle piattaforme ANSI native, ma è un punto di codice Unicode nelle piattaforme Unicode native. MsLU non presenta queste limitazioni.

### <a name="queueuserworkitem"></a>(QueueUserWorkItem)

La **funzione SHQueueUserWorkItem** è leggermente diversa dalla funzione [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) corrispondente. La sintassi **per SHQueueUserWorkItem** è illustrata qui.

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

I parametri devono essere impostati come segue:

-   I *parametri pfnCallback* *e pContext* hanno gli stessi significati dei parametri *Function* e *Context,* rispettivamente, di [**QueueUserWorkItem.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)
-   Il *parametro dwTag* non è usato e deve essere impostato su 0.
-   Il *parametro pdwld* non è usato e deve essere impostato su **NULL.**
-   Il *parametro pszModule* punta a una stringa ANSI con terminazione Null facoltativa che specifica il nome di una libreria da caricare prima che l'elemento di lavoro inizi e venga scaricato dopo il completamento dell'elemento di lavoro. Questo parametro può essere **NULL**.
-   Il *parametro dwFlags* supporta solo un subset dei valori supportati da [**QueueUserWorkItem.**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) Vengono riconosciuti i flag seguenti.

    

    | Nome              | Valore      | Significato                          |
    |-------------------|------------|----------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Uguale a WT \_ EXECUTEINIOTHREAD.   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Uguale a WT \_ EXECUTELONGFUNCTION. |

    

     

    > [!Note]  
    > Il flag LONGEXECTIME di TPS non ha lo stesso valore numerico del \_ flag WT \_ EXECUTELONGFUNCTION. Quando si **usa SHQueueUserWorkItem,** il parametro dwFlags deve essere una combinazione di valori TPS, \_ \* non di valori WT. \_ \*

     

**SHQueueUserWorkItem** restituisce un valore diverso da zero se l'elemento di lavoro è stato accodato correttamente e 0 in caso contrario. Se la funzione ha esito negativo, è possibile [**usare GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere informazioni aggiuntive.

### <a name="registerclass"></a>(RegisterClass)

Nelle piattaforme ANSI native non viene eseguita alcuna conversione sul membro **lpfnWndProc** della [**struttura WNDCLASSW.**](/windows/win32/api/winuser/ns-winuser-wndclassa) La finestra riceverà i messaggi della finestra ANSI sulle piattaforme ANSI native e i messaggi della finestra Unicode sulle piattaforme Unicode native. La routine della finestra deve essere preparata per gestire entrambi i casi. MsLU non presenta queste limitazioni.

### <a name="regqueryvalueexw"></a>(RegQueryValueExW)

**Anche RegQueryValueExWrapW** è stato chiamato con il nome **RegQueryValueExW.** Come per qualsiasi funzione senza nome esportata esclusivamente in base al numero ordinale, è possibile scegliere il nome con cui la funzione è nota nel codice.

### <a name="sendmessage"></a>(SendMessage)

Nelle piattaforme Unicode native, **la funzione SendMessageWrapW** inoltra alla [**funzione SendMessageW.**](/windows/win32/api/winuser/nf-winuser-sendmessage) Nelle piattaforme ANSI native **SendMessageWrapW offre** un supporto limitato per la conversione di messaggi Unicode in ANSI. L'elenco dei messaggi supportati è riportato nella tabella seguente. La funzione non convertirà altri messaggi.

MsLU non presenta queste limitazioni.



|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| CB \_ ADDSTRING        | (b) (f) (c)                                                                                               |
| CB \_ FINDSTRING       | (b) (f) (c)                                                                                               |
| CB \_ FINDSTRINGEXACT  | (a) (f) (c)                                                                                               |
| CB \_ GETLBTEXT        | (b) (f) (c) (o) Il buffer passato nel parametro *lParam* deve avere spazio per almeno 256 caratteri.   |
| CB \_ GETLBTEXTLEN     | (a)                                                                                                       |
| CB \_ INSERTSTRING     | (b) (f) (c)                                                                                               |
| CB \_ SELECTSTRING     | (b) (f) (c)                                                                                               |
| EM \_ CHARFROMPOS      |                                                                                                           |
| EM \_ GETLINE          | (e) Il valore restituito è il numero di caratteri ANSI copiati.                                             |
| EM \_ GETSEL           |                                                                                                           |
| EM \_ REPLACESEL       | (b) (f)                                                                                                   |
| EM \_ SETPASSWORDCHAR  | (a)                                                                                                       |
| EM \_ SETSEL           |                                                                                                           |
| EM \_ SETWORDBREAKPROC | Questo messaggio non ha alcun effetto. La routine word break non è impostata.                                          |
| LB \_ ADDSTRING        | (b) (f) (d)                                                                                               |
| LB \_ FINDSTRING       | (b) (f) (d)                                                                                               |
| LB \_ FINDSTRINGEXACT  | (b) (f) (lbs)                                                                                             |
| LB \_ GETTEXT          | (b) (f) (lbs) (o) Il buffer passato nel parametro *lParam* deve avere spazio per almeno 256 caratteri. |
| LB \_ GETTEXTLEN       | (a)                                                                                                       |
| LB \_ INSERTSTRING     | (b) (f) (d)                                                                                               |
| LB \_ SELECTSTRING     | (b) (f) (d)                                                                                               |
| WM \_ GETTEXT          | (b) (f)                                                                                                   |
| WM \_ GETTEXTLENGTH    | (a)                                                                                                       |
| WM \_ SETTEXT          | (b) (f)                                                                                                   |
| WM \_ SETTINGCHANGE    | (a) Il messaggio viene inviato con un timeout di tre secondi.                                                  |



 


-   (a) La stringa ANSI misurata o recuperata deve soddisfare la condizione seguente: la lunghezza della versione Unicode corrispondente della stringa non può superare la lunghezza della versione ANSI della stringa. Se questa condizione non viene soddisfatta, la lunghezza restituita sarà breve. Se la memoria non è sufficiente per determinare la lunghezza della stringa Unicode, la funzione restituisce zero, non LB ERR o \_ CB ERR come \_ previsto.
-   (b) Se è necessaria la conversione di stringhe, tutte le stringhe vengono convertite tramite la tabella \_ codici CP ACP.

    Questa funzione usa i caratteri più adatti e non esegue il controllo predefinito durante la conversione da Unicode ad ANSI. Inoltre, se la stringa non può essere convertita da Unicode ad ANSI, la funzione passa una stringa Null alla funzione ANSI sottostante. Ciò può verificarsi, ad esempio, quando la memoria è insufficiente. Il passaggio di una stringa Null può causare l'esito negativo di alcune funzioni con un errore di parametro non valido, ma altre funzioni accettano la stringa Null e la trattano come parametro previsto. Ad esempio, se si verifica un errore quando il wrapper WM SETTEXT tenta di convertire il titolo della finestra in ANSI, la finestra \_ avrà una didascalia vuota. La funzione non invia una notifica quando si verificano questi problemi. Mslu non presenta queste limitazioni.

-   (c) L'handle di finestra specificato deve essere l'handle per un [controllo ComboBox](../controls/combo-boxes.md) o [ComboBoxEx.](../controls/comboboxex-controls.md) Se l'handle si trova in un controllo casella combinata che è di tipo owner-draw e non è stato creato con lo stile [List Box Styles,](../controls/list-box-styles.md) la traduzione di questo messaggio avrà esito negativo e potrebbe persino verificarsi un arresto anomalo.
-   (d) L'handle di finestra specificato deve essere l'handle di un controllo casella di riepilogo. Se la casella di riepilogo è di tipo owner-draw e non è stata creata con lo stile [Stili](../controls/list-box-styles.md) casella di riepilogo, la traduzione di questo messaggio avrà esito negativo e potrebbe persino verificarsi un arresto anomalo.
-   (e) Se è necessaria la conversione di stringhe, tutte le stringhe vengono convertite tramite la tabella codici \_ CP ACP.

    Quando si esegue la conversione da ANSI a Unicode per l'output, le funzioni wrapper troncano la stringa restituita se non rientra nel buffer fornito. Il valore restituito per le funzioni che restituiscono il numero di caratteri copiati nel buffer o il numero di caratteri necessari per evitare il troncamento si riferisce al numero di caratteri ANSI copiati nel buffer o richiesti dalla funzione ANSI sottostante, non al numero di caratteri Unicode copiati nel buffer fornito o richiesti dall'applicazione chiamante che ha chiamato la funzione wrapper. Mslu non presenta questa limitazione. Per altre informazioni, vedere [Microsoft Layer for Unicode on Windows 95/98/Me Systems (Livello Microsoft per Unicode in sistemi Windows 95/98/Me).](/previous-versions/ms812865(v=msdn.10))

### <a name="settimerqueuetimer"></a>(SetTimerQueueTimer)

La **funzione SHSetTimerQueueTimer** è leggermente diversa dalla funzione [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) corrispondente. La sintassi è la seguente:

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

I parametri devono essere impostati come segue:

-   Il *parametro hQueue* deve essere impostato su **NULL,** specificando la coda timer predefinita.
-   I parametri *pfnCallback*, *pContext*, *dwDueTime* e *dwPeriod* hanno gli stessi significati dei parametri *Callback*, *Parameter*, *DueTime* e *Period,* rispettivamente, [**di CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).
-   Il *parametro lpszLibrary* non è usato e deve essere impostato su **NULL.**
-   Il *parametro Flags* supporta solo un subset dei valori supportati da [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).

    

    | Nome              | Valore      | Significato                         |
    |-------------------|------------|---------------------------------|
    | TPS \_ EXECUTEIO    | 0x00000001 | Uguale a WT \_ EXECUTEINIOTHREAD   |
    | TPS \_ LONGEXECTIME | 0x00000008 | Uguale a WT \_ EXECUTELONGFUNCTION |

    

     

    > [!Note]  
    > Il flag LONGEXECTIME di TPS non ha lo stesso valore \_ numerico del flag WT \_ EXECUTELONGFUNCTION. Quando si **usa SHSetTimerQueueTimer,** il *parametro dwFlags* deve essere una combinazione di valori TPS, \_ \* non di valori WT. \_ \*

     

**SHSetTimerQueueTimer restituisce** l'handle del timer creato in caso di esito positivo e NULL in caso **contrario.**

### <a name="shellexecuteex"></a>(ShellExecuteEx)

Il **membro lpFile** della [**struttura SHELLEXECUTEINFO**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) passato nell'unico parametro di questa funzione non può superare i caratteri INTERNET \_ MAX URL \_ \_ LENGTH. Se il flag SEE MASK CLASSNAME viene \_ \_ omesso, il membro **lpClass** deve essere inizializzato su **NULL.**

### <a name="valueex"></a>(ValueEx)

Sono supportati solo i tipi di dati del Registro di sistema seguenti: REG \_ SZ, REG \_ EXPAND \_ SZ, REG \_ BINARY e REG \_ DWORD. A differenza di queste funzioni wrapper, MSLU supporta anche REG \_ MULTI \_ EXPAND \_ SZ.

### <a name="windowlong"></a>(WindowLong)

Nelle piattaforme ANSI native, la funzione non esegue alcuna conversione in una delle finestre lunghe. Ad esempio, se si passa GWLP WNDPROC, la funzione restituisce la routine della finestra \_ ANSI, non un thunk. Mslu non presenta queste limitazioni.

 

 
