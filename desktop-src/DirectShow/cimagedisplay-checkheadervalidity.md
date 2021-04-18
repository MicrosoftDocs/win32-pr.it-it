---
description: Il metodo CheckHeaderValidity convalida una struttura BITMAPINFOHEADER. Questo metodo è utile solo per i tipi RGB non compressi, non per i tipi compressi o i tipi YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Metodo CImageDisplay. CheckHeaderValidity (Winutil. h)
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
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325324"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>CImageDisplay. CheckHeaderValidity, metodo

Il `CheckHeaderValidity` metodo convalida una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Questo metodo è utile solo per i tipi RGB non compressi, non per i tipi compressi o i tipi YUV.

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

Puntatore a una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) contenente la struttura **BITMAPINFOHEADER** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se **BITMAPINFOHEADER** è valido o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo metodo verifica che le dimensioni dell'immagine siano non negative; il tipo di compressione è BI \_ RGB o \_ bi campi; le maschere di colore e profondità sono valide; il membro **Biplanes** è uguale a uno e i membri **bidimensionali** e **biSizeImage** sono corretti. Verifica anche la presenza di errori comuni nelle voci della tavolozza, se presenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




