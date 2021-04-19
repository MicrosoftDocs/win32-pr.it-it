---
description: Metodo del costruttore.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Costruttore CPersistStream. CPersistStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328936"
---
# <a name="cpersiststreamcpersiststream-constructor"></a>Costruttore CPersistStream. CPersistStream

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** dell'oggetto delegato.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore al valore restituito COM generale. Questo valore viene modificato solo se questa funzione ha esito negativo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PStream. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




