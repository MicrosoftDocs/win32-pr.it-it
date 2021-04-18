---
description: L'interfaccia ISCardLocate fornisce servizi per l'individuazione di una smart card in base al nome.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interfaccia ISCardLocate (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313734"
---
# <a name="iscardlocate-interface"></a>Interfaccia ISCardLocate

\[L'interfaccia **ISCardLocate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

L'interfaccia **ISCardLocate** fornisce servizi per l'individuazione di una [*Smart Card*](../secgloss/s-gly.md) in base al nome.

Questa interfaccia può visualizzare l' [*interfaccia utente*](../secgloss/u-gly.md) della smart card, se necessaria.

Nello scenario seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardLocate** . L'interfaccia **ISCardLocate** viene utilizzata per compilare un' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).

**Per individuare una scheda specifica usando il nome**

1.  Creare un'interfaccia **ISCardLocate** .
2.  Chiamare [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) per cercare il nome di una smart card.
3.  Chiamare [**FindCard**](iscardlocate-findcard.md) per cercare la smart card.
4.  Interpretare i risultati.
5.  Rilasciare l'interfaccia **ISCardLocate** .

## <a name="members"></a>Membri

L'interfaccia **ISCardLocate** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardLocate** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardLocate** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Riservato per utilizzi futuri.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Specifica il nome della scheda da utilizzare nella ricerca.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Cerca la smart card e apre una connessione valida.<br/> |



 

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
| IID<br/>                      | IID \_ ISCardLocate è definito come 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
