---
description: L'interfaccia ITTimeCollection è un'interfaccia specifica del provider per l'oggetto BLOB della conferenza SDP (Session Descriptor Protocol).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interfaccia ITTimeCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d086dcf0df7fb4d55552c734798244209fc3e9f52a2f2462693f6aaad7110347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762295"
---
# <a name="ittimecollection-interface"></a>Interfaccia ITTimeCollection

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia ITTimeCollection** è un'interfaccia specifica del provider per l'oggetto BLOB della conferenza SDP (Session Descriptor Protocol). Questa interfaccia consente l'accesso [**alle interfacce ITTime**](ittime.md) in base all'indice e consente anche la creazione e l'eliminazione di componenti di tempo. Il [**metodo ITSdp::get \_ TimeCollection**](itsdp-get-timecollection.md) crea **l'interfaccia ITTimeCollection.**

## <a name="members"></a>Membri

**L'interfaccia ITTimeCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITTimeCollection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITTimeCollection** include questi metodi.



| Metodo                                                           | Descrizione                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Creare**](ittimecollection-create.md)                        | Crea un [**componente ITTime.**](ittime.md)<br/>                                                             |
| [**Elimina**](ittimecollection-delete.md)                        | Elimina un [**componente ITTime.**](ittime.md)<br/>                                                             |
| [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Restituisce un enumeratore per la raccolta.<br/>                                                                  |
| [**get \_ count**](ittimecollection-get-count.md)                 | Ottiene il numero di elementi nella raccolta.<br/>                                                                        |
| [**get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Restituisce [**l'interfaccia di enumerazione IEnumTime**](ienumtime.md) che enumera [**ITTime.**](ittime.md)<br/> |
| [**get \_ Item**](ittimecollection-get-item.md)                   | Dato un indice, restituisce un elemento nella raccolta.<br/>                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

