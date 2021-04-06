---
description: La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un provider di servizi per smart card.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interfaccia ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882902"
---
# <a name="iscardfileaccess-interface"></a>Interfaccia ISCardFileAccess

\[L'interfaccia **ISCardFileAccess** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) .

L'interfaccia **ISCardFileAccess** può essere usata per implementare un'interfaccia di alto livello per una file System basata su schede con una scheda sottostante file System basata sulla struttura definita in ISO/IEC 7816-4. Sono possibili altre implementazioni, ma questo dovrebbe essere il più comune.

L'interfaccia **ISCardFileAccess** può essere utilizzata per esporre file System entità in modo molto familiare agli sviluppatori di applicazioni nell'ambiente del computer. Fornisce meccanismi per l'individuazione di file specifici e l'esecuzione di operazioni comuni, ad esempio la selezione, la lettura, la scrittura, la creazione e l'eliminazione. Incapsula e maschera gran parte dei dettagli di basso livello necessari per eseguire queste operazioni a livello di scheda.

Di seguito è riportato un utilizzo tipico dell'interfaccia **ISCardFileAccess** . In questo caso, l'interfaccia **ISCardFileAccess** viene utilizzata per selezionare, aprire e scrivere in un file.

**Per scrivere in un file**

1.  Chiamare [**ISCardManage:: CreateFileAccess**](iscardmanage-createfileaccess.md) per creare un'interfaccia **ISCardFileAccess** .
2.  Chiamare [**Open**](iscardfileaccess-open.md) per selezionare e aprire il file.
3.  Chiamata [**Write**](iscardfileaccess-write.md).
4.  [**Chiusura**](iscardfileaccess-close.md)della chiamata.
5.  Rilasciare l'interfaccia **ISCardFileAccess** .

## <a name="members"></a>Membri

L'interfaccia **ISCardFileAccess** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardFileAccess** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardFileAccess** dispone di questi metodi.



| Metodo                                                              | Descrizione                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeDir**](iscardfileaccess-changedir.md)                     | Imposta la directory della smart card corrente sulla nuova directory specificata.<br/>                                                          |
| [**Chiudi**](iscardfileaccess-close.md)                             | Chiude il file specificato.<br/>                                                                                                        |
| [**Creare**](iscardfileaccess-create.md)                           | Crea un file in una posizione specificata all'interno del file system ICC.<br/>                                                                    |
| [**Delete**](iscardfileaccess-delete.md)                           | Elimina un file specificato.<br/>                                                                                                         |
| [**Directory**](iscardfileaccess-directory.md)                     | Recupera un elenco di file.<br/>                                                                                                        |
| [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)             | Restituisce un percorso assoluto della directory attualmente selezionata.<br/>                                                                     |
| [**GetFileCapabilities**](iscardfileaccess-getfilecapabilities.md) | Recupera le funzionalità del file.<br/>                                                                                                      |
| [**GetProperties**](iscardfileaccess-getproperties.md)             | Recupera i dati primitivi a cui fanno riferimento i tag per l'oggetto specificato.<br/>                                                           |
| [**Invalidate**](iscardfileaccess-invalidate.md)                   | Rende il file specificato non valido.<br/>                                                                                               |
| [**Aprire**](iscardfileaccess-open.md)                               | Apre il file specificato per un ulteriore utilizzo.<br/>                                                                                         |
| [**Lettura**](iscardfileaccess-read.md)                               | Legge e restituisce i dati specificati da un file specificato.<br/>                                                                           |
| [**Riabilitare**](iscardfileaccess-rehabilitate.md)               | Rende un file (EF o DF), che in precedenza non è stato reso valido tramite il comando Invalidate, accessibile dall'applicazione.<br/> |
| [**Seek**](iscardfileaccess-seek.md)                               | Seleziona l'oggetto da cui verrà eseguita l'autorizzazione di lettura/scrittura.<br/>                                                                 |
| [**SetProperties**](iscardfileaccess-setproperties.md)             | Imposta i dati primitivi a cui fanno riferimento i tag per l'oggetto specificato.<br/>                                                                |
| [**Scrittura**](iscardfileaccess-write.md)                             | Scrive i dati in un file aperto corrente.<br/>                                                                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
