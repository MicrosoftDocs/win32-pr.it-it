---
description: L'interfaccia ITTimeCollection è un'interfaccia specifica del provider per l'oggetto BLOB della conferenza SDP (Session Descriptor Protocol).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interfaccia ITTimeCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326746"
---
# <a name="ittimecollection-interface"></a>Interfaccia ITTimeCollection

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITTimeCollection** è un'interfaccia specifica del provider per l'oggetto BLOB della conferenza SDP (Session Descriptor Protocol). Questa interfaccia consente l'accesso alle interfacce [**ITTime**](ittime.md) in base all'indice e consente inoltre la creazione e l'eliminazione di componenti temporali. Il metodo [**ITSdp:: Get \_ TimeCollection**](itsdp-get-timecollection.md) crea l'interfaccia **ITTimeCollection** .

## <a name="members"></a>Membri

L'interfaccia **ITTimeCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTimeCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITTimeCollection** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Creare**](ittimecollection-create.md)                        | Crea un componente [**ITTime**](ittime.md) .<br/>                                                             |
| [**Delete**](ittimecollection-delete.md)                        | Elimina un componente [**ITTime**](ittime.md) .<br/>                                                             |
| [**ottenere \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | Restituisce un enumeratore per la raccolta.<br/>                                                                  |
| [**Ottieni \_ conteggio**](ittimecollection-get-count.md)                 | Ottiene il numero di elementi nella raccolta.<br/>                                                                        |
| [**ottenere \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | Restituisce l'interfaccia di enumerazione [**IEnumTime**](ienumtime.md) che enumera [**ITTime**](ittime.md).<br/> |
| [**Ottieni \_ elemento**](ittimecollection-get-item.md)                   | Dato un indice, restituisce un elemento nella raccolta.<br/>                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

