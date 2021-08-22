---
description: Identificatore dell'ultimo thread che ha chiamato il metodo IPinFlowControl::Block su questo pin. Questa variabile membro è valida solo quando il pin è bloccato.
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: Membro CDynamicOutputPin::m_dwBlockCallerThreadID (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b52bd7f718798ea9dd2cf9d227f6d22e069d2c1a59bb8591f6126c20599af9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539751"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Membro CDynamicOutputPin::m \_ dwBlockCallerThreadID

Identificatore dell'ultimo thread che ha chiamato il [**metodo IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) su questo pin. Questa variabile membro è valida solo quando il pin è bloccato.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Osservazioni

Prima di accedere a questa variabile, mantenere la [**sezione critica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




