---
description: La funzione FindFirstPrinterChangeNotification crea un oggetto notifica di modifica e restituisce un handle per l'oggetto. È quindi possibile usare questo handle in una chiamata a una delle funzioni wait per monitorare le modifiche apportate alla stampante o al server di stampa.
ms.assetid: 4155ef5c-cd96-4960-919b-d9a495bb73a5
title: Funzione FindFirstPrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindFirstPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2da6a2ae73aa5b987ea3b8f8789f81ed0b4cdf06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227471"
---
# <a name="findfirstprinterchangenotification-function"></a>FindFirstPrinterChangeNotification (funzione)

La funzione **FindFirstPrinterChangeNotification** crea un oggetto notifica di modifica e restituisce un handle per l'oggetto. È quindi possibile usare questo handle in una chiamata a una delle funzioni wait per monitorare le modifiche apportate alla stampante o al server di stampa.

La chiamata **FindFirstPrinterChangeNotification** specifica il tipo di modifiche da monitorare. È possibile specificare un set di condizioni per il monitoraggio delle modifiche, un set di campi di informazioni sulla stampante da monitorare o entrambi.

Un'operazione di attesa sull'handle della notifica di modifica ha esito positivo quando si verifica una delle modifiche specificate nella stampante o nel server di stampa specificato. Si chiama quindi la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) per recuperare le informazioni sulla modifica e per reimpostare l'oggetto notifica di modifica per l'uso nell'operazione di attesa successiva.

## <a name="syntax"></a>Sintassi


```C++
HANDLE FindFirstPrinterChangeNotification(
  _In_     HANDLE hPrinter,
           DWORD  fdwFilter,
           DWORD  fdwOptions,
  _In_opt_ LPVOID pPrinterNotifyOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante o il server di stampa che si desidera monitorare. Utilizzare la funzione [**OpenPrinter**](openprinter.md) o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*fdwFilter* 
</dt> <dd>

Condizioni che comporteranno l'immissione dello stato segnalato per l'oggetto notifica di modifica. Una notifica di modifica si verifica quando vengono soddisfatte una o più condizioni specificate. Il parametro *fdwFilter* può essere zero se *pPrinterNotifyOptions* è diverso da **null**.

Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CHANGE_FORM"></span><span id="printer_change_form"></span><dl> <dt>**\_modulo di modifica della stampante \_**</dt> </dl>                                   | Notifica delle modifiche apportate a un modulo. È possibile impostare questo flag generale oppure uno o più dei flag specifici seguenti:<br/> <dl> <dd>\_modulo di \_ aggiunta della modifica della stampante \_</dd> <dd>\_modulo del \_ set di modifiche della stampante \_</dd> <dd>\_modulo di \_ eliminazione della modifica della stampante \_</dd> </dl>                                                                              |
| <span id="PRINTER_CHANGE_JOB"></span><span id="printer_change_job"></span><dl> <dt>**\_processo di modifica della stampante \_**</dt> </dl>                                      | Notifica delle modifiche apportate a un processo. È possibile impostare questo flag generale oppure uno o più dei flag specifici seguenti:<br/> <dl> <dd>modifica della stampante \_ \_ Aggiungi \_ processo</dd> <dd>\_processo del \_ set di modifiche della stampante \_</dd> <dd>\_processo di \_ eliminazione della modifica della stampante \_</dd> <dd>\_processo di \_ scrittura \_ modifica stampante</dd> </dl>                                  |
| <span id="PRINTER_CHANGE_PORT"></span><span id="printer_change_port"></span><dl> <dt>**\_porta di modifica della stampante \_**</dt> </dl>                                   | Notificare eventuali modifiche a una porta. È possibile impostare questo flag generale oppure uno o più dei flag specifici seguenti:<br/> <dl> <dd>modifica della stampante \_ \_ Aggiungi \_ porta</dd> <dd>modifica della stampante \_ \_ configurare la \_ porta </dd> <dd>\_porta di \_ eliminazione delle modifiche della stampante \_</dd> </dl>                                                                       |
| <span id="PRINTER_CHANGE_PRINT_PROCESSOR"></span><span id="printer_change_print_processor"></span><dl> <dt>**\_processore di \_ stampa \_ modifica stampante**</dt> </dl> | Notifica delle modifiche apportate a un processore di stampa. È possibile impostare questo flag generale oppure uno o più dei flag specifici seguenti: <br/> <dl> <dd>\_modifica stampante \_ Aggiungi \_ processore di stampa \_ </dd> <dd>\_modifica stampante \_ Elimina \_ processore di stampa \_</dd> </dl>                                                                                        |
| <span id="PRINTER_CHANGE_PRINTER"></span><span id="printer_change_printer"></span><dl> <dt>**\_stampante modifica \_ stampante**</dt> </dl>                          | Notifica delle modifiche apportate a una stampante. È possibile impostare questo flag generale oppure uno o più dei flag specifici seguenti:<br/> <dl> <dd>\_modifica stampante \_ Aggiungi \_ stampante</dd> <dd>\_ \_ stampante set di modifiche stampante \_</dd> <dd>\_modifica stampante \_ Elimina \_ stampante</dd> <dd>\_modifica stampante \_ non \_ riuscita \_ stampante di connessione</dd> </dl> |
| <span id="PRINTER_CHANGE_PRINTER_DRIVER"></span><span id="printer_change_printer_driver"></span><dl> <dt>**\_ \_ driver della stampante per la modifica della stampante \_**</dt> </dl>    | Notifica delle modifiche apportate a un driver della stampante. È possibile impostare questo flag generale oppure uno o più dei flag specifici seguenti:<br/> <dl> <dd>\_modifica stampante \_ Aggiungi \_ driver della stampante \_</dd> <dd>\_ \_ \_ driver della stampante del set di modifiche della stampante \_</dd> <dd>modifica stampante- \_ \_ Elimina \_ driver della stampante \_</dd> </dl>                                   |
| <span id="PRINTER_CHANGE_ALL"></span><span id="printer_change_all"></span><dl> <dt>**\_modifica \_ tutte le stampanti**</dt> </dl>                                      | Notificare se si verifica una delle modifiche precedenti.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <dt>**\_server di modifica della stampante \_**</dt> </dl>                             | Windows 7: notifica di eventuali modifiche al server.<br/> Questo flag non è incluso nelle modifiche monitorate impostando il valore di **\_ modifica di \_ tutte le stampanti** .<br/>                                                                                                                                                                                                      |



 

Per le descrizioni dei flag più specifici nella tabella precedente, vedere la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .

</dd> <dt>

*fdwOptions* 
</dt> <dd>

Flag che determina la categoria di stampanti per le quali funzioneranno le notifiche.



| Valore                                                                                                                                                                                                                                                               | Significato                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_NOTIFY_CATEGORY_ALL"></span><span id="printer_notify_category_all"></span><dl> <dt>**Stampante \_ NOTIFICA \_ categoria \_ tutti**</dt> <dt>0x001000</dt> </dl> | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) restituisce le notifiche per le stampanti 2D e 3D.<br/> |
| <span id="PRINTER_NOTIFY_CATEGORY_3D"></span><span id="printer_notify_category_3d"></span><dl> <dt>**Stampante \_ NOTIFICA \_ alla \_ categoria**</dt> <dt>0x002000</dt> 3D </dl>    | [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) restituisce le notifiche solo per le stampanti 3D.<br/>        |



 

Quando questo flag è impostato su zero (0), **FindFirstPrinterChangeNotification** funzionerà solo per le stampanti 2D. Si tratta del valore predefinito.

</dd> <dt>

*pPrinterNotifyOptions* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ Opzioni di notifica della stampante**](printer-notify-options.md) . Il membro **pTypes** di questa struttura è una matrice di uno o più [**\_ \_ \_ tipi di opzioni di notifica della stampante**](printer-notify-options-type.md) , ognuno dei quali specifica un campo di informazioni sulla stampante da monitorare. Una notifica di modifica si verifica quando uno o più dei campi specificati vengono modificati. Quando si verifica una modifica, la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) può recuperare le informazioni sulla nuova stampante. Questo parametro può essere **null** se *fdwFilter* è diverso da zero.

Per un elenco dei campi che è possibile monitorare, vedere [**\_ Opzioni di notifica stampanti \_ \_ tipo**](printer-notify-options-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per un oggetto notifica di modifica associato alla stampante o al server di stampa specificato.

Se la funzione ha esito negativo, il valore restituito è un valore di handle non valido \_ \_ .

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Per monitorare una stampante o un server di stampa, chiamare la funzione **FindFirstPrinterChangeNotification** , quindi utilizzare l'handle dell'oggetto notifica di modifica restituito in una chiamata a una delle [funzioni di attesa](/windows/desktop/Sync/wait-functions). Un'operazione di attesa su un oggetto notifica di modifica viene soddisfatta quando l'oggetto notifica di modifica entra nello stato segnalato. Il sistema segnala l'oggetto quando una o più delle modifiche specificate da *fdwFilter* o *pPrinterNotifyOptions* si verificano nella stampante o nel server di stampa monitorato.

Quando si chiama **FindFirstPrinterChangeNotification**, *fdwFilter* deve essere diverso da zero o *PPrinterNotifyOptions* deve essere diverso da **null**. Se vengono specificati entrambi, le notifiche si verificheranno per entrambe.

Quando un'operazione di attesa su un oggetto notifica di modifica della stampante viene soddisfatta, chiamare la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) per determinare la relativa origine. Per una condizione specificata da *fdwFilter*, **FindNextPrinterChangeNotification** segnala la condizione o le condizioni modificate. Per un campo di informazioni sulla stampante specificato da *pPrinterNotifyOptions*, **FindNextPrinterChangeNotification** segnala il campo o i campi che sono stati modificati e le nuove informazioni per questi campi. **FindNextPrinterChangeNotification** Reimposta inoltre l'oggetto notifica di modifica sullo stato non segnalato, in modo che sia possibile utilizzarlo in un'altra operazione di attesa per continuare a monitorare la stampante o il server di stampa.

Con un'eccezione, non chiamare la funzione [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) se l'oggetto notifica di modifica non è nello stato segnalato. Se la funzione wait restituisce il timeout di attesa del valore \_ , l'oggetto Change non è nello stato segnalato. Chiamare la funzione **FindNextPrinterChangeNotification** solo se la funzione wait riesce senza scadere. L'eccezione si verifica quando viene chiamato **FindNextPrinterChangeNotification** con il \_ bit di aggiornamento delle opzioni di notifica della stampante \_ \_ impostato nel parametro *pPrinterNotifyOptions* .

Quando l'oggetto notifica di modifica non è più necessario, chiuderlo chiamando la funzione [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .

I chiamanti di **FindFirstPrinterChangeNotification** devono verificare che l'handle della stampante passato a **FindFirstPrinterChangeNotification** rimanga valido fino a quando non viene chiamato [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) . Se l'handle della stampante viene chiuso prima dell'handle di notifica della modifica della stampante, le notifiche successive non verranno recapitate.

**FindFirstPrinterChangeNotification** non invierà le notifiche di modifica per le stampanti 3D agli handle del server.

> [!Note]  
> In Windows XP con Service Pack 2 (SP2) e versioni successive, il firewall connessione Internet (ICF) blocca le porte della stampante per impostazione predefinita, ma è possibile abilitare un'eccezione per la condivisione di file e stampanti. Se un utente esegue una connessione alla stampante a un altro computer e l'eccezione non è abilitata, l'utente non riceverà le notifiche di modifica della stampante dal server. Un amministratore del computer dovrà abilitare l'eccezione.

 

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Opzioni di notifica stampanti \_**](printer-notify-options.md)
</dt> <dt>

[**\_tipo di \_ Opzioni di notifica stampanti \_**](printer-notify-options-type.md)
</dt> </dl>

 

