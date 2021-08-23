---
description: Esegue un'operazione su un file specificato.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Funzione WOWShellExecute
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
ms.openlocfilehash: 4389c348a06b7c54dc899da8114eee09e740681f043084bb0c32ab9f7163772e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591831"
---
# <a name="wowshellexecute-function"></a>Funzione WOWShellExecute

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Esegue un'operazione su un file specificato. **WOWShellExecute** esiste solo per l'uso con Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), che consente l'esecuzione del sistema operativo su disco (DOS) e del software a 16 bit in un sistema Windows e non deve essere usato da altri utenti. In [**alternativa, usare ShellExecute.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)

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

*hwnd* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra proprietaria usata per visualizzare un'interfaccia utente o messaggi di errore. Questo valore può essere **NULL** se l'operazione non è associata a una finestra.

</dd> <dt>

*lpOperation* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a una stringa con terminazione **Null,** definita in questo caso *come verbo*, che specifica l'azione da eseguire. Il set di verbi disponibili dipende dal file o dalla cartella specifica. In genere, le azioni disponibili nel menu di scelta rapida di un oggetto sono verbi disponibili. Per altre informazioni sui verbi e sulla relativa disponibilità, vedere la sezione *Verbi oggetto* di [Avvio di applicazioni](launch.md). Per altre informazioni sui menu di scelta [rapida,](context.md) vedere Estensione dei menu di scelta rapida. Vengono comunemente usati i verbi seguenti.

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span id="edit"></span><span id="EDIT"></span>**Modifica**


</dt> <dd>

Avvia un editor e apre il documento per la modifica. Se *lpFile non* è un file di documento, la funzione avrà esito negativo.

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span id="explore"></span><span id="EXPLORE"></span>**Esplorare**


</dt> <dd>

Esplora la cartella specificata da *lpFile*.

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span id="find"></span><span id="FIND"></span>**Trovare**


</dt> <dd>

Avvia una ricerca a partire dalla directory specificata.

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span id="open"></span><span id="OPEN"></span>**Aperto**


</dt> <dd>

Apre il file specificato dal *parametro lpFile.* Il file può essere un file eseguibile, un file di documento o una cartella.

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span id="print"></span><span id="PRINT"></span>**Stampare**


</dt> <dd>

Stampa il file di documento specificato da *lpFile*. Se *lpFile non* è un file di documento, la funzione avrà esito negativo.

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span id="NULL"></span><span id="null"></span>**Null**


</dt> <dd>

Per i sistemi precedenti Windows 2000, viene usato il verbo predefinito se è valido e disponibile nel Registro di sistema. In caso contrario, viene usato il verbo "open".

Per Windows 2000 e versioni successive, viene usato il verbo predefinito, se disponibile. In caso contrario, viene usato il verbo "open". Se nessuno dei due verbi è disponibile, il sistema usa il primo verbo elencato nel Registro di sistema.

</dd> </dl> </dd> <dt>

*lpFile* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a una **stringa con** terminazione Null che specifica il file o l'oggetto su cui eseguire il verbo specificato. Per specificare un oggetto spazio dei nomi Shell, passare il nome di analisi completo. Si noti che non tutti i verbi sono supportati in tutti gli oggetti. Ad esempio, non tutti i tipi di documento supportano il verbo "print".

</dd> <dt>

*lpParameters* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Se il *parametro lpFile* specifica un file eseguibile, *lpParameters* è un puntatore a una stringa con terminazione **Null** che specifica i parametri da passare all'applicazione. Il formato di questa stringa è determinato dal verbo che deve essere richiamato. Se *lpFile specifica* un file di documento, *lpParameters* deve essere **NULL.**

</dd> <dt>

*lpDirectory* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore a una **stringa con** terminazione Null che specifica la directory predefinita.

</dd> <dt>

*nShowCmd* \[ Pollici\]
</dt> <dd>

Tipo: **INT**

Flag che specificano la modalità di visualizzazione di un'applicazione all'apertura. Se *lpFile* specifica un file di documento, il flag viene semplicemente passato all'applicazione associata. È l'applicazione a decidere come gestirla. Può essere uno dei valori che possono essere specificati nel *parametro nCmdShow* per la [funzione ShowWindow.](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> <dt>

*lpfnCBWinExec* 
</dt> <dd>

Tipo: **\* void**

Funzione di callback usata per [**chiamare CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) nel kernel a 16 bit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HINSTANCE**

Restituisce un valore maggiore di 32 in caso di esito positivo oppure un valore di errore minore o uguale a 32 in caso contrario. Nella tabella seguente sono elencati i valori di errore. Il cast del valore restituito viene eseguito come HINSTANCE per garantire la compatibilità con le versioni precedenti con applicazioni Windows a 16 bit. Non si tratta tuttavia di una vera HINSTANCE. L'unica operazione che può essere eseguita con HINSTANCE restituita è eseguire il cast a **un valore int** e confrontarlo con il valore 32 o uno dei codici di errore seguenti.



| Codice restituito                                                                                             | Descrizione                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>                        | Memoria o risorse insufficiente per il sistema operativo.<br/>                                                                                                           |
| <dl> <dt>**FILE \_ DI ERRORE NON \_ \_ TROVATO**</dt> </dl>  | Il file specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**PERCORSO \_ ERRORE \_ NON \_ TROVATO**</dt> </dl>  | Il percorso specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**ERRORE \_ FORMATO \_ NON VALIDO**</dt> </dl>       | Il .exe file non è valido (non Win32 .exe o errore nell'.exe immagine).<br/>                                                                                             |
| <dl> <dt>**\_edizione Standard ACCESSO ERR \_ NEGATO**</dt> </dl>    | Il sistema operativo ha negato l'accesso al file specificato.<br/>                                                                                                     |
| <dl> <dt>**\_edizione Standard ERR \_ ASSOCINCOMPLETE**</dt> </dl> | L'associazione del nome file non è completa o non è valida.<br/>                                                                                                           |
| <dl> <dt>**\_edizione Standard ERR \_ DDEBUSY**</dt> </dl>         | Impossibile completare la transazione DDE perché sono in corso l'elaborazione di altre transazioni DDE.<br/>                                                               |
| <dl> <dt>**\_edizione Standard ERR \_ DDEFAIL**</dt> </dl>         | La transazione DDE non è riuscita.<br/>                                                                                                                                   |
| <dl> <dt>**\_edizione Standard ERR \_ DDETIMEOUT**</dt> </dl>      | Impossibile completare la transazione DDE perché si è verificata la richiesta.<br/>                                                                                     |
| <dl> <dt>**\_edizione Standard ERR \_ DLLNOTFOUND**</dt> </dl>     | La DLL specificata non è stata trovata.<br/>                                                                                                                              |
| <dl> <dt>**\_edizione Standard ERR \_ FNF**</dt> </dl>             | Il file specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**\_edizione Standard ERR \_ NOASSOC**</dt> </dl>         | Non è presente alcuna applicazione associata all'estensione di file specificata. Questo errore verrà restituito anche se si tenta di stampare un file non stampabile.<br/> |
| <dl> <dt>**\_edizione Standard ERR \_ OOM**</dt> </dl>             | Memoria insufficiente per completare l'operazione.<br/>                                                                                                        |
| <dl> <dt>**\_edizione Standard ERR \_ PNF**</dt> </dl>             | Il percorso specificato non è stato trovato.<br/>                                                                                                                             |
| <dl> <dt>**\_edizione Standard CONDIVISIONE \_ ERR**</dt> </dl>           | Si è verificata una violazione di condivisione.<br/>                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

**WOWShellExecute** non è incluso in un file di intestazione o lib. Viene esportato dal Shell32.dll in base al nome.

Questo metodo consente di eseguire qualsiasi comando nel menu di scelta rapida di una cartella o archiviato nel Registro di sistema.

Se *lpOperation* è **NULL,** la funzione apre il file specificato da *lpFile*. Se *lpOperation* è "open" o "explore", la funzione tenta di aprire o esplorare la cartella.

Per ottenere informazioni sull'applicazione avviata in seguito alla chiamata a **WOWShellExecute,** usare [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

> [!Note]  
> Le **finestre della cartella di avvio in un processo separato** in Opzioni cartella influiscono su **WOWShellExecute.** Se questa opzione è disabilitata (impostazione predefinita), **WOWShellExecute** usa una finestra di Explorer aperta anziché avviarne una nuova. Se non è aperta alcuna finestra di Esplora risorse, **WOWShellExecute** ne avvia una nuova.

 

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

 

 
