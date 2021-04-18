---
description: La funzione seprinter imposta i dati per una stampante specificata o imposta lo stato della stampante specificata sospendendo la stampa, riprendendo la stampa o cancellando tutti i processi di stampa.
ms.assetid: ade367c5-20d6-4da9-bb52-ce6768cf7537
title: Funzione seprinter (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinter
- SetPrinterA
- SetPrinterW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-printer-WinSpool-l1-1-0.dll
- Ext-MS-Win-printer-WinSpool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 5f2c58d97315ff108c8f12bd029849993a307025
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314977"
---
# <a name="setprinter-function"></a>Funzione seprinter

La funzione **Seprinter** imposta i dati per una stampante specificata o imposta lo stato della stampante specificata sospendendo la stampa, riprendendo la stampa o cancellando tutti i processi di stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPrinter* \[ in\]
</dt> <dd>

Handle per la stampante. Utilizzare la funzione [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)o [**AddPrinter**](addprinter.md) per recuperare un handle di stampante.

</dd> <dt>

*Livello* \[ di in\]
</dt> <dd>

Tipo di dati che la funzione archivia nel buffer a cui punta *pPrinter*. Se il parametro del *comando* non è uguale a zero, il parametro del *livello* deve essere zero.

Questo valore può essere 0, 2, 3, 4, 5, 6, 7, 8 o 9.

</dd> <dt>

*pPrinter* \[ in\]
</dt> <dd>

Puntatore a un buffer contenente i dati da impostare per la stampante o che contengono informazioni per il comando specificato dal parametro *Command* . Il tipo di dati nel buffer è determinato dal valore di *Level*.



| Level                                                                                                | Struttura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Se il parametro *Command* è **\_ \_ \_ Status set di controllo Printer**, *pPrinter* deve contenere un valore **DWORD** che specifica il nuovo stato della stampante da impostare. Per un elenco dei valori di stato possibili, vedere il membro **status** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) . Si noti che **lo stato della stampante è \_ \_ sospeso** e **\_ lo stato della stampante \_ \_ eliminazione in sospeso** non sono valori di stato validi da impostare.<br/> Se *Level* è 0, ma il parametro *Command* non è **\_ \_ impostato \_ sullo stato del controllo Printer**, *pPrinter* deve essere **null**.<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Struttura [**di \_ info \_ 2 della stampante**](printer-info-2.md) che contiene informazioni dettagliate sulla stampante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Struttura [**di \_ informazioni \_ sulla stampante 3**](printer-info-3.md) contenente le informazioni di sicurezza della stampante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Struttura [**di \_ informazioni \_ di stampa 4**](printer-info-4.md) contenente informazioni minime sulla stampante, tra cui il nome della stampante, il nome del server e l'eventuale presenza di una stampante remota o locale.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Struttura [**di \_ informazioni \_ sulla stampante 5**](printer-info-5.md) che contiene informazioni sulla stampante, ad esempio attributi della stampante e impostazioni di timeout.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Struttura della [**stampante \_ info \_ 6**](printer-info-6.md) che specifica il valore di stato di una stampante.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Struttura [**di \_ info \_ 7 della stampante**](printer-info-7.md) . Il membro *dwAction* di questa struttura **indica se il** selettore deve pubblicare, annullare la pubblicazione, pubblicare di nuovo o aggiornare i dati della stampante nel servizio directory.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Una struttura di [**\_ Info stampa \_ 8**](printer-info-8.md) che specifica le impostazioni della stampante predefinite globali.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Struttura [**Printer \_ info \_ 9**](printer-info-9.md) che specifica le impostazioni della stampante predefinite per utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*Comando* \[ in\]
</dt> <dd>

l'azione da eseguire.

Se il parametro *Level* è diverso da zero, impostare il valore di questo parametro su zero. In questo caso, la stampante mantiene lo stato corrente e la funzione riconfigura i dati della stampante come specificato dai parametri *Level* e *pPrinter* .

Se il parametro *Level* è zero, impostare il valore di questo parametro su uno dei valori seguenti.



| Valore                                                                                                                                                                                                  | Significato                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_CONTROL_PAUSE"></span><span id="printer_control_pause"></span><dl> <dt>**\_sospensione controllo \_ stampante**</dt> </dl>                 | Sospendere la stampante.<br/>                                                                                                                       |
| <span id="PRINTER_CONTROL_PURGE"></span><span id="printer_control_purge"></span><dl> <dt>**\_ripulitura controllo stampanti \_**</dt> </dl>                 | Elimina tutti i processi di stampa nella stampante.<br/>                                                                                                    |
| <span id="PRINTER_CONTROL_RESUME"></span><span id="printer_control_resume"></span><dl> <dt>**\_ripresa del controllo della stampante \_**</dt> </dl>              | Riprendere una stampante sospesa.<br/>                                                                                                                 |
| <span id="PRINTER_CONTROL_SET_STATUS"></span><span id="printer_control_set_status"></span><dl> <dt>**\_stato del \_ set di controlli della stampante \_**</dt> </dl> | Impostare lo stato della stampante.<br/> Impostare il parametro *pPrinter* su un puntatore a un valore **DWORD** che specifica il nuovo stato della stampante.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un valore diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero.

Se il *livello* è 7 e l'azione di pubblicazione non è riuscita, **viene restituito l'** errore i/o in **\_ \_ sospeso** e i tentativi di completare l'azione in background. Se il *livello* è 7 e l'azione di aggiornamento non è riuscita, il **seprinter** restituisce il **file di errore \_ \_ non \_ trovato**.

## <a name="remarks"></a>Commenti

> [!Note]  
> Si tratta di una funzione di blocco o sincrona e potrebbe non essere restituita immediatamente. La velocità di restituzione di questa funzione dipende da fattori di runtime quali lo stato della rete, la configurazione del server di stampa e i fattori di implementazione del driver della stampante difficili da prevedere durante la scrittura di un'applicazione. La chiamata di questa funzione da un thread che gestisce l'interazione con l'interfaccia utente potrebbe far sembrare che l'applicazione non risponda.

 

Non è possibile utilizzare l'utilità di **stampa** per modificare la stampante predefinita.

Per modificare le impostazioni della stampante correnti, chiamare la funzione [**GetPrinter**](getprinter.md) per recuperare le impostazioni correnti in una struttura [**Printer \_ info \_ 2**](printer-info-2.md) , modificare i membri della struttura in modo che siano necessari, quindi chiamare **seprinter**.

La funzione **Seprinter** ignora i membri **pServerName**, **AveragePPM**, **status** e **cJobs** di una struttura [**Printer \_ info \_ 2**](printer-info-2.md) .

Con la sospensione di una stampante viene sospesa la pianificazione di tutti i processi di stampa per tale stampante, ad eccezione di un processo di stampa che può essere attualmente stampato. I processi di stampa possono essere inviati a una stampante sospesa, ma non verrà pianificato alcun processo di stampa su tale stampante fino a quando la stampa non viene ripresa. Se una stampante viene deselezionata, tutti i processi di stampa per tale stampante vengono eliminati, ad eccezione del processo di stampa corrente.

Se si utilizza **Seprinter** per modificare la struttura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) predefinita per una stampante (impostando globalmente le impostazioni predefinite della stampante), è necessario chiamare prima la funzione [**DocumentProperties**](documentproperties.md) per convalidare la struttura **DEVMODE** .

Per le strutture [**Printer \_ info \_ 2**](printer-info-2.md) e [**Printer \_ info \_ 3**](printer-info-3.md) contenenti un puntatore a un descrittore di sicurezza, la funzione può impostare solo i componenti del descrittore di sicurezza che il chiamante dispone delle autorizzazioni per la modifica. Per impostare particolari componenti del descrittore di sicurezza, è necessario specificare i diritti di accesso necessari quando si chiama la funzione [**OpenPrinter**](openprinter.md) o [**OpenPrinter2**](openprinter2.md) per recuperare un handle per la stampante. La tabella seguente illustra i diritti di accesso necessari per modificare i vari componenti del descrittore di sicurezza.



| Autorizzazione di accesso            | Componente del descrittore di sicurezza             |
|------------------------------|-------------------------------------------|
| **Scrivi \_ proprietario**             | Proprietario<br/> Gruppo primario<br/> |
| **Scrivi \_ DAC**               | Elenco di controllo di accesso discrezionale (DACL)  |
| **ACCESSO \_ alla \_ sicurezza del sistema** | Elenco di controllo di accesso di sistema (SACL)         |



 

Se il descrittore di sicurezza contiene un componente per il quale il chiamante non dispone del diritto di accesso da modificare, il **Seprinter** ha esito negativo. I componenti di un descrittore di sicurezza che non si desidera modificare devono essere **null** o non essere presenti, a seconda dei casi. Se non si desidera modificare il descrittore di sicurezza e si chiama l'oggetto di **stampa** con una struttura di [**\_ info \_ 2 della stampante**](printer-info-2.md) , impostare il membro **pSecurityDescriptor** della struttura su **null**.

Per impostazione predefinita, il firewall connessione Internet (ICF) blocca le porte della stampante, ma è possibile abilitare un'eccezione per la condivisione di file e stampanti. Se il **Seprinter** viene chiamato da un amministratore del computer, l'eccezione viene abilitata. Se viene chiamato da un non amministratore e l'eccezione non è già stata abilitata, la chiamata ha esito negativo.

È possibile utilizzare il livello 7 con la struttura [**Printer \_ info \_ 7**](printer-info-7.md) per pubblicare, annullare la pubblicazione o aggiornare i dati del servizio directory per la stampante. I dati del servizio directory per una stampante includono tutti i dati archiviati con le \_ \* chiavi di SPLDS tramite chiamate alla funzione [**SetPrinterDataEx**](setprinterdataex.md) per la stampante. Prima di chiamare l'agente di **stampa**, impostare il membro **pszObjectGUID** di **Printer \_ info \_ 7** su **null** e impostare il membro *dwAction* su uno dei valori seguenti.



| Valore                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_pubblicazione DSPRINT**<br/>   | Pubblica i dati del servizio directory.<br/>                                                                                                                                                                                                                                                                                                                                        |
| **\_ripubblicazione DSPRINT**<br/> | I dati del servizio directory per la stampante non vengono pubblicati e quindi pubblicati nuovamente, aggiornando tutte le proprietà della stampante pubblicata. La ripubblicazione modifica anche il GUID della stampante pubblicata. Utilizzare questo valore se si ritiene che i dati pubblicati della stampante siano danneggiati.<br/>                                                                                         |
| **DSPRINT \_ annullare la pubblicazione**<br/> | Annulla la pubblicazione dei dati del servizio directory.<br/>                                                                                                                                                                                                                                                                                                                                      |
| **aggiornamento di DSPRINT \_**<br/>    | Aggiorna i dati del servizio directory. Questa operazione è identica a quella di **DSPRINT \_ Publish**, **con la differenza che il** file di errore non viene trovato se la stampante non è già **\_ \_ \_ stata** pubblicata.<br/> Usare **l' \_ aggiornamento di DSPRINT** per aggiornare le proprietà pubblicate ma non forzare la pubblicazione. I driver della stampante devono sempre usare l' **\_ aggiornamento DSPRINT** anziché **DSPRINT \_ Publish**.<br/> |



 

**DSPRINT \_ PENDING** non è un valore *dwAction* valido per **seprinter**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>WinSpool. h (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Nomi Unicode e ANSI<br/>   | **SetPrinterW** (Unicode) e **seprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Funzioni dell'API spooler di stampa](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Informazioni stampante \_ 3**](printer-info-3.md)
</dt> <dt>

[**\_Informazioni stampante \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_Informazioni stampante \_ 5**](printer-info-5.md)
</dt> <dt>

[**\_Informazioni stampante \_ 6**](printer-info-6.md)
</dt> <dt>

[**Informazioni sulla stampante \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**\_Informazioni stampante \_ 8**](printer-info-8.md)
</dt> <dt>

[**Informazioni sulla stampante \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




