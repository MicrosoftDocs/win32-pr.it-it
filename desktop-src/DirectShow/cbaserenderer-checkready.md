---
description: Il metodo CheckReady esegue una query per determinare se una transizione di stato è stata completata.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Metodo CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329399"
---
# <a name="cbaserenderercheckready-method"></a>CBaseRenderer. CheckReady, metodo

Il `CheckReady` metodo esegue una query per determinare se una transizione di stato è stata completata.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckReady();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la transizione di stato è completa oppure **false** se il filtro è ancora in fase di transizione a un nuovo stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer:: nobattistrada**](cbaserenderer-notready.md)
</dt> <dt>

[**CBaseRenderer:: Ready**](cbaserenderer-ready.md)
</dt> </dl>

 

 




