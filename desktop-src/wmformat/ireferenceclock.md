---
title: Interfaccia IReferenceClock
description: L'interfaccia IReferenceClock fornisce l'accesso a un clock esterno. Questa interfaccia viene fornita per consentire la sincronizzazione di tutte le routine di rendering con lo stesso clock. Questa interfaccia può essere ottenuta da un oggetto Reader.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Formato Windows Media Interface IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299828"
---
# <a name="ireferenceclock-interface"></a>Interfaccia IReferenceClock

L'interfaccia **IReferenceClock** fornisce l'accesso a un clock esterno. Questa interfaccia viene fornita per consentire la sincronizzazione di tutte le routine di rendering con lo stesso clock.

Questa interfaccia può essere ottenuta da un oggetto Reader.

## <a name="members"></a>Membri

L'interfaccia **IReferenceClock** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReferenceClock** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IReferenceClock** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**AdvisePeriodic**](ireferenceclock-adviseperiodic.md) | Non implementato da questo SDK.<br/>                                   |
| [**AdviseTime**](ireferenceclock-advisetime.md)         | Richiede una notifica asincrona che è trascorso un periodo di tempo.<br/> |
| [**GetTime**](ireferenceclock-gettime.md)               | Recupera l'ora di riferimento corrente.<br/>                          |
| [**Unadvise**](ireferenceclock-unadvise.md)             | Annulla una richiesta di notifica.<br/>                                |



 

## <a name="remarks"></a>Commenti

Per informazioni su altre interfacce che possono essere ottenute usando il metodo QueryInterface di questa interfaccia, vedere oggetto Reader.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](interfaces.md)
</dt> </dl>

 

