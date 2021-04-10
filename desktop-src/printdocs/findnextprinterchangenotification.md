---
description: La funzione FindNextPrinterChangeNotification recupera le informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Funzione FindNextPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882825"
---
# <a name="findnextprinterchangenotification-function"></a>FindNextPrinterChangeNotification (funzione)

La funzione **FindNextPrinterChangeNotification** recupera le informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa. Chiamare questa funzione quando viene soddisfatta un'operazione di attesa sull'oggetto notifica di modifica.

La funzione Reimposta anche l'oggetto notifica di modifica sullo stato non segnalato. È quindi possibile usare l'oggetto in un'altra operazione di attesa per continuare a monitorare la stampante o il server di stampa. Il sistema operativo imposterà l'oggetto sullo stato segnalato la volta successiva in cui si verificherà un set di modifiche specificato per la stampante o il server di stampa. La funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crea l'oggetto notifica di modifica e specifica il set di modifiche da monitorare.

## <a name="syntax"></a>Sintassi


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hChange* \[ in\]
</dt> <dd>

Handle per un oggetto notifica di modifica associato a una stampante o a un server di stampa. È possibile ottenere tale handle chiamando la funzione [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Il sistema operativo imposta questo oggetto notifica di modifica sullo stato segnalato quando rileva una delle modifiche specificate nel filtro delle notifiche di modifica dell'oggetto.

</dd> <dt>

*pdwChange* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile i cui bit sono impostati per indicare le modifiche che hanno causato la notifica più recente. I flag di bit che possono essere impostati corrispondono a quelli specificati nel parametro *fdwFilter* della chiamata [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . Il sistema imposta uno o più dei seguenti flag di bit.



| Valore                                                                                                                                                                                                                                             | Significato                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**\_modulo di \_ aggiunta della modifica della stampante \_**</dt> </dl>                                                     | Un modulo è stato aggiunto al server.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**modifica della stampante \_ \_ Aggiungi \_ processo**</dt> </dl>                                                        | Un processo di stampa è stato inviato alla stampante.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**modifica della stampante \_ \_ Aggiungi \_ porta**</dt> </dl>                                                     | Una porta o un monitoraggio è stato aggiunto al server.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**\_modifica stampante \_ Aggiungi \_ processore di stampa \_**</dt> </dl>                   | Un processore di stampa è stato aggiunto al server.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**\_modifica stampante \_ Aggiungi \_ stampante**</dt> </dl>                                            | È stata aggiunta una stampante al server.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**\_modifica stampante \_ Aggiungi \_ driver della stampante \_**</dt> </dl>                      | Un driver della stampante è stato aggiunto al server.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**modifica della stampante \_ \_ configurare la \_ porta**</dt> </dl>                                   | Una porta è stata configurata nel server.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**\_modulo di \_ eliminazione della modifica della stampante \_**</dt> </dl>                                            | Un modulo è stato eliminato dal server.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**\_processo di \_ eliminazione della modifica della stampante \_**</dt> </dl>                                               | Un processo è stato eliminato.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**\_porta di \_ eliminazione delle modifiche della stampante \_**</dt> </dl>                                            | Una porta o un monitoraggio è stato eliminato dal server.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**\_modifica stampante \_ Elimina \_ processore di stampa \_**</dt> </dl>          | Un processore di stampa è stato eliminato dal server.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**\_modifica stampante \_ Elimina \_ stampante**</dt> </dl>                                   | Una stampante è stata eliminata.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**modifica stampante- \_ \_ Elimina \_ driver della stampante \_**</dt> </dl>             | Un driver della stampante è stato eliminato dal server.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**\_modifica stampante \_ non \_ riuscita \_ stampante di connessione**</dt> </dl> | Errore di connessione alla stampante.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**\_modulo del \_ set di modifiche della stampante \_**</dt> </dl>                                                     | Un modulo è stato impostato sul server.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**\_processo del \_ set di modifiche della stampante \_**</dt> </dl>                                                        | Un processo è stato impostato.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**\_ \_ stampante set di modifiche stampante \_**</dt> </dl>                                            | È stata impostata una stampante.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**\_ \_ \_ driver della stampante del set di modifiche della stampante \_**</dt> </dl>                      | È stato impostato un driver della stampante.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**\_processo di \_ scrittura \_ modifica stampante**</dt> </dl>                                                  | I dati del processo sono stati scritti.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**\_timeout modifica \_ stampante**</dt> </dl>                                                         | Timeout del processo.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_server di modifica della stampante \_**</dt> </dl>                                                            | Windows 7: è stata apportata una modifica nel server.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ Opzioni di notifica della stampante**](printer-notify-options.md) . Impostare il membro **Flags** di questa struttura su **Printer \_ Notify \_ Options \_ Refresh** per fare in modo che la funzione restituisca i dati correnti per tutti i campi di informazioni sulla stampante monitorata. La funzione ignora tutti gli altri membri della struttura. Questo parametro può essere **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile puntatore che riceve un puntatore a un buffer di sola lettura allocato dal sistema. Chiamare la funzione [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) per liberare il buffer al termine dell'operazione. Questo parametro può essere **null** se non è richiesta alcuna informazione.

Il buffer contiene una struttura di [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) , che contiene una matrice di strutture di [**\_ \_ \_ dati di notifica della stampante**](printer-notify-info-data.md) . Ogni elemento della matrice contiene informazioni su uno dei campi specificati nel parametro *pPrinterNotifyOptions* della chiamata [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . In genere, la funzione fornisce dati solo per i campi modificati in modo da generare la notifica più recente. Tuttavia, se la struttura a cui punta il parametro *pPrinterNotifyOptions* specifica **l' \_ \_ \_ aggiornamento delle opzioni di notifica della stampante**, la funzione fornisce dati per tutti i campi monitorati.

Se il bit delle **\_ \_ informazioni \_ di notifica della stampante** è impostato nel membro **flag** della struttura delle [**\_ \_ informazioni di notifica della stampante**](printer-notify-info.md) , si è verificato un overflow o si è verificato un errore e le notifiche potrebbero andare perse. In questo caso, non verranno inviate notifiche aggiuntive fino a quando non si effettua una seconda chiamata **FindNextPrinterChangeNotification** che specifica l' **aggiornamento delle \_ Opzioni di notifica \_ \_ della stampante**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Chiamare la funzione **FindNextPrinterChangeNotification** dopo che un'operazione di attesa su un oggetto notifica creato da [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) è stata soddisfatta. La chiamata a **FindNextPrinterChangeNotification** consente di ottenere informazioni sulla modifica che ha soddisfatto l'operazione di attesa e di reimpostare l'oggetto notifica in modo che possa essere segnalato quando si verifica la modifica successiva.

Con un'eccezione, non chiamare la funzione **FindNextPrinterChangeNotification** se l'oggetto notifica di modifica non è nello stato segnalato. Se una funzione wait restituisce il **\_ timeout di attesa** del valore, l'oggetto Change non è nello stato segnalato. Chiamare la funzione **FindNextPrinterChangeNotification** solo se la funzione wait riesce senza scadere. L'eccezione si verifica quando viene chiamato **FindNextPrinterChangeNotification** con il bit di **aggiornamento delle \_ Opzioni di notifica \_ \_ della stampante** impostato nel parametro *pPrinterNotifyOptions* . Si noti che anche quando questo flag è impostato, è comunque possibile che il flag per le **\_ \_ informazioni \_ di notifica della stampante** non sia impostato nel parametro *ppPrinterNotifyInfo* .

Per continuare a monitorare la stampante o il server di stampa per le modifiche, ripetere il ciclo di chiamata a una delle [funzioni di attesa](/windows/desktop/Sync/wait-functions) e quindi chiamare la funzione **FindNextPrinterChangeNotification** per esaminare la modifica e reimpostare l'oggetto notifica.

**FindNextPrinterChangeNotification** può combinare più modifiche allo stesso campo di informazioni della stampante in una singola notifica. Quando si verifica questa situazione, la funzione comprime in genere tutte le modifiche per il campo in una singola voce della matrice delle strutture di [**dati di \_ notifica delle \_ informazioni \_ di stampa**](printer-notify-info-data.md) in *ppPrinterNotifyInfo*. la singola voce riporta solo le informazioni più aggiornate. Tuttavia, per alcuni campi di informazioni su processi e stampanti, la funzione può restituire più voci di matrice per lo stesso campo. In questo caso, l'ultima voce di matrice per il campo indica i dati correnti e le voci precedenti contengono i dati per le fasi intermedie.

Quando l'oggetto notifica di modifica non è più necessario, chiuderlo chiamando la funzione [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

> [!Note]  
> In Windows XP con Service Pack 2 (SP2) e versioni successive, il firewall connessione Internet (ICF) blocca le porte della stampante per impostazione predefinita, ma è possibile abilitare un'eccezione per la condivisione di file e stampanti. Se un utente esegue una connessione alla stampante a un altro computer e l'eccezione non è abilitata, l'utente non riceverà le notifiche di modifica della stampante dal server. Un amministratore del computer dovrà abilitare l'eccezione.

 

## <a name="examples"></a>Esempio

Nell'esempio di codice riportato di seguito viene illustrato come è possibile monitorare lo stato della stampante utilizzando queste funzioni.


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_informazioni notifica \_ stampante**](printer-notify-info.md)
</dt> <dt>

[**\_dati delle \_ informazioni di notifica della stampante \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_Opzioni di notifica stampanti \_**](printer-notify-options.md)
</dt> </dl>

 

