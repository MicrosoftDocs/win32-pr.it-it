---
description: Il metodo IsUsingTimeFormat determina se un formato di ora specificato è il formato attualmente in uso. Questo metodo implementa il metodo IMediaSeeking::IsUsingTimeFormat.
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Metodo CPosPassThru.IsUsingTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64c240a0b1c269dde57e07e50bcbdbbd4d5d7e03d24a4e6d263662947f3d65de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954010"
---
# <a name="cpospassthruisusingtimeformat-method"></a>Metodo CPosPassThru.IsUsingTimeFormat

Il `IsUsingTimeFormat` metodo determina se un formato di ora specificato è il formato attualmente in uso. Questo metodo implementa il [**metodo IMediaSeeking::IsUsingTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a un GUID di formato ora.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> <dt>

[**GUID di formato ora**](time-format-guids.md)
</dt> </dl>

 

 




