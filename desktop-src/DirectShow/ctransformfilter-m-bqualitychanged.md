---
description: Flag che indica se la qualità è stata modificata.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Membro CTransformFilter:: m_bQualityChanged (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331145"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Membro bQualityChanged di CTransformFilter:: m \_

Flag che indica se la qualità è stata modificata. La prima volta che il filtro elimina un campione, invia un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) al gestore del grafico del filtro e imposta questo flag su **true**. Questo evento non viene inviato di nuovo fino a quando il filtro non viene arrestato e riavviato, anche se nel frattempo continua a eliminare i campioni.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




