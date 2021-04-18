---
description: L'interfaccia ISCardDatabase fornisce i metodi per l'esecuzione delle operazioni di database di gestione risorse smart card.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interfaccia ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307234"
---
# <a name="iscarddatabase-interface"></a>Interfaccia ISCardDatabase

\[L'interfaccia **ISCardDatabase** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

L'interfaccia **ISCardDatabase** fornisce i metodi per l'esecuzione delle operazioni [*di database di gestione risorse*](../secgloss/r-gly.md) [*Smart Card*](../secgloss/s-gly.md) . Queste operazioni includono l'elenco di smart card, [*lettori*](../secgloss/r-gly.md)e gruppi di lettori noti, oltre a recuperare le interfacce supportate da una smart card e dal relativo [*provider di servizi primario*](../secgloss/p-gly.md).

> [!Note]  
> L'identificatore del provider di servizi primario è un GUID COM che può essere utilizzato per creare un'istanza di e utilizzare gli oggetti COM per una scheda specifica.

 

Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardDatabase** . In questo caso, l'interfaccia **ISCardDatabase** viene utilizzata per elencare tutte le smart card note.

**Per inviare una transazione a una scheda specifica**

1.  Creare un'interfaccia **ISCardDatabase** .
2.  Chiamare [**ListCards**](iscarddatabase-listcards.md) per recuperare tutte le smart card note in base a una [*stringa ATR*](../secgloss/a-gly.md) o alle relative interfacce supportate.
3.  Rilasciare l'interfaccia **ISCardDatabase** .

## <a name="members"></a>Membri

L'interfaccia **ISCardDatabase** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardDatabase** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardDatabase** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Recupera l'identificatore del [*provider di servizi primario*](../secgloss/p-gly.md) per una smart card specifica.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Recupera gli identificatori di interfaccia (GUID) di tutte le interfacce supportate da una smart card specifica.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Recupera tutti i nomi delle smart card che corrispondono a un set specifico di identificatori di interfaccia (GUID) o una [*stringa ATR*](../secgloss/a-gly.md).<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Recupera i nomi dei [*gruppi di Reader*](../secgloss/r-gly.md) a cui il gestore di risorse è a conoscenza.<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | Recuperare i nomi dei [*lettori*](../secgloss/r-gly.md) di cui il gestore di risorse è a conoscenza.<br/>                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
