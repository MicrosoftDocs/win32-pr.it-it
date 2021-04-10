---
description: La funzione AddPrinter aggiunge una stampante all'elenco delle stampanti supportate per un server specificato.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Funzione AddPrinter (winspool. h)
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
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227360"
---
# <a name="addprinter-function"></a>AddPrinter (funzione)

La funzione **AddPrinter** aggiunge una stampante all'elenco delle stampanti supportate per un server specificato.

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

*pname* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del server in cui deve essere installata la stampante. Se la stringa è **null**, la stampante viene installata localmente.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Versione della struttura a cui punta *pPrinter* . Questo valore deve essere 2.

</dd> <dt>

*pPrinter* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ informazioni \_ sulla stampante 2**](printer-info-2.md) che contiene informazioni sulla stampante. È necessario specificare valori non **null** per i membri **pPrinterName**, **pPortName**, **pDriverName** e **pPrintProcessor** di questa struttura prima di chiamare **AddPrinter**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle (non thread-safe) a un nuovo oggetto Printer. Al termine dell'handle, passarlo alla funzione [**ClosePrinter**](closeprinter.md) per chiuderlo.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Non chiamare questo metodo in [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Il chiamante deve avere [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

L'handle restituito non è thread-safe. Se i chiamanti devono utilizzarlo contemporaneamente su più thread, devono fornire l'accesso di sincronizzazione personalizzato all'handle della stampante utilizzando le [funzioni di sincronizzazione](/windows/desktop/Sync/synchronization-functions). Per evitare di scrivere codice personalizzato, l'applicazione può aprire un handle della stampante in ogni thread, in base alle esigenze.

Di seguito sono riportati i membri della [**struttura \_ info \_ 2 della stampante**](printer-info-2.md) che è possibile impostare prima della chiamata della funzione **AddPrinter** :

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

I membri **status**, **cJobs** e **AveragePPM** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) sono riservati per l'uso da parte della funzione [**GetPrinter**](getprinter.md) . Non devono essere impostate prima di chiamare **AddPrinter**.

Se **pSecurityDescriptor** è **null**, il sistema assegna un descrittore di sicurezza predefinito alla stampante. Il descrittore di sicurezza predefinito dispone delle autorizzazioni seguenti.



| Valore                          | Descrizione                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amministratori e utenti esperti | Controllo completo della coda di stampa. Ciò significa che i membri di questi gruppi possono stampare, gestire la coda (può eliminare la coda, modificare qualsiasi impostazione della coda, incluso il descrittore di sicurezza) e gestire i processi di stampa di tutti gli utenti (eliminazione, sospensione, ripresa, riavvio dei processi). Si noti che gli utenti avanzati non esistono prima di Windows XP Professional.<br/> |
| Autore/proprietario                  | Consente di gestire i processi personali. Ciò significa che l'utente che invia processi può gestire (eliminare, sospendere, riprendere, riavviare) i propri processi.                                                                                                                                                                                                                                  |
| Tutti                       | Esecuzione e controllo di lettura standard. Ciò significa che i membri del gruppo Everyone possono stampare e leggere le proprietà della coda di stampa.                                                                                                                                                                                                                     |



 

Dopo che un'applicazione ha creato un oggetto Printer con la funzione **AddPrinter** , è necessario utilizzare la funzione [**PrinterProperties**](printerproperties.md) per specificare le impostazioni corrette per il driver della stampante associato all'oggetto Printer.

La funzione **AddPrinter** restituisce un errore se esiste già un oggetto Printer con lo stesso nome, a meno che l'oggetto non sia contrassegnato come eliminazione in sospeso. In tal caso, la stampante esistente non viene eliminata e i parametri per la creazione di **AddPrinter** vengono usati per modificare le impostazioni della stampante esistente (come se l'applicazione avesse usato la funzione [**seprinter**](setprinter.md) ).

Utilizzare la funzione [**EnumPrintProcessors**](enumprintprocessors.md) per enumerare il set di processori di stampa installati in un server. Utilizzare la funzione [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) per enumerare il set di tipi di dati supportati da un processore di stampa. Utilizzare la funzione [**EnumPorts**](enumports.md) per enumerare il set di porte disponibili. Utilizzare la funzione [**EnumPrinterDrivers**](enumprinterdrivers.md) per enumerare i driver della stampante installati.

Il chiamante della funzione **AddPrinter** deve avere \_ accesso al server \_ per amministrare l'accesso al server in cui deve essere creata la stampante. L'handle restituito dalla funzione avrà \_ le \_ autorizzazioni di accesso a tutte le stampanti e potrà essere utilizzato per eseguire operazioni amministrative sulla stampante.

Se la funzione **DrvPrinterEvent** viene passata al flag di evento della stampante \_ \_ \_ senza \_ flag dell'interfaccia utente, il driver non deve usare una chiamata dell'interfaccia utente durante **DrvPrinterEvent**. Per eseguire processi correlati all'interfaccia utente, il programma di installazione deve usare la voce **VendorSetup** nel file con estensione inf della stampante o, per plug and Play dispositivi, il programma di installazione può usare un programma di coinstallazione specifico del dispositivo. Per ulteriori informazioni su **VendorSetup**, vedere Microsoft Windows Driver Development Kit (DDK).

Per impostazione predefinita, il firewall connessione Internet (ICF) blocca le porte della stampante, ma viene abilitata un'eccezione per la condivisione di file e stampanti quando si esegue **AddPrinter**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

