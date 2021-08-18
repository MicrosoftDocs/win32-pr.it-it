---
description: L'interfaccia ISCardLocate fornisce servizi per l'individuazione di smart card in base al nome.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interfaccia ISCardLocate (Scardmgr.h)
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
ms.openlocfilehash: 70679a2decc62011df70e68c119365bb8a98f7bdb06af6d7989eac18e7c14fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922930"
---
# <a name="iscardlocate-interface"></a>Interfaccia ISCardLocate

\[**L'interfaccia ISCardLocate** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

**L'interfaccia ISCardLocate** fornisce servizi per l'individuazione di smart card [*in*](../secgloss/s-gly.md) base al nome.

Questa interfaccia può visualizzare la [*smart card'interfaccia utente,*](../secgloss/u-gly.md) se necessario.

Lo scenario seguente illustra un uso tipico **dell'interfaccia ISCardLocate.** **L'interfaccia ISCardLocate** viene usata per creare [*un'unità*](../secgloss/a-gly.md) dati del protocollo applicativo (APDU).

**Per individuare una scheda specifica usando il nome**

1.  Creare **un'interfaccia ISCardLocate.**
2.  Chiamare [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) per cercare un smart card nome.
3.  Chiamare [**FindCard**](iscardlocate-findcard.md) per cercare il smart card.
4.  Interpretare i risultati.
5.  Rilasciare **l'interfaccia ISCardLocate.**

## <a name="members"></a>Membri

**L'interfaccia ISCardLocate** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardLocate** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISCardLocate** include questi metodi.



| Metodo                                                                  | Descrizione                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Riservato per utilizzi futuri.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Specifica il nome della scheda da usare nella ricerca.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Cerca il smart card e apre una connessione valida.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate è definito come 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
