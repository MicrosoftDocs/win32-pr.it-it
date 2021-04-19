---
description: "L'interfaccia IEnumMedia fornisce metodi di enumerazione standard COM per l'interfaccia ITMedia. Il metodo ITMediaCollection:: Get \\_ EnumerationIf restituisce un puntatore a IEnumMedia."
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Interfaccia IEnumMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333145"
---
# <a name="ienummedia-interface"></a>Interfaccia IEnumMedia

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **IEnumMedia** fornisce metodi di enumerazione standard com per l'interfaccia [**ITmedia**](itmedia.md) . Il metodo [**ITMediaCollection:: Get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) restituisce un puntatore a **IEnumMedia**.

## <a name="members"></a>Membri

L'interfaccia **IEnumMedia** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumMedia** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumMedia** dispone di questi metodi.



| Metodo                            | Descrizione                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienummedia-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienummedia-next.md)   | Ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.<br/>                 |
| [**Reset**](ienummedia-reset.md) | Reimposta l'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienummedia-skip.md)   | Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

