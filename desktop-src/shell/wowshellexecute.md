---
description: Esegue un'operazione su un file specificato.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 841c30be827ddabc40bd8af50423c844ce927e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524426"
---
# <a name="wowshellexecute-function"></a>WOWShellExecute (funzione)

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Esegue un'operazione su un file specificato. **WOWShellExecute** è disponibile solo per l'utilizzo con la macchina virtuale dos (Ntvdm.exe) di Microsoft Windows NT, che consente l'esecuzione di software DOS (Disk Operating System) e software a 16 bit in un sistema Windows e che non devono essere utilizzati da altri utenti. In alternativa, usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="syntax"></a>Sintassi


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra proprietaria utilizzato per visualizzare un'interfaccia utente o messaggi di errore. Questo valore può essere **null** se l'operazione non è associata a una finestra.

</dd> <dt>

*lpOperation* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a una stringa con terminazione **null**, a cui si fa riferimento in questo caso come *verbo*, che specifica l'azione da eseguire. Il set di verbi disponibili dipende dal file o dalla cartella specifica. In genere, le azioni disponibili dal menu di scelta rapida di un oggetto sono i verbi disponibili. Per ulteriori informazioni sui verbi e sulla relativa disponibilità, vedere la sezione relativa ai *verbi degli oggetti* di [avvio delle applicazioni](launch.md). Per ulteriori informazioni sui menu di scelta rapida, vedere [estensione dei menu di scelta rapida](context.md) . I verbi seguenti sono comunemente usati.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**modifica**


</dt> <dd>

Avvia un editor e apre il documento per la modifica. Se *lpFile* non è un file di documento, la funzione avrà esito negativo.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**esplorare**


</dt> <dd>

Esplora la cartella specificata da *lpFile*.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**trovare**


</dt> <dd>

Avvia una ricerca a partire dalla directory specificata.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**aprire**


</dt> <dd>

Apre il file specificato dal parametro *lpFile* . Il file può essere un file eseguibile, un file di documento o una cartella.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**stampa**


</dt> <dd>

Stampa il file di documento specificato da *lpFile*. Se *lpFile* non è un file di documento, la funzione avrà esito negativo.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**NULL**


</dt> <dd>

Per i sistemi precedenti a Windows 2000, viene usato il verbo predefinito se è valido e disponibile nel registro di sistema. In caso contrario, viene utilizzato il verbo "Open".

Per i sistemi Windows 2000 e versioni successive, viene usato il verbo predefinito, se disponibile. In caso contrario, viene utilizzato il verbo "Open". Se nessuno dei due verbi è disponibile, il sistema usa il primo verbo elencato nel registro di sistema.

</dd> </dl> </dd> <dt>

*lpFile* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a una stringa con terminazione **null** che specifica il file o l'oggetto su cui eseguire il verbo specificato. Per specificare un oggetto spazio dei nomi della shell, passare il nome completo dell'analisi. Si noti che non tutti i verbi sono supportati in tutti gli oggetti. Ad esempio, non tutti i tipi di documento supportano il verbo "Print".

</dd> <dt>

*lpParameters* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Se il parametro *lpFile* specifica un file eseguibile, *lpParameters* è un puntatore a una stringa con terminazione **null** che specifica i parametri da passare all'applicazione. Il formato di questa stringa è determinato dal verbo da richiamare. Se *lpFile* specifica un file di documento, *LpParameters* deve essere **null**.

</dd> <dt>

*lpDirectory* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a una stringa con terminazione **null** che specifica la directory predefinita.

</dd> <dt>

*nShowCmd* \[ in\]
</dt> <dd>

Tipo: **int**

Flag che specificano la modalità di visualizzazione di un'applicazione all'apertura. Se *lpFile* specifica un file di documento, il flag viene semplicemente passato all'applicazione associata. Spetta all'applicazione decidere come gestirla.

<dt>

<span id="SW_HIDE"></span><span id="sw_hide"></span>

<span id="SW_HIDE"></span><span id="sw_hide"></span>**Nascondi il SW \_**


</dt> <dd>

Nasconde la finestra e attiva un'altra finestra.

</dd> <dt>

<span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>

<span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>**\_ingrandimento SW**


</dt> <dd>

Ingrandisce la finestra specificata.

</dd> <dt>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW \_ Riduci a icona**


</dt> <dd>

Riduce a icona la finestra specificata e attiva la finestra di primo livello successiva nell'ordine z.

</dd> <dt>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>**\_ripristino SW**


</dt> <dd>

Attiva e visualizza la finestra. Se la finestra è ridotta a icona o ingrandita, Windows ne ripristina le dimensioni e la posizione originali. Un'applicazione deve specificare questo flag durante il ripristino di una finestra ridotta a icona.

</dd> <dt>

<span id="SW_SHOW"></span><span id="sw_show"></span>

<span id="SW_SHOW"></span><span id="sw_show"></span>**\_visualizzazione SW**


</dt> <dd>

Attiva la finestra e la Visualizza nelle dimensioni e nella posizione correnti.

</dd> <dt>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**\_SHOWDEFAULT SW**


</dt> <dd>

Imposta lo stato di visualizzazione basato sul \_ flag SW specificato nella struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) passata alla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) dal programma che ha avviato l'applicazione. Un'applicazione deve chiamare [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) con questo flag per impostare lo stato di visualizzazione iniziale della finestra principale.

</dd> <dt>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**\_SHOWMAXIMIZED SW**


</dt> <dd>

Attiva la finestra e la Visualizza come finestra ingrandita.

</dd> <dt>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**\_SHOWMINIMIZED SW**


</dt> <dd>

Attiva la finestra e la Visualizza come finestra ridotta a icona.

</dd> <dt>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**\_SHOWMINNOACTIVE SW**


</dt> <dd>

Visualizza la finestra come finestra ridotta a icona. La finestra attiva rimane attiva.

</dd> <dt>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW \_ visualizzato**


</dt> <dd>

Consente di visualizzare la finestra nello stato corrente. La finestra attiva rimane attiva.

</dd> <dt>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**\_SHOWNOACTIVATE SW**


</dt> <dd>

Visualizza una finestra nelle dimensioni e nella posizione più recenti. La finestra attiva rimane attiva.

</dd> <dt>

<span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>

<span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>**\_SHOWNORMAL SW**


</dt> <dd>

Attiva e visualizza una finestra. Se la finestra è ridotta a icona o ingrandita, Windows ne ripristina le dimensioni e la posizione originali. Un'applicazione deve specificare questo flag quando la finestra viene visualizzata per la prima volta.

</dd> </dl> </dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Tipo: **void \** _

Funzione di callback utilizzata per chiamare [_ *CreateProcess* *](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) nel kernel a 16 bit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HINSTANCE**

Restituisce un valore maggiore di 32 in caso di esito positivo o un valore di errore minore o uguale a 32 in caso contrario. Nella tabella seguente sono elencati i valori di errore. Viene eseguito il cast del valore restituito come HINSTANCE per la compatibilità con le versioni precedenti delle applicazioni Windows a 16 bit. Tuttavia, non si tratta di un vero e proprio HINSTANCE. L'unica cosa che può essere eseguita con il HINSTANCE restituito è eseguirne il cast a un valore **int** e confrontarlo con il valore 32 o uno dei codici di errore riportati di seguito.



| Codice restituito                                                                                             | Descrizione                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | Memoria o risorse insufficienti per il sistema operativo.<br/>                                                                                                           |
| <dl> <dt>**FILE di errore \_ \_ non \_ trovato**</dt> </dl>  | Il file specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**il percorso dell'errore non è stato \_ \_ \_ trovato**</dt> </dl>  | Il percorso specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**\_formato errore errato \_**</dt> </dl>       | Il file exe non è valido (non Win32. exe o errore nell'immagine exe).<br/>                                                                                             |
| <dl> <dt>**SE \_ Err \_ AccessDenied**</dt> </dl>    | Il sistema operativo ha negato l'accesso al file specificato.<br/>                                                                                                     |
| <dl> <dt>**SE \_ Err \_ ASSOCINCOMPLETE**</dt> </dl> | L'associazione del nome file è incompleta o non valida.<br/>                                                                                                           |
| <dl> <dt>**SE \_ Err \_ DDEBUSY**</dt> </dl>         | Non è stato possibile completare la transazione DDE perché sono in corso l'elaborazione di altre transazioni DDE.<br/>                                                               |
| <dl> <dt>**SE \_ Err \_ DDEFAIL**</dt> </dl>         | Transazione DDE non riuscita.<br/>                                                                                                                                   |
| <dl> <dt>**SE \_ Err \_ DDETIMEOUT**</dt> </dl>      | Non è stato possibile completare la transazione DDE perché si è verificato il timeout della richiesta.<br/>                                                                                     |
| <dl> <dt>**SE \_ Err \_ DLLNOTFOUND**</dt> </dl>     | Impossibile trovare la DLL specificata.<br/>                                                                                                                              |
| <dl> <dt>**SE \_ Err \_ FNF**</dt> </dl>             | Il file specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**SE \_ Err \_ NOASSOC**</dt> </dl>         | All'estensione di file specificata non è associata alcuna applicazione. Questo errore viene restituito anche se si tenta di stampare un file non stampabile.<br/> |
| <dl> <dt>**SE \_ Err \_**</dt> </dl>             | Memoria insufficiente per completare l'operazione.<br/>                                                                                                        |
| <dl> <dt>**SE \_ Err \_ PNF**</dt> </dl>             | Il percorso specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**SE \_ Err, \_ condivisione**</dt> </dl>           | Si è verificata una violazione di condivisione.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

**WOWShellExecute** non è incluso in un'intestazione o in un file con estensione LIB. Viene esportato da Shell32.dll in base al nome.

Questo metodo consente di eseguire qualsiasi comando nel menu di scelta rapida di una cartella o di archiviarlo nel registro di sistema.

Se *lpOperation* è **null**, la funzione apre il file specificato da *lpFile*. Se *lpOperation* è "Open" o "Explore", la funzione tenta di aprire o esplorare la cartella.

Per ottenere informazioni sull'applicazione avviata come risultato della chiamata a **WOWShellExecute**, utilizzare [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

> [!Note]  
> Le **finestre della cartella di avvio in un'impostazione di processo separata** in Opzioni cartella influiscono su **WOWShellExecute**. Se questa opzione è disabilitata (impostazione predefinita), **WOWShellExecute** usa una finestra di Esplora risorse anziché avviarne una nuova. Se non è aperta alcuna finestra di Esplora risorse, **WOWShellExecute** ne avvia una nuova.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
