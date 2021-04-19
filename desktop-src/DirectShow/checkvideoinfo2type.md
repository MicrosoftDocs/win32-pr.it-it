---
description: La funzione CheckVideoInfo2Type controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER2 per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Funzione CheckVideoInfo2Type (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329778"
---
# <a name="checkvideoinfo2type-function"></a>CheckVideoInfo2Type (funzione)

La `CheckVideoInfo2Type` funzione controlla un tipo di supporto che contiene una struttura di formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.

> [!Note]  
> Questa funzione non garantisce che il tipo di supporto sia valido o che il codice che utilizza la struttura sia protetto.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convalidare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                                | Descrizione                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Operazione riuscita<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Valore del puntatore **null**<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | Tipo di supporto non valido<br/>     |



 

## <a name="remarks"></a>Commenti

Questa funzione chiama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) per convalidare la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel tipo di supporto. Se il tipo di formato non è **Format \_ VideoInfo2**, la funzione restituisce il **\_ tipo VFW E non è \_ \_ \_ accettato**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




