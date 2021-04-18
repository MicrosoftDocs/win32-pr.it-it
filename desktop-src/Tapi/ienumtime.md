---
description: "L'interfaccia IEnumTime fornisce metodi di enumerazione standard COM per l'interfaccia ITTime. Il metodo ITTimeCollection:: Get \\_ EnumerationIf restituisce un puntatore a IEnumTime."
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Interfaccia IEnumTime (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328734"
---
# <a name="ienumtime-interface"></a>Interfaccia IEnumTime

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **IEnumTime** fornisce metodi di enumerazione standard com per l'interfaccia [**ITTime**](ittime.md) . Il metodo [**ITTimeCollection:: Get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) restituisce un puntatore a **IEnumTime**.

## <a name="members"></a>Membri

L'interfaccia **IEnumTime** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumTime** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumTime** dispone di questi metodi.



| Metodo                           | Descrizione                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumtime-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumtime-next.md)   | Ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.<br/>                 |
| [**Reset**](ienumtime-reset.md) | Reimposta l'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumtime-skip.md)   | Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

