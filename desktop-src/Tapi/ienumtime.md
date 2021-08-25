---
description: L'interfaccia IEnumTime fornisce metodi di enumerazione standard COM per l'interfaccia ITTime. Il metodo ITTimeCollection::get \_ EnumerationIf restituisce un puntatore a IEnumTime.
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaccia IEnumTime (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c79d780374bcf121dcb5010aef51725f9836e511bed4b86c855970bb47b838e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992201"
---
# <a name="ienumtime-interface"></a>Interfaccia IEnumTime

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia IEnumTime** fornisce metodi di enumerazione standard COM per [**l'interfaccia ITTime.**](ittime.md) Il [**metodo ITTimeCollection::get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) restituisce un puntatore a **IEnumTime.**

## <a name="members"></a>Membri

**L'interfaccia IEnumTime** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumTime** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IEnumTime** include questi metodi.



| Metodo                           | Descrizione                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumtime-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumtime-next.md)   | Ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.<br/>                 |
| [**Reset**](ienumtime-reset.md) | Reimposta all'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumtime-skip.md)   | Ignora il successivo numero specificato di elementi nella sequenza di enumerazione.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

