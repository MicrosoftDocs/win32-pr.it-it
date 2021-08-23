---
description: La funzione AddPrinter aggiunge una stampante all'elenco di stampanti supportate per un server specificato.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Funzione AddPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6034c330da19f5982e9bbacbf75cc16f0a7d10dd65f9c8bded2efa5cbda70835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601141"
---
# <a name="addprinter-function"></a>Funzione AddPrinter

La **funzione AddPrinter** aggiunge una stampante all'elenco di stampanti supportate per un server specificato.

## <a name="syntax"></a>Sintassi


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del server in cui deve essere installata la stampante. Se questa stringa è **NULL,** la stampante viene installata in locale.

</dd> <dt>

*Livello* \[ Pollici\]
</dt> <dd>

Versione della struttura a cui *punta pPrinter.* Questo valore deve essere 2.

</dd> <dt>

*pPrinter* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura PRINTER \_ INFO \_ 2**](printer-info-2.md) che contiene informazioni sulla stampante. È necessario specificare valori non **NULL** per i membri **pPrinterName**, **pPortName**, **pDriverName** e **pPrintProcessor** di questa struttura prima di **chiamare AddPrinter**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle (non thread-safe) per un nuovo oggetto stampante. Al termine dell'operazione, passarlo alla [**funzione ClosePrinter**](closeprinter.md) per chiuderlo.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non restituire immediatamente . La velocità di ritorno di questa funzione dipende da fattori in fase di esecuzione, ad esempio lo stato di rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non rispetti.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

L'handle restituito non è thread-safe. Se i chiamanti devono usarlo contemporaneamente su più thread, devono fornire l'accesso di sincronizzazione personalizzato all'handle della stampante usando le funzioni [di sincronizzazione](/windows/desktop/Sync/synchronization-functions). Per evitare di scrivere codice personalizzato, l'applicazione può aprire un handle della stampante in ogni thread, in base alle esigenze.

Di seguito sono riportati i membri della struttura [**PRINTER \_ INFO \_ 2**](printer-info-2.md) che possono essere impostati prima della chiamata della funzione **AddPrinter:**

-   **Attributes (Attributi)**
-   **pPrintProcessor**
-   **DefaultPriority**
-   **Priorità**
-   **pComment**
-   **pSecurityDescriptor**
-   **pDatatype**
-   **pSepFile**
-   **pDevMode**
-   **pShareName**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

I **membri Status**, **cJobs** e **AveragePPM** della struttura [**PRINTER INFO \_ \_ 2**](printer-info-2.md) sono riservati per l'uso da parte [**della funzione GetPrinter.**](getprinter.md) Non devono essere impostate prima di **chiamare AddPrinter**.

Se **pSecurityDescriptor** è **NULL,** il sistema assegna un descrittore di sicurezza predefinito alla stampante. Il descrittore di sicurezza predefinito dispone delle autorizzazioni seguenti.



| Valore                          | Descrizione                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amministratori e utenti esperti | Controllo completo sulla coda di stampa. Ciò significa che i membri di questi gruppi possono stampare, gestire la coda (può eliminare la coda, modificare qualsiasi impostazione della coda, incluso il descrittore di sicurezza) e gestire i processi di stampa di tutti gli utenti (eliminazione, sospensione, ripresa, riavvio dei processi). Si noti che Power Users non esiste prima di Windows XP Professional.<br/> |
| Autore/proprietario                  | Può gestire processi personalizzati. Ciò significa che l'utente che invia processi può gestire (eliminare, sospendere, riprendere, riavviare) i propri processi.                                                                                                                                                                                                                                  |
| Tutti                       | Controllo di esecuzione e lettura standard. Ciò significa che i membri del gruppo everyone possono stampare e leggere le proprietà della coda di stampa.                                                                                                                                                                                                                     |



 

Dopo che un'applicazione ha creato un oggetto stampante con la funzione **AddPrinter,** deve usare la funzione [**PrinterProperties**](printerproperties.md) per specificare le impostazioni corrette per il driver della stampante associato all'oggetto stampante.

La **funzione AddPrinter** restituisce un errore se esiste già un oggetto stampante con lo stesso nome, a meno che tale oggetto non sia contrassegnato come eliminazione in sospeso. In tal caso, la stampante esistente non viene eliminata e i parametri di creazione **AddPrinter** vengono usati per modificare le impostazioni della stampante esistenti (come se l'applicazione avesse usato la [**funzione SetPrinter).**](setprinter.md)

Usare la [**funzione EnumPrintProcessors**](enumprintprocessors.md) per enumerare il set di processori di stampa installati in un server. Usare la [**funzione EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) per enumerare il set di tipi di dati supportati da un processore di stampa. Usare la [**funzione EnumPorts**](enumports.md) per enumerare il set di porte disponibili. Usare la [**funzione EnumPrinterDrivers**](enumprinterdrivers.md) per enumerare i driver della stampante installati.

Il chiamante della **funzione AddPrinter** deve disporre dell'accesso SERVER ACCESS ADMINISTER al server in cui deve \_ essere creata la \_ stampante. L'handle restituito dalla funzione avrà l'autorizzazione PRINTER ALL ACCESS e può essere usato per eseguire \_ \_ operazioni amministrative sulla stampante.

Se alla **funzione DrvPrinterEvent** viene passato il flag DELL'interfaccia utente PRINTER EVENT FLAG NO, il driver non deve usare una chiamata dell'interfaccia utente durante \_ \_ \_ \_ **DrvPrinterEvent**. Per eseguire processi correlati all'interfaccia utente, il programma di installazione deve usare la voce **VendorSetup** nel file inf della stampante o, per i dispositivi Plug and Play, il programma di installazione può usare un co-programma di installazione specifico del dispositivo. Per altre informazioni su **VendorSetup,** vedere Microsoft Windows Driver Development Kit (DDK).

Il Internet Connection Firewall (ICF) blocca le porte della stampante per impostazione predefinita, ma un'eccezione per Condivisione file e stampa è abilitata quando si esegue **AddPrinter**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **AddPrinterW** (Unicode) e **AddPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMAZIONI \_ STAMPANTE \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

