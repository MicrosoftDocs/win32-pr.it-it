---
description: Il metodo getmascheres recupera le maschere dei colori per un formato VIDEOINFO specificato.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Metodo CImageDisplay. getmascherations (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333076"
---
# <a name="cimagedisplaygetbitmasks-method"></a>Metodo CImageDisplay. getmascherations

Il `GetBitMasks` metodo recupera le maschere dei colori per un formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) specificato.

## <a name="syntax"></a>Sintassi


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore alla struttura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una matrice di tre valori **DWORD** .

## <a name="remarks"></a>Commenti

Se il membro di **biCompression** è bi \_ campi, il metodo restituisce un puntatore alle maschere dei colori fornite nel membro **dwBitMasks** . Se il membro di **biCompression** è bi \_ RGB, il metodo restituisce le maschere dei colori che corrispondono alla profondità del bit. Se il metodo ha esito negativo, ad esempio se la profondità del bit è inferiore a 16, il metodo restituisce la matrice {0,0,0} .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




