---
description: Il metodo CheckHeaderValidity convalida una struttura BITMAPINFOHEADER. Questo metodo è utile solo per i tipi RGB non compressi, non per i tipi compressi o YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Metodo CImageDisplay.CheckHeaderValidity (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c8ce12f7e383e04942184e3897d0ddc52700a1a621844719d94f54f60203ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652361"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Metodo CImageDisplay.CheckHeaderValidity

Il `CheckHeaderValidity` metodo convalida una struttura [**BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Questo metodo è utile solo per i tipi RGB non compressi, non per i tipi compressi o YUV.

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInput* 
</dt> <dd>

Puntatore a [**una struttura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) contenente la **struttura BITMAPINFOHEADER.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se **BITMAPINFOHEADER è** valido oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Questo metodo verifica che le dimensioni dell'immagine non siano negative. Il tipo di compressione è BI RGB o BI BITFIELDS, la profondità del colore e le maschere di colore sono valide, il membro biPlanes è uguale a uno e i membri \_ \_ **biSize** e **biSizeImage** sono corretti.  Verifica anche la presenza di errori comuni nelle voci della tavolozza, se presenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




