---
description: Le tabelle di questo documento elencano le funzioni wrapper da Shlwapi.dll che forniscono funzionalità Unicode limitate a Windows 95, Windows 98 e Windows Millennium Edition (Windows Me).
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
ms.openlocfilehash: 52e3a5b60a331a74ced1888d5a196348497c5ff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757718"
---
# <a name="shlwapi-wrapper-functions"></a>Funzioni wrapper SHLWAPI

\[Queste funzioni sono disponibili tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003. Potrebbero essere modificate o non disponibili nelle versioni successive di Windows.\]

Le tabelle di questo documento elencano le funzioni wrapper da Shlwapi.dll che forniscono funzionalità Unicode limitate a Windows 95, Windows 98 e Windows Millennium Edition (Windows Me).

Windows 95, Windows 98 e Windows Millennium Edition (Windows Me) sono indicati come "piattaforme ANSI native". Nelle piattaforme ANSI native queste funzioni wrapper convertono i parametri stringa di input Unicode in ANSI e chiamano versioni ANSI di funzioni nella colonna **inoltri a** . Ad esempio, **AppendMenuWrapW** chiama **AppendMenuA**, che è la versione ANSI di [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Le altre funzioni seguono lo stesso modello. Tutte le stringhe restituite dalla funzione ANSI vengono convertite in Unicode e restituite all'applicazione chiamante. A parte le eccezioni indicate nella colonna **osservazioni** , la funzione wrapper ha la stessa sintassi e fornisce la stessa funzionalità della funzione nella colonna **inoltri a** . Per informazioni dettagliate sull'utilizzo, vedere la pagina di riferimento.

**Avviso di sicurezza:** Più stringhe Unicode possono essere convertite nella stessa stringa ANSI. I conflitti imprevisti dopo la conversione potrebbero causare un comportamento imprevisto. Se, ad esempio, si usa **CreateEventWrapW** per creare due eventi con nome diverso, i cui nomi corrispondono dopo la conversione da Unicode a ANSI, la seconda chiamata restituirà un handle allo stesso evento della prima chiamata, anche se le stringhe Unicode originali erano diverse.

Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 e sistemi operativi successivi vengono indicati come "piattaforme Unicode native". Nella maggior parte dei casi, nelle piattaforme Unicode native queste funzioni wrapper inviano semplicemente i parametri di stringa di input alla versione Unicode della funzione nella colonna **inoltri a** . Ad esempio, **AppendMenuWrapW** si inoltrerà a **AppendMenuW**, che è la versione Unicode di [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua). Le altre funzioni seguono lo stesso modello. Tutte le stringhe restituite dalla funzione Unicode vengono restituite all'applicazione chiamante. A parte le eccezioni indicate nella colonna **osservazioni** , la funzione wrapper ha la stessa sintassi e fornisce la stessa funzionalità della funzione nella colonna **inoltri a** . Per informazioni dettagliate sull'utilizzo, vedere la pagina di riferimento.

**Avviso di sicurezza:** I problemi di sicurezza indicati per le funzioni nella colonna **inoltri a** sono validi anche per le funzioni wrapper corrispondenti. Per informazioni dettagliate, vedere la documentazione di riferimento per la funzione nella colonna **inoltri a** .

Le funzioni wrapper in questa tabella sono tutte contenute in Shlwapi.dll. Per chiamarli, è necessario usare il numero ordinale elencato nella tabella.

> [!Note]  
> Queste funzioni wrapper sono disponibili in Windows XP ma non forniscono funzionalità wrapper in Windows XP Service Pack 2 (SP2) e versioni successive. Inoltre, non forniscono funzionalità wrapper in Windows Server 2003. Usare invece le funzioni elencate nella colonna **inoltri a** .

 



| Funzione                  | Ordinale | Inoltri a                                             | DLL      | Commenti                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| AppendMenuWrapW           | 36      | [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menu)](#menu)                                                           |
| CallWindowProcWrapW       | 37      | [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [i](#shlwapi-wrapper-functions)                                                                                                   |
| CharLowerWrapW            | 38      | [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32 | [e](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperBufWrapW         | 44      | [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32 | [e](#shlwapi-wrapper-functions)                                                                                                   |
| CharUpperWrapW            | 43      | [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32 | [e](#shlwapi-wrapper-functions)                                                                                                   |
| CompareStringWrapW        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32 | [CompareString](#comparestring)                                                                                                   |
| CopyFileWrapW             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateEventWrapW          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| CreateFileWrapW           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| CreateWindowExWrapW       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| DefWindowProcWrapW        | 56      | [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [i](#shlwapi-wrapper-functions)                                                                                                   |
| DeleteFileWrapW           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| DialogBoxParamWrapW       | 59      | [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(DialogBoxParam)](#dialogboxparam)                                       |
| DispatchMessageWrapW      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [i](#shlwapi-wrapper-functions)                                                                                                   |
| DragQueryFileWrapW        | 318     | [**DragQueryFile**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | SHELL32  | [(b](#dialogboxparam)), [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DragQueryFile)](#dragqueryfile)               |
| DrawTextExWrapW           | 301     | [**DrawTextEx**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| DrawTextWrapW             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| ExtTextOutWrapW           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| FormatMessageWrapW        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| GetClassInfoWrapW         | 69      | [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [GetClassInfo](#getclassinfo)                                                                                                     |
| GetDateFormatWrapW        | 311     | [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetDlgItemTextWrapW       | 74      | [**GetDlgItemText**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [g](#compareexchange)                                                                                                             |
| GetFileAttributesWrapW    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| GetLocaleInfoWrapW        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32 | [g](#compareexchange)                                                                                                             |
| GetMenuItemInfoWrapW      | 302     | [**GetMenuItemInfo**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(MenuItemInfo)](#menuiteminfo)                                                     |
| GetModuleFileNameWrapW    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetModuleHandleWrapW      | 83      | [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetObjectWrapW            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [g](#compareexchange)                                                                                                             |
| GetOpenFileNameWrapW      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OPENFILENAME)](#openfilename)                 |
| GetSaveFileNameWrapW      | 389     | [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OPENFILENAME)](#openfilename)                 |
| GetSystemDirectoryWrapW   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetTimeFormatWrapW        | 310     | [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| GetWindowLongWrapW        | 94      | [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| GetWindowsDirectoryWrapW  | 97      | [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| GetWindowTextLengthWrapW  | 96      | [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [j](#j)                                                                                                                           |
| GetWindowTextWrapW        | 95      | [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| InsertMenuItemWrapW       | 98      | [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(menu)](#menu), [(MenuItemInfo)](#menuiteminfo)                          |
| IsCharAlphaWrapW          | 25      | [**IsCharAlpha**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [e](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharAlphaNumericWrapW   | 28      | [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32 | [e](#shlwapi-wrapper-functions)                                                                                                   |
| IsCharUpperWrapW          | 26      | [**IsCharUpper**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [e](#shlwapi-wrapper-functions)                                                                                                   |
| LoadLibraryWrapW          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| LoadStringWrapW           | 107     | [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32 | [e](#shlwapi-wrapper-functions)                                                                                                   |
| MessageBoxWrapW           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| MoveFileWrapW             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| OutputDebugStringWrapW    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| PeekMessageWrapW          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage e PostMessage)](#peekmessage-and-postmessage)                                                                       |
| PostMessageWrapW          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage e PostMessage)](#peekmessage-and-postmessage)                                                                       |
| RegCreateKeyExWrapW       | 120     | [**RegCreateKeyEx**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| RegisterClassWrapW        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(registerClass)](#registerclass)                                                                |
| RegOpenKeyExWrapW         | 125     | [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [un](#shlwapi-wrapper-functions)                                                                                                   |
| RegQueryValueExWrapW      | 128     | [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(ValueEx)](#regqueryvalueexw), [(RegQueryValueExW)](#regqueryvalueexw) |
| RegQueryValueWrapW        | 127     | [**RegQueryValue**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| RegSetValueExWrapW        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(ValueEx)](#regqueryvalueexw)                                                                   |
| SendMessageWrapW          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [SendMessage](#sendmessage)                                                                                                       |
| SetDlgItemTextWrapW       | 138     | [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| SetWindowLongWrapW        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(WindowLong)](#windowlong)                                                                                                         |
| SetWindowTextWrapW        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |
| ShellExecuteExWrapW       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| ShellMessageBoxWrapW      | 388     | [**ShellMessageBox**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| SHGetFileInfoWrapW        | 313     | [**SHGetFileInfo**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | SHELL32  | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| SHGetPathFromIDListWrapW  | 334     | [**SHGetPathFromIDList**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [g](#compareexchange)                                                                                                             |
| TranslateAcceleratorWrapW | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [i](#shlwapi-wrapper-functions)                                                                                                   |
| UnregisterClassWrapW      | 147     | [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [un](#shlwapi-wrapper-functions)                                                                                                   |



 

Le funzioni wrapper nella tabella seguente non eseguono alcuna conversione del set di caratteri. Forniscono invece un supporto limitato per le funzionalità del sistema operativo non disponibili sulle piattaforme precedenti.



| Funzione                     | Ordinale | Inoltri a                                                                     | DLL      | Commenti                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| MLGetUILanguage              | 376     | [**GetUserDefaultUILanguage**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32 | [h](#shlwapi-wrapper-functions)                                              |
| SHCancelTimerQueueTimer      | 265     | [**DeleteTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32 | [h](#shlwapi-wrapper-functions)                                              |
| SHDeleteTimerQueue           | 262     | [**Deletetimerqueue ha provocato**](/windows/win32/api/winbase/nf-winbase-deletetimerqueue)                                   | KERNEL32 | [h](#shlwapi-wrapper-functions)                                              |
| SHInterlockedCompareExchange | 342     | [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32 | [CompareExchange](#compareexchange)                                          |
| SHQueueUserWorkItem          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| SHSetTimerQueueTimer         | 263     | [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32 | [(SetTimerQueueTimer)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Commenti

### <a name="a"></a>un

Se è necessaria la conversione della stringa, tutte le stringhe vengono convertite tramite la \_ tabella codici CP ACP.

Queste funzioni usano i caratteri più adatti e non eseguono il controllo predefinito durante la conversione da Unicode a ANSI. Inoltre, se la stringa non può essere convertita da Unicode a ANSI, la funzione wrapper passa una stringa **null** alla funzione ANSI sottostante. Questa situazione può verificarsi, ad esempio, quando la memoria è insufficiente. Il passaggio di una stringa **null** può causare l'esito negativo di alcune funzioni con un errore di parametro non valido, ma altre funzioni accettano la stringa **null** e la considerano come parametro previsto. Ad esempio, si verifica un errore quando la funzione **CreateWindowExWrapW** tenta di convertire il parametro *lpWindowName* in ANSI e [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una finestra con una didascalia vuota. Il wrapper non invia notifiche quando si verificano questi problemi.

Microsoft Layer for Unicode (MSLU) verifica la presenza di errori durante la conversione da Unicode a ANSI e restituisce i valori di errore appropriati. Ad esempio, la funzione wrapper [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) in MSLU restituisce 0 se l'elemento non è stato accodato correttamente.

### <a name="b"></a>b

Queste funzioni usano un collegamento a caricamento ritardato per la funzione appropriata. Ciò significa che la DLL che contiene la funzione nella colonna "inoltri a" non viene caricata dal Shlwapi.dll finché non viene chiamata una funzione in tale DLL. Il linker Microsoft Visual C++ supporta più in generale questa funzionalità tramite l'opzione/DELAYLOAD.

### <a name="c"></a>c

Questa funzione modifica i nomi file. Come indicato in [(a)](#shlwapi-wrapper-functions), le funzioni convertono tutte le stringhe tramite la \_ tabella codici CP ACP. Non controllano se le funzioni di I/O dei file sono state impostate sulla modalità ANSI. Se le funzioni di I/O dei file sono in modalità OEM, le stringhe verranno convertite in e dal set di caratteri errato. Un'applicazione può impostare in modo esplicito le funzioni di I/O dei file sulla modalità OEM chiamando la funzione [**SetFileApisToOEM**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) .

* * Avviso di sicurezza: * * l'utilizzo di queste funzioni wrapper per i nomi di file può compromettere la sicurezza dell'applicazione. Poiché non viene eseguito alcun controllo predefinito e vengono utilizzati i caratteri più adatti, i caratteri filename possono essere convertiti in modi imprevisti. Questo potrebbe causare file system attacchi di spoofing. Inoltre, è possibile che si verifichi una perdita di dati invisibile durante la conversione da Unicode ad ANSI.

Il MSLU non presenta queste limitazioni.

### <a name="d"></a>d

Se la stringa da disegnare richiede un set di caratteri non disponibile nel tipo di carattere selezionato nel contesto di dispositivo, queste funzioni wrapper utilizzano la funzionalità di [collegamento dei tipi di carattere](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) della libreria [mlang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) per eseguire il rendering di ogni carattere in un tipo di carattere appropriato. A differenza della maggior parte delle altre funzioni wrapper, queste funzionalità sono funzionali in Microsoft Windows NT 4,0 oltre alle piattaforme ANSI native.

### <a name="e"></a>e

Le implementazioni Unicode complete di queste funzioni sono disponibili nelle piattaforme ANSI native. Queste funzioni non chiamano la funzione ANSI correlata.

### <a name="f"></a>f

Se la lingua dell'interfaccia utente predefinita dell'utente utilizza un set di caratteri diverso da quello della lingua dell'interfaccia utente predefinita del sistema, il sistema tenta di riscrivere i modelli di finestra di dialogo e di sottoclasse e di convertire le voci di menu in modo che le stringhe della lingua dell'interfaccia utente predefinite dell'utente continuino a essere visualizzate correttamente. Gli unici controlli supportati dalle regole di riscrittura del modello di finestra di dialogo sono i controlli statici, Button, ListBox e ComboBox. Questi controlli sono sottoclassati in modo che la funzione **SendMessageWrapW** possa ottenere la stringa Unicode originale senza essere convertita tramite il set di caratteri ANSI. A differenza della maggior parte delle altre funzioni wrapper, queste funzionalità sono funzionali in Microsoft Windows NT 4,0 e nelle piattaforme ANSI native. Per ulteriori informazioni sulla modalità di determinazione della lingua dell'interfaccia utente predefinita e della lingua dell'interfaccia utente predefinita del sistema, vedere le note nella documentazione della funzione [**MLLoadLibrary**](./callbacks.md) .

### <a name="g"></a>g

Se è necessaria la conversione della stringa, tutte le stringhe vengono convertite tramite la \_ tabella codici CP ACP.

Quando si esegue la conversione da ANSI a Unicode per l'output, se la stringa restituita non rientra nel buffer fornito, le funzioni wrapper troncano la stringa. Le funzioni che restituiscono il numero di caratteri copiati nel buffer o il numero di caratteri necessari per evitare il troncamento non restituiscono il numero di caratteri Unicode copiato nel buffer fornito da o richiesto dal chiamante della funzione wrapper. Restituiscono il numero di caratteri ANSI copiati nel buffer o richiesti dalla funzione ANSI sottostante. Il MSLU non presenta queste limitazioni.

### <a name="h"></a>h

Nei sistemi precedenti a Windows XP, queste funzioni implementano un pool di thread semplificato e una coda del timer. In Windows XP e versioni successive, queste funzioni usano il pool di thread di sistema e la coda del timer di sistema. Per le funzioni della coda del timer, il parametro *hQueue* deve essere impostato su **null** per indicare che l'operazione deve essere eseguita nella coda del timer predefinita.

### <a name="i"></a>i

Sulle piattaforme Unicode, queste funzioni convertono il messaggio da Unicode a ANSI se la finestra di destinazione è ANSI. Queste funzioni non eseguono la conversione dei messaggi su piattaforme ANSI native. Pertanto, la chiamata di applicazioni che chiamano questa funzione deve garantire che il messaggio sia in formato Unicode su piattaforme Unicode e in formato ANSI sulle piattaforme ANSI. Nella chiamata di funzione seguente, ad esempio, il *wParam* deve essere un punto di codice Unicode se il programma è in esecuzione su una piattaforma Unicode e deve essere un carattere ANSI se il programma è in esecuzione su una piattaforma ANSI.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

MSLU tiene traccia del set di caratteri della routine della finestra di destinazione e converte il messaggio in caso di necessità.

### <a name="j"></a>j

Sulle piattaforme ANSI, queste funzioni restituiscono la lunghezza della stringa ANSI sottostante, non la lunghezza della stringa Unicode tradotta. Il MSLU non presenta queste limitazioni.

### <a name="compareexchange"></a>CompareExchange

La sintassi di **SHInterlockedCompareExchange** è leggermente diversa da quella di [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer), ma funziona in modo identico.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>CompareString

Tenere presente che nelle piattaforme ANSI native entrambe le stringhe vengono convertite in ANSI e confrontate come stringhe ANSI. Se le stringhe Unicode contengono caratteri che non possono essere rappresentati in ANSI, i risultati potrebbero essere imprevisti. Se, ad esempio, la tabella codici ANSI predefinita non supporta i caratteri CJK, le stringhe L " \\ x66F0" e l " \\ x6708" verrebbero confrontate con le piattaforme ANSI native perché entrambe eseguono il mapping alla stringa ANSI "?".

### <a name="datetime"></a>DateTime

In Shlwapi.dll versione 5,0, fornita con Windows 2000, la tabella codici dell'identificatore delle impostazioni locali passato come primo parametro di **GetDateFormatWrapW** e **GetTimeFormatWrapW** deve corrispondere alla tabella codici ANSI corrente. In caso contrario, la stringa restituita potrebbe essere convertita in modo errato. Questa limitazione non si applica a Shlwapi.dll versioni 5,5 o successive. Ciò significa che i sistemi Windows XP e versioni successive non sono soggetti a questa limitazione. Il MSLU non ha questa limitazione.

### <a name="dialogboxparam"></a>(DialogBoxParam)

Il parametro *lpTemplateName* per la funzione **DialogBoxParamWrapW** non può essere una stringa. Deve essere un ordinale creato dalla macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . La routine della finestra di dialogo specificata dal parametro *lpDialogFunc* riceve messaggi ANSI su piattaforme ANSI native e messaggi Unicode su piattaforme Unicode native. La routine della finestra di dialogo deve essere preparata per la gestione di entrambi i casi. Il MSLU non presenta queste limitazioni.

### <a name="exttextout"></a>ExtTextOut

Le piattaforme ANSI native implementano la funzione [**ExtTextOutW**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e le piattaforme Unicode native. Lo scopo di **ExtTextOutWrapW** è quello di eseguire il collegamento dei tipi di carattere, come descritto in un contrassegno separato.

### <a name="dragqueryfile"></a>DragQueryFile

La funzione **DragQueryFileWrapW** non consente di eseguire una query per la lunghezza di un file nell'handle di rilascio passando **null** come parametro *lpszFile* . Il MSLU non presenta queste limitazioni.

### <a name="formatmessage"></a>FormatMessage

Nelle piattaforme ANSI native i formati nella stringa non vengono convertiti da Unicode a ANSI. Ad esempio, l'esempio di codice seguente è in errore.


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



Questo esempio di codice USA "! s!" . Nelle piattaforme ANSI native questa stringa viene passata alla versione ANSI della funzione [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) . Di conseguenza, è prevista una stringa ANSI anziché una stringa Unicode. Analogamente, il formato "%2" implica un argomento di stringa. Quando viene passato alla funzione ANSI **FormatMessage** , viene interpretato come stringa ANSI anziché come stringa Unicode. La stringa di formato corretta è L "%1! WS! %2! WS! ". In questo modo le stringhe vengono stampate correttamente nelle piattaforme ANSI e Unicode.

La funzione non supporta "%0" stringa di formato speciale.

Il MSLU non presenta queste limitazioni.

### <a name="getclassinfo"></a>GetClassInfo

Nelle piattaforme ANSI native i membri **lpszMenuName** e **LpszClassName** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) non vengono convertiti in Unicode e sono sempre impostati su **null**. Inoltre, la routine della finestra restituita nel membro **lpfnWndProc** della struttura **WNDCLASS** non viene convertita in Unicode e fa riferimento a una procedura della finestra ANSI. Il MSLU non presenta queste limitazioni.

### <a name="menu"></a>Menu

In Shlwapi.dll versione 5,0, fornita con Windows 2000, le stringhe delle voci di menu che contengono caratteri di tabulazione ( \\ t) potrebbero non essere visualizzate correttamente. Questa limitazione non si applica a Shlwapi.dll versioni 5,5 o successive. Ciò significa che i sistemi Windows XP e versioni successive non sono soggetti a questa limitazione. Il MSLU non ha questa limitazione.

### <a name="menuiteminfo"></a>MenuItemInfo

Questa funzione supporta solo la versione Microsoft Windows NT 4,0 della struttura [**MENUITEMINFOW**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . Questa struttura non dispone di un membro **hbmpItem** . Inoltre, la funzione non supporta il \_ flag bitmap MIIm. Il MSLU non presenta queste limitazioni.

### <a name="openfilename"></a>OPENFILENAME

Il membro **cbSize** della struttura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve essere impostato su sizeof (OPENFILENAME \_ NT4W).

Il membro **lpstrCustomFilter** della struttura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve essere impostato su **null**.

I valori dei membri **nMaxFile** e **NMaxFileTitle** della struttura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) non devono superare il percorso massimo \_ .

Se il membro **lpfnHook** della struttura [**OPENFILENAMEW**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) non è **null**, deve fare riferimento a una procedura di hook ANSI sulle piattaforme ANSI native e una procedura di hook Unicode su piattaforme Unicode native.

Il MSLU non presenta queste limitazioni.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage e PostMessage)

Sulle piattaforme ANSI native, nessuna conversione viene eseguita sul messaggio trasmesso o recuperato. Il messaggio trasmesso/recuperato è ANSI su piattaforme ANSI native e Unicode su piattaforme Unicode native. L'applicazione chiamante deve essere preparata a gestire entrambi i casi. Ad esempio, se il messaggio recuperato è WM \_ Char, il *wParam* è un codice carattere ANSI sulle piattaforme ANSI native, ma è un punto di codice Unicode sulle piattaforme Unicode native. Il MSLU non presenta queste limitazioni.

### <a name="queueuserworkitem"></a>QueueUserWorkItem

La funzione **SHQueueUserWorkItem** è leggermente diversa dalla funzione [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) corrispondente. Di seguito è illustrata la sintassi per **SHQueueUserWorkItem** .

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

-   I parametri *pfnCallback* e *pContext* hanno gli stessi significati della *funzione* e dei parametri di *contesto* , rispettivamente, di [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem).
-   Il parametro *dwTag* è inutilizzato e deve essere impostato su 0.
-   Il parametro *pdwld* è inutilizzato e deve essere impostato su **null**.
-   Il parametro *pszModule* punta a una stringa ANSI con terminazione null facoltativa che specifica il nome di una libreria da caricare prima che l'elemento di lavoro venga avviato e scaricato al termine dell'elemento di lavoro. Questo parametro può essere **NULL**.
-   Il parametro *dwFlags* supporta solo un subset dei valori supportati da [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem). Vengono riconosciuti i flag seguenti.

    

    | Nome              | Valore      | Significato                          |
    |-------------------|------------|----------------------------------|
    | \_EXECUTEIO TPS    | 0x00000001 | Uguale a WT \_ EXECUTEINIOTHREAD.   |
    | \_LONGEXECTIME TPS | 0x00000008 | Uguale a WT \_ EXECUTELONGFUNCTION. |

    

     

    > [!Note]  
    > Il \_ flag LONGEXECTIME di TPS non ha lo stesso valore numerico del \_ flag WT EXECUTELONGFUNCTION. Quando si usa **SHQueueUserWorkItem**, il parametro dwFlags deve essere una combinazione di valori di TPS \_ \* , non di \_ \* valori WT.

     

**SHQueueUserWorkItem** restituisce un valore diverso da zero se l'elemento di lavoro è stato accodato correttamente e 0 in caso contrario. Se la funzione ha esito negativo, è possibile utilizzare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere informazioni aggiuntive.

### <a name="registerclass"></a>RegisterClass

Sulle piattaforme ANSI native, non viene eseguita alcuna conversione sul membro **lpfnWndProc** della struttura [**WNDCLASSW**](/windows/win32/api/winuser/ns-winuser-wndclassa) . La finestra riceverà i messaggi della finestra ANSI sulle piattaforme ANSI native e i messaggi della finestra Unicode nelle piattaforme Unicode native. La procedura della finestra deve essere preparata per la gestione di entrambi i casi. Il MSLU non presenta queste limitazioni.

### <a name="regqueryvalueexw"></a>(RegQueryValueExW)

**RegQueryValueExWrapW** è stato anche chiamato con il nome **RegQueryValueExW**. Come per qualsiasi funzione senza nome esportata rigorosamente dall'ordinale, è possibile scegliere il nome che la funzione è nota nel codice.

### <a name="sendmessage"></a>SendMessage

Nelle piattaforme Unicode native la funzione **SendMessageWrapW** viene trasmessa alla funzione [**SendMessageW**](/windows/win32/api/winuser/nf-winuser-sendmessage) . Sulle piattaforme ANSI native, **SendMessageWrapW** offre un supporto limitato per la conversione di messaggi Unicode in ANSI. L'elenco dei messaggi supportati è indicato nella tabella seguente. La funzione non tradurrà altri messaggi.

Il MSLU non presenta queste limitazioni.



|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| CB \_ ADDSTRING        | (b) (f) (c)                                                                                               |
| CB \_ FindString       | (b) (f) (c)                                                                                               |
| CB \_ FindExactString  | (a) (f) (c)                                                                                               |
| CB \_ GETLBTEXT        | (b) (f) (c) (o) il buffer passato nel parametro *lParam* deve contenere spazio per almeno 256 caratteri.   |
| CB \_ GETLBTEXTLEN     | un                                                                                                       |
| CB \_ INSERTSTRING     | (b) (f) (c)                                                                                               |
| CB \_ SELECTSTRING     | (b) (f) (c)                                                                                               |
| \_CHARFROMPOS em      |                                                                                                           |
| \_riga em          | (e) il valore restituito è il numero di caratteri ANSI copiati.                                             |
| \_GETSEL em           |                                                                                                           |
| \_REPLACESEL em       | (b) (f)                                                                                                   |
| \_SETPASSWORDCHAR em  | un                                                                                                       |
| \_SETSEL em           |                                                                                                           |
| \_SETWORDBREAKPROC em | Questo messaggio non ha alcun effetto. La procedura di Word break non è impostata.                                          |
| \_ADDSTRING lb        | (b) (f) (d)                                                                                               |
| \_FindString lb       | (b) (f) (d)                                                                                               |
| \_FINDEXACTSTRING lb  | (b) (f) (lbs)                                                                                             |
| GetText LB \_          | (b) (f) (lbs) (o) il buffer passato nel parametro *lParam* deve contenere spazio per almeno 256 caratteri. |
| \_GETTEXTLEN lb       | un                                                                                                       |
| \_INSERTSTRING lb     | (b) (f) (d)                                                                                               |
| \_SELECTSTRING lb     | (b) (f) (d)                                                                                               |
| WM \_ GETtext          | (b) (f)                                                                                                   |
| \_GETTEXTLENGTH WM    | un                                                                                                       |
| \_testo WM          | (b) (f)                                                                                                   |
| \_SETTINGCHANGE WM    | (a) il messaggio viene inviato con un timeout di tre secondi.                                                  |



 


-   (a) la stringa ANSI da misurare o recuperare deve soddisfare la condizione seguente: la lunghezza della versione Unicode corrispondente della stringa non può superare la lunghezza della versione ANSI della stringa. Se questa condizione non viene soddisfatta, la lunghezza restituita sarà corta. Se la memoria disponibile non è sufficiente per determinare la lunghezza della stringa Unicode, la funzione restituisce zero, non LB \_ Err o CB \_ Err come previsto.
-   (b) se è necessaria la conversione della stringa, tutte le stringhe vengono convertite tramite la \_ tabella codici CP ACP.

    Questa funzione usa i caratteri più idonei e non esegue il controllo predefinito quando si esegue la conversione da Unicode ad ANSI. Inoltre, se la stringa non può essere convertita da Unicode a ANSI, la funzione passa una stringa null alla funzione ANSI sottostante. Questa situazione può verificarsi, ad esempio, quando la memoria è insufficiente. Il passaggio di una stringa null può causare l'esito negativo di alcune funzioni con un errore di parametro non valido, ma altre funzioni accettano la stringa null e la considerano come parametro previsto. Se, ad esempio, si verifica un errore quando il \_ wrapper del testo WM tenta di convertire il titolo della finestra in ANSI, la finestra avrà una didascalia vuota. La funzione non invia notifiche quando si verificano questi problemi. Il MSLU non presenta queste limitazioni.

-   (c) l'handle di finestra specificato deve essere l'handle di un controllo [ComboBox](../controls/combo-boxes.md) o [ComboBoxEx](../controls/comboboxex-controls.md) . Se l'handle è per un controllo ComboBox che è creato dal proprietario e non è stato creato con lo stile degli [stili della casella di riepilogo](../controls/list-box-styles.md) , la conversione di questo messaggio avrà esito negativo e potrebbe anche arrestarsi in modo anomalo.
-   (d) l'handle di finestra specificato deve essere l'handle per un controllo ListBox. Se il controllo ListBox è creato dal proprietario e non è stato creato con lo stile degli [stili della casella di riepilogo](../controls/list-box-styles.md) , la conversione di questo messaggio avrà esito negativo e potrebbe anche arrestarsi in modo anomalo.
-   (e) se è necessaria la conversione della stringa, tutte le stringhe vengono convertite tramite la \_ tabella codici CP ACP.

    Quando si esegue la conversione da ANSI a Unicode per l'output, le funzioni wrapper troncano la stringa restituita se non rientra nel buffer specificato. Il valore restituito per le funzioni che restituiscono il numero di caratteri copiati nel buffer o il numero di caratteri necessari per evitare il troncamento si riferisce al numero di caratteri ANSI copiati nel buffer o richiesti dalla funzione ANSI sottostante, non al numero di caratteri Unicode copiati nel buffer fornito da o richiesto dall'applicazione chiamante che ha chiamato la funzione wrapper. Il MSLU non ha questa limitazione. Per ulteriori informazioni, vedere [Microsoft Layer for Unicode nei sistemi Windows 95/98/me](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>(SetTimerQueueTimer)

La funzione **SHSetTimerQueueTimer** è leggermente diversa dalla funzione [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) corrispondente. La sintassi è la seguente:

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

-   Il parametro *hQueue* deve essere impostato su **null**, specificando la coda predefinita del timer.
-   I parametri *pfnCallback*, *pContext*, *dwDueTime* e *dwPeriod* hanno gli stessi significati dei parametri *callback*, *Parameter*, *DueTime* e *period* rispettivamente di [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).
-   Il parametro *lpszLibrary* è inutilizzato e deve essere impostato su **null**.
-   Il parametro *Flags* supporta solo un subset dei valori supportati da [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).

    

    | Nome              | Valore      | Significato                         |
    |-------------------|------------|---------------------------------|
    | \_EXECUTEIO TPS    | 0x00000001 | Uguale a WT \_ EXECUTEINIOTHREAD   |
    | \_LONGEXECTIME TPS | 0x00000008 | Uguale a WT \_ EXECUTELONGFUNCTION |

    

     

    > [!Note]  
    > Il \_ flag LONGEXECTIME di TPS non ha lo stesso valore numerico del \_ flag WT EXECUTELONGFUNCTION. Quando si usa **SHSetTimerQueueTimer**, il parametro *dwFlags* deve essere una combinazione di valori di TPS \_ \* , non di \_ \* valori WT.

     

**SHSetTimerQueueTimer** restituisce l'handle del timer creato in caso di esito positivo e **null** in caso contrario.

### <a name="shellexecuteex"></a>ShellExecuteEx

Il membro **lpFile** della struttura [**SHELLEXECUTEINFO**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) passato nel parametro only della funzione non può superare i caratteri di \_ \_ lunghezza URL Internet Max \_ . Se il \_ flag See mask \_ NomeClasse viene omesso, è necessario inizializzare il membro **lpClass** su **null**.

### <a name="valueex"></a>(ValueEx)

Sono supportati solo i tipi di dati del registro di sistema seguenti: REG \_ SZ, reg \_ expand \_ SZ, REG \_ Binary e reg \_ DWORD. A differenza di queste funzioni wrapper, MSLU supporta anche REG \_ \_ multiexpand \_ SZ.

### <a name="windowlong"></a>(WindowLong)

Nelle piattaforme ANSI native la funzione non esegue alcuna conversione in alcuna finestra Long. Se ad esempio si passa GWLP \_ WndProc, la funzione restituisce la routine della finestra ANSI, non un thunk. Il MSLU non presenta queste limitazioni.

 

 
