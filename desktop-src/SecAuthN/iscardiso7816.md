---
description: L'interfaccia ISCardISO7816 fornisce metodi per l'implementazione della funzionalità ISO 7816-4.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: Interfaccia ISCardISO7816 (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 09e5dc9e84a36148e240e4ba2d31f04216454994
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756443"
---
# <a name="iscardiso7816-interface"></a>Interfaccia ISCardISO7816

\[L'interfaccia **ISCardISO7816** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

L'interfaccia **ISCardISO7816** fornisce metodi per l'implementazione della funzionalità ISO 7816-4. Ad eccezione di [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md), questi metodi creano un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) incapsulato in un oggetto [**ISCardCmd**](iscardcmd.md) .

La specifica ISO 7816-4 definisce i comandi standard disponibili sulle [*Smart Card*](../secgloss/s-gly.md). La specifica definisce anche il modo in cui un comando APDU della smart card deve essere costruito e inviato alla smart card per l'esecuzione. Questa interfaccia automatizza il processo di compilazione.

Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardISO7816** . In questo caso, l'interfaccia **ISCardISO7816** viene utilizzata per compilare un comando APDU.

**Per inviare una transazione a una scheda specifica**

1.  Creare un'interfaccia **ISCardISO7816** e [**ISCardCmd**](iscardcmd.md) .

    L'interfaccia [**ISCardCmd**](iscardcmd.md) viene utilizzata per incapsulare APDU.

2.  Chiamare il metodo appropriato dell'interfaccia **ISCardISO7816** , passando i parametri obbligatori e il puntatore all'interfaccia [**ISCardCmd**](iscardcmd.md) .

    Il comando ISO 7816-4 APDU verrà compilato e incapsulato nell'interfaccia [**ISCardCmd**](iscardcmd.md) .

3.  Rilasciare le interfacce **ISCardISO7816** e [**ISCardCmd**](iscardcmd.md) .

> [!Note]  
> Nelle pagine di riferimento del metodo, se non è definita una sequenza di bit in una tabella, si supponga che la sequenza di bit sia riservata per un utilizzo futuro o proprietario di un fornitore specifico.

 

## <a name="members"></a>Membri

L'interfaccia **ISCardISO7816** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardISO7816** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardISO7816** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | Costruisce un comando che aggiunge un record alla fine di un file elementare (EF).<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | Imposta parte del contenuto di un EF sullo stato di cancellazione logica, in sequenza, a partire da un offset specificato.<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | Aggiorna in modo condizionale lo stato di sicurezza usando il risultato del calcolo dalla scheda, in base a una richiesta di verifica precedentemente rilasciata dalla scheda (ad esempio, il \_ comando ins get \_ Challenge), una chiave segreta eventualmente archiviata nella scheda e i dati di autenticazione trasmessi dal dispositivo di interfaccia.<br/> |
| [**Getchallenge**](iscardiso7816-getchallenge.md)                 | Richiede l'emissione di una richiesta di verifica da utilizzare in una procedura correlata alla sicurezza.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Recupera un singolo oggetto dati primitivo o un set di oggetti dati contenuti in un oggetto dati costruito, in base al tipo di file specificato.<br/>                                                                                                                                                          |
| [**GetResponse**](iscardiso7816-getresponse.md)                   | Trasmette dalla scheda al dispositivo di interfaccia APDUs che altrimenti non poteva essere trasmesso dai protocolli disponibili.<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | Avvia il calcolo dei dati di autenticazione tramite la scheda usando i dati di richiesta inviati dal dispositivo di interfaccia e un segreto pertinente archiviato nella scheda.<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | Consente di aprire e chiudere i canali logici.<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | Archivia un oggetto dati primitivo o uno o più oggetti dati contenuti in un oggetto dati costruito, all'interno del [*contesto corrente di Resource Manager*](../secgloss/r-gly.md).<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | Costruisce un comando che acquisisce un messaggio di risposta che fornisce tale parte del contenuto di un EF con struttura trasparente.<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | Costruisce un comando che legge il contenuto dei record specificati di un file elementare.<br/>                                                                                                                                                                                                            |
| [**SelectFile**](iscardiso7816-selectfile.md)                     | Imposta un file corrente all'interno di un canale logico.<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | Assegna un byte ID di classe standard che verrà usato in tutte le operazioni quando si costruisce un comando ISO 7816-4 APDU.<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | Avvia l'aggiornamento dei bit già presenti in un EF con i bit specificati nel comando APDU.<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | Costruisce un comando che avvia l'aggiornamento di un record specifico.<br/>                                                                                                                                                                                                                                  |
| [**Verificare**](iscardiso7816-verify.md)                             | Avvia il confronto nella scheda dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda.<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | Avvia la scrittura di valori binari in un EF.<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | Costruisce un comando che scrive un record.<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



 

 
