---
description: 'Identificatore del thread che ha chiamato per ultimo il metodo IPinFlowControl:: Block su questo pin. Questa variabile membro è valida solo quando il PIN è bloccato.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Membro CDynamicOutputPin:: m_dwBlockCallerThreadID (Amfilter. h)'
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
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333448"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Membro dwBlockCallerThreadID di CDynamicOutputPin:: m \_

Identificatore del thread che ha chiamato per ultimo il metodo [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) su questo pin. Questa variabile membro è valida solo quando il PIN è bloccato.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Osservazioni

Prima di accedere a questa variabile, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




