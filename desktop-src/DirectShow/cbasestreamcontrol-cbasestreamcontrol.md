---
description: Metodo del costruttore.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Costruttore CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d325a48476fe2a80b7424850eb71a9d667cb60e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326566"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>Costruttore CBaseStreamControl. CBaseStreamControl

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PHR* 
</dt> <dd>

Puntatore a un valore **HRESULT** . Se il costruttore ha esito negativo, questo parametro riceve un codice di errore. In tal caso, lo stato dell'oggetto non è valido.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




