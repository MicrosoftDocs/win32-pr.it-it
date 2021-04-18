---
description: Flag che indica se il filtro ha inviato una notifica di fine del flusso.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Membro CTransformFilter:: m_bEOSDelivered (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331146"
---
# <a name="ctransformfilterm_beosdelivered-member"></a>Membro bEOSDelivered di CTransformFilter:: m \_

Flag che indica se il filtro ha inviato una notifica di fine del flusso.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a>Osservazioni

Se il filtro si interrompe quando non dispone di una connessione di input, invia una notifica di fine flusso a valle e imposta il flag su **true**. La notifica di fine flusso garantisce che il filtro downstream non attenda gli esempi. Si noti che il metodo [**EndOfStream**](ctransformfilter-endofstream.md) del filtro non imposta questo flag.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




