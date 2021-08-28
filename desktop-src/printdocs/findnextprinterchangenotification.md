---
description: La funzione FindNextPrinterChangeNotification recupera informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: Funzione FindNextPrinterChangeNotification (Winspool.h)
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
ms.openlocfilehash: 37b05603a75f7bc8e68ead2d0dffdec2e99e7618e5461360760f2d9c89ae52da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112481"
---
# <a name="findnextprinterchangenotification-function"></a>Funzione FindNextPrinterChangeNotification

La **funzione FindNextPrinterChangeNotification** recupera informazioni sulla notifica di modifica più recente per un oggetto notifica di modifica associato a una stampante o a un server di stampa. Chiamare questa funzione quando viene soddisfatta un'operazione di attesa sull'oggetto notifica di modifica.

La funzione reimposta anche l'oggetto notifica di modifica sullo stato non segnalato. È quindi possibile usare l'oggetto in un'altra operazione di attesa per continuare a monitorare la stampante o il server di stampa. Il sistema operativo imposta l'oggetto sullo stato segnalato la volta successiva che si verifica una delle modifiche specificate nella stampante o nel server di stampa. La [**funzione FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crea l'oggetto notifica delle modifiche e specifica il set di modifiche da monitorare.

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

*hChange* \[ Pollici\]
</dt> <dd>

Handle per un oggetto notifica di modifica associato a una stampante o a un server di stampa. Per ottenere tale handle, chiamare la [**funzione FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) Il sistema operativo imposta questo oggetto notifica di modifica sullo stato segnalato quando rileva una delle modifiche specificate nel filtro di notifica delle modifiche dell'oggetto.

</dd> <dt>

*pdwChange* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile i cui bit sono impostati per indicare le modifiche che hanno causato la notifica più recente. I flag di bit che possono essere impostati corrispondono a quelli specificati nel *parametro fdwFilter* della [**chiamata FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) Il sistema imposta uno o più dei flag di bit seguenti.



| Valore                                                                                                                                                                                                                                             | Significato                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <dt>**MODIFICA \_ DELLA STAMPANTE - AGGIUNGI \_ \_ MODULO**</dt> </dl>                                                     | È stato aggiunto un modulo al server.<br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <dt>**MODIFICA STAMPANTE \_ \_ - AGGIUNGI \_ PROCESSO**</dt> </dl>                                                        | Un processo di stampa è stato inviato alla stampante.<br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <dt>**MODIFICA DELLA \_ STAMPANTE \_ AGGIUNGI \_ PORTA**</dt> </dl>                                                     | È stata aggiunta una porta o un monitor al server.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <dt>**MODIFICA DELLA \_ STAMPANTE \_ - AGGIUNGI \_ PROCESSORE DI \_ STAMPA**</dt> </dl>                   | È stato aggiunto un processore di stampa al server.<br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <dt>**MODIFICA \_ DELLA STAMPANTE AGGIUNGI \_ \_ STAMPANTE**</dt> </dl>                                            | È stata aggiunta una stampante al server.<br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <dt>**MODIFICA DELLA \_ STAMPANTE AGGIUNGI DRIVER DELLA \_ \_ \_ STAMPANTE**</dt> </dl>                      | È stato aggiunto un driver della stampante al server.<br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <dt>**MODIFICA \_ DELLA STAMPANTE CONFIGURARE LA \_ \_ PORTA**</dt> </dl>                                   | Nel server è stata configurata una porta.<br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <dt>**MODULO DI \_ ELIMINAZIONE MODIFICA \_ \_ STAMPANTE**</dt> </dl>                                            | Un modulo è stato eliminato dal server.<br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <dt>**PROCESSO DI \_ ELIMINAZIONE MODIFICA \_ \_ STAMPANTE**</dt> </dl>                                               | Un processo è stato eliminato.<br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <dt>**CAMBIARE \_ LA PORTA DI ELIMINAZIONE DELLA \_ \_ STAMPANTE**</dt> </dl>                                            | Una porta o un monitoraggio è stato eliminato dal server.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <dt>**MODIFICA STAMPANTE \_ ELIMINA \_ \_ PROCESSORE \_ DI STAMPA**</dt> </dl>          | Un processore di stampa è stato eliminato dal server.<br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <dt>**MODIFICA STAMPANTE \_ \_ ELIMINA \_ STAMPANTE**</dt> </dl>                                   | È stata eliminata una stampante.<br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <dt>**MODIFICA DELLA \_ STAMPANTE ELIMINARE IL DRIVER DELLA \_ \_ \_ STAMPANTE**</dt> </dl>             | Un driver della stampante è stato eliminato dal server.<br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <dt>**PRINTER \_ CHANGE \_ FAILED \_ CONNECTION \_ PRINTER**</dt> </dl> | Una connessione alla stampante non è riuscita.<br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <dt>**MODULO \_ \_ DELL'INSIEME DI MODIFICHE DELLA \_ STAMPANTE**</dt> </dl>                                                     | È stato impostato un modulo nel server.<br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <dt>**PROCESSO \_ \_ DELL'INSIEME DI MODIFICHE \_ DELLA STAMPANTE**</dt> </dl>                                                        | È stato impostato un processo.<br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <dt>**PRINTER \_ CHANGE \_ SET \_ PRINTER**</dt> </dl>                                            | È stata impostata una stampante.<br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <dt>**DRIVER \_ DELLA STAMPANTE \_ DELL'INSIEME \_ DI MODIFICHE DELLA \_ STAMPANTE**</dt> </dl>                      | È stato impostato un driver della stampante.<br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <dt>**PROCESSO DI \_ SCRITTURA MODIFICA \_ \_ STAMPANTE**</dt> </dl>                                                  | I dati del processo sono stati scritti.<br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <dt>**TIMEOUT MODIFICA \_ \_ STAMPANTE**</dt> </dl>                                                         | Timeout del processo.<br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**SERVER DI \_ MODIFICA \_ STAMPANTE**</dt> </dl>                                                            | Windows 7: si è verificata una modifica nel server.<br/>    |



 

</dd> <dt>

*pPrinterNotifyOptions* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura PRINTER \_ NOTIFY \_ OPTIONS.**](printer-notify-options.md) Impostare il **membro Flags** di questa struttura su PRINTER NOTIFY **OPTIONS \_ \_ \_ REFRESH** per fare in modo che la funzione restituirà i dati correnti per tutti i campi di informazioni della stampante monitorati. La funzione ignora tutti gli altri membri della struttura . Questo parametro può essere **NULL**.

</dd> <dt>

*ppPrinterNotifyInfo* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile puntatore che riceve un puntatore a un buffer di sola lettura allocato dal sistema. Chiamare la [**funzione FreePrinterNotifyInfo**](freeprinternotifyinfo.md) per liberare il buffer al termine dell'operazione. Questo parametro può essere **NULL** se non sono necessarie informazioni.

Il buffer contiene una [**struttura PRINTER NOTIFY \_ \_ INFO**](printer-notify-info.md) che contiene una matrice di [**strutture PRINTER NOTIFY \_ \_ INFO \_**](printer-notify-info-data.md) DATA. Ogni elemento della matrice contiene informazioni su uno dei campi specificati nel *parametro pPrinterNotifyOptions* della [**chiamata FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) In genere, la funzione fornisce i dati solo per i campi modificati per generare la notifica più recente. Tuttavia, se la struttura a cui punta il *parametro pPrinterNotifyOptions* specifica **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH,** la funzione fornisce i dati per tutti i campi monitorati.

Se il bit **PRINTER NOTIFY INFO \_ \_ \_ DISCARDED** è impostato nel membro **Flags** della struttura PRINTER [**NOTIFY \_ \_ INFO,**](printer-notify-info.md) si è verificato un overflow o un errore e le notifiche potrebbero essere state perse. In questo caso, non verrà inviata alcuna notifica aggiuntiva fino a quando non si effettua una seconda chiamata **FindNextPrinterChangeNotification** che specifica **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona che potrebbe non essere restituita immediatamente. La velocità di ritorno di questa funzione dipende da fattori di run-time, ad esempio lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante, difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Chiamare la **funzione FindNextPrinterChangeNotification** dopo che è stata soddisfatta un'operazione di attesa su un oggetto notifica creato da [**FindFirstPrinterChangeNotification.**](findfirstprinterchangenotification.md) La **chiamata a FindNextPrinterChangeNotification** consente di ottenere informazioni sulla modifica che ha soddisfatto l'operazione di attesa e reimposta l'oggetto notifica in modo che possa essere segnalato quando si verifica la modifica successiva.

Con un'eccezione, non chiamare la **funzione FindNextPrinterChangeNotification** se l'oggetto notifica di modifica non si trova nello stato segnalato. Se una funzione di attesa restituisce il valore **WAIT \_ TIMEOUT**, l'oggetto di modifica non si trova nello stato segnalato. Chiamare la **funzione FindNextPrinterChangeNotification** solo se la funzione wait ha esito positivo senza timeout. L'eccezione si verifica quando **findNextPrinterChangeNotification** viene chiamato con il bit **PRINTER NOTIFY OPTIONS \_ \_ \_ REFRESH** impostato nel *parametro pPrinterNotifyOptions.* Si noti che anche quando questo flag è impostato, è comunque possibile impostare il flag **PRINTER \_ NOTIFY INFO \_ \_ DISCARDED** nel parametro *ppPrinterNotifyInfo.*

Per continuare a monitorare la stampante o il server di stampa per le modifiche, ripetere il ciclo di chiamata a una delle funzioni di attesa [e](/windows/desktop/Sync/wait-functions) quindi chiamare la funzione **FindNextPrinterChangeNotification** per esaminare la modifica e reimpostare l'oggetto notifica.

**FindNextPrinterChangeNotification può** combinare più modifiche allo stesso campo di informazioni della stampante in un'unica notifica. In questo caso, la funzione in genere comprime tutte le modifiche per il campo in una singola voce nella matrice di strutture [**PRINTER \_ NOTIFY INFO \_ \_ DATA**](printer-notify-info-data.md) in *ppPrinterNotifyInfo.* La singola voce restituisce solo le informazioni più aggiornate. Tuttavia, per alcuni campi di informazioni su processi e stampanti, la funzione può restituire più voci di matrice per lo stesso campo. In questo caso, l'ultima voce di matrice per il campo segnala i dati correnti e le voci precedenti contengono i dati per le fasi intermedie.

Quando l'oggetto notifica di modifica non è più necessario, chiuderlo chiamando la [**funzione FindClosePrinterChangeNotification.**](findcloseprinterchangenotification.md)

> [!Note]  
> In Windows XP con Service Pack 2 (SP2) e versioni successive, il Internet Connection Firewall (ICF) blocca le porte della stampante per impostazione predefinita, ma è possibile che sia abilitata un'eccezione per condivisione file e stampa. Se un utente esegue una connessione della stampante a un altro computer e l'eccezione non è abilitata, l'utente non riceverà le notifiche di modifica della stampante dal server. Un amministratore del computer dovrà abilitare l'eccezione.

 

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra come monitorare lo stato della stampante usando queste funzioni.


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
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
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

[**INFORMAZIONI DI \_ NOTIFICA \_ DELLA STAMPANTE**](printer-notify-info.md)
</dt> <dt>

[**DATI \_ INFORMARE \_ LA \_ STAMPANTE**](printer-notify-info-data.md)
</dt> <dt>

[**OPZIONI DI \_ NOTIFICA \_ DELLA STAMPANTE**](printer-notify-options.md)
</dt> </dl>

 

