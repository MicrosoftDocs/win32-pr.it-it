---
description: L'interfaccia ISCardDatabase fornisce i metodi per l'smart card delle operazioni di database di Resource Manager.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interfaccia ISCardDatabase (Scardmgr.h)
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
ms.openlocfilehash: a5bdad1db29630dcf029aab4fbc3812cfc83e0c69dab33c31edb73e21b297b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577171"
---
# <a name="iscarddatabase-interface"></a>Interfaccia ISCardDatabase

\[**L'interfaccia ISCardDatabase** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

**L'interfaccia ISCardDatabase** fornisce i metodi per l'smart card delle operazioni di database di Resource [](../secgloss/s-gly.md) [*Manager.*](../secgloss/r-gly.md) Queste operazioni includono l'elenco di smart card [*note,*](../secgloss/r-gly.md)lettori e gruppi di lettori, nonché il recupero delle interfacce supportate da un smart card e dal relativo provider di [*servizi primario.*](../secgloss/p-gly.md)

> [!Note]  
> L'identificatore del provider di servizi primario è un GUID COM che può essere usato per creare un'istanza e usare gli oggetti COM per una scheda specifica.

 

L'esempio seguente illustra un uso tipico **dell'interfaccia ISCardDatabase.** In questo caso, **l'interfaccia ISCardDatabase** viene usata per elencare tutte le smart card note.

**Per inviare una transazione a una scheda specifica**

1.  Creare **un'interfaccia ISCardDatabase.**
2.  Chiamare [**ListCards**](iscarddatabase-listcards.md) per recuperare tutte le smart card note in base a una stringa [*ATR*](../secgloss/a-gly.md) o alle relative interfacce supportate.
3.  Rilasciare **l'interfaccia ISCardDatabase.**

## <a name="members"></a>Membri

**L'interfaccia ISCardDatabase** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardDatabase** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISCardDatabase** include questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Recupera l'identificatore del [*provider di servizi primario*](../secgloss/p-gly.md) per una specifica smart card.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Recupera gli identificatori di interfaccia (GUID) di tutte le interfacce supportate da una specifica smart card.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Recupera tutti i nomi smart card che corrispondono a un set specifico di identificatori di interfaccia (GUID) o a una stringa [*ATR.*](../secgloss/a-gly.md)<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Recupera i nomi dei gruppi [*di lettori di*](../secgloss/r-gly.md) cui il gestore di risorse è a conoscenza.<br/>                        |
| [**ListReader**](iscarddatabase-listreaders.md)               | Recuperare i nomi dei lettori [*di*](../secgloss/r-gly.md) cui il gestore di risorse dispone delle informazioni.<br/>                                          |



 

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
| IID<br/>                      | IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
