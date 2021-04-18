---
description: La funzione CheckVideoInfoType controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Funzione CheckVideoInfoType (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329777"
---
# <a name="checkvideoinfotype-function"></a>CheckVideoInfoType (funzione)

La `CheckVideoInfoType` funzione controlla un tipo di supporto che contiene una struttura di formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.

> [!Note]  
> Questa funzione non garantisce che il tipo di supporto sia valido o che il codice che utilizza la struttura sia protetto.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convalidare

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** .



| Codice restituito                                                                                                | Descrizione                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Valore del puntatore **null** .<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt> </dl> | Tipo di supporto non valido.<br/>     |



 

## <a name="remarks"></a>Commenti

Questa funzione chiama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) per convalidare la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel tipo di supporto. Se il tipo di formato non è FORMAT \_ videoinfo, la funzione restituisce il \_ tipo VFW E non è \_ \_ \_ accettato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




