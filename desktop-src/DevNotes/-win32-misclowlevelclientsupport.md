---
description: Questo argomento contiene informazioni sulle API di basso livello usate dall'infrastruttura client di Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Supporto client vario Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877145"
---
# <a name="miscellaneous-low-level-client-support"></a>Supporto client vario Low-Level

Questo argomento contiene informazioni sulle API di basso livello usate dall'infrastruttura client di Windows.

### <a name="functions"></a>Funzioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></td>
<td>La funzione _lclose chiude il file specificato in modo che non sia più disponibile per la lettura o la scrittura. Questa funzione viene fornita per la compatibilità con le versioni di Windows a 16 bit. Le applicazioni basate su Win32 devono usare la funzione CloseHandle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></td>
<td>La funzione _lopen apre un file esistente e imposta il puntatore del file all'inizio del file. Questa funzione viene fornita per la compatibilità con le versioni di Windows a 16 bit. Le applicazioni basate su Win32 devono utilizzare la funzione CreateFile. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></td>
<td>La funzione _lread legge i dati dal file specificato. Questa funzione viene fornita per la compatibilità con le versioni di Windows a 16 bit. Le applicazioni basate su Win32 devono usare la funzione ReadFile. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></td>
<td>Restituisce un valore che indica se i codec DVD sono abilitati nel dispositivo corrente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></td>
<td>Disabilita la funzionalità di ghosting della finestra per il processo GUI chiamante. Il fantasma della finestra è una funzionalità di Windows Manager che consente all'utente di ridurre, spostare o chiudere la finestra principale di un'applicazione che non risponde.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></td>
<td>Restituisce un elenco di proprietà per tutti i codec multimediali installati nel sistema che soddisfano i requisiti specificati.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></td>
<td>Crea una factory di comunicazione per la registrazione di un'estensione per supporti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></td>
<td>Crea un'istanza di una classe in un pacchetto dell'applicazione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></td>
<td>Ottiene un valore che indica se il comportamento del supporto associato al GUID specificato è abilitato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></td>
<td>Deprecato. Questa funzione viene utilizzata per chiudere l'handle specificato. <a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> viene sostituito da <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></td>
<td>Deprecato. Compila i descrittori per i buffer forniti e passa i dati non tipizzati al driver di dispositivo associato all'handle di file. <a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> viene sostituito da <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></td>
<td>Deprecato. Attende che l'oggetto specificato raggiunga uno stato <code>signaled</code> . <a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> viene sostituito da <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></td>
<td>Converte la stringa di origine ANSI specificata in una stringa Unicode. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></td>
<td>Converte una stringa di caratteri in un Integer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></td>
<td>Inizializza il buffer fornito con una rappresentazione di stringa del SID per l'utente corrente. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></td>
<td>Libera il buffer di stringa allocato da <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></td>
<td>Libera il buffer di stringa allocato da <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></td>
<td>Libera il buffer di stringa allocato da <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> o da <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></td>
<td>Inizializza una stringa calcolata. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></td>
<td>Inizializza una stringa Unicode conteggiata. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></td>
<td>Converte la stringa di origine Unicode specificata in una stringa ANSI. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></td>
<td>Questa funzione converte la stringa di origine Unicode specificata in una stringa OEM. La traduzione viene eseguita rispetto alla tabella codici OEM (OCP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></td>
<td>Determina il numero di byte necessari per rappresentare una stringa Unicode come stringa ANSI.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></td>
<td>La funzione <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> converte la stringa Unicode specificata in una nuova stringa di caratteri, usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></td>
<td>La funzione <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> converte la stringa di origine specificata in una stringa Unicode, usando la tabella codici UTF-8.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></td>
<td>Specifica un'azione o un'elaborazione per l'IME (Input Method Editor) tramite una sottofunzione specificata.
<blockquote>
[!Note]<br />
Questa funzione è obsoleta e non deve essere utilizzata.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></td>
<td>Abilita o Disabilita temporaneamente un IME e, allo stesso tempo, attiva o disattiva la visualizzazione di tutte le finestre di proprietà dell'IME.
<blockquote>
[!Note]<br />
Questa funzione è obsoleta e non deve essere utilizzata.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Strutture



| Argomento                                 | Contenuto                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMESTRUCT**](/windows/win32/api/ime/ns-ime-imestruct) | Utilizzato da [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) per specificare la funzione subfunction da eseguire nel messaggio IME e i relativi parametri. Questa struttura viene utilizzata anche per ricevere i valori restituiti da tali funzioni.<br/> |
| [**STRINGA**](/windows/desktop/api/Winternl/ns-winternl-string)       | Questa struttura viene utilizzata con la funzione [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) . <br/>                                                                                                              |



 

### <a name="compiler-routines"></a>Routine del compilatore



| Argomento                                                             | Contenuto                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_\_\_Routine del gestore specifico di C \_**](--c-specific-handler2.md) | Il [**\_ \_ \_ \_ gestore specifico di c**](--c-specific-handler2.md) è una routine di supporto per il compilatore c.<br/> |
| [\_Routine alldiv](-win32-alldiv.md)                             | la [ \_ routine alldiv](-win32-alldiv.md) è una routine di supporto per il compilatore C.<br/>                     |
| [\_allmul](-win32-allmul.md) | Moltiplica due **LONGLONG** o **ULONGLONG**. |
| [\_aulldiv](-win32-aulldiv.md) | Divide due interi **ULONGLONG** . |
| [\_Routine chkstk](-win32-chkstk.md)                             | la [ \_ routine chkstk](-win32-chkstk.md) è una routine di supporto per il compilatore C.<br/>                     |
