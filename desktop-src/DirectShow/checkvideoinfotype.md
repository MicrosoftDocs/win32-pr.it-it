---
description: La funzione CheckVideoInfoType controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER per verificare la presenza di alcuni errori comuni che possono causare sovraccarichi del buffer o overflow di interi.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Funzione CheckVideoInfoType (Checkbmi.h)
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
ms.openlocfilehash: 4463a1edb2002f64e983a38eb4a0ace5b5289b4d47ac43c8ea27bf165138ff95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539541"
---
# <a name="checkvideoinfotype-function"></a>Funzione CheckVideoInfoType

La funzione controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER per verificare la presenza di alcuni errori comuni che possono causare sovraccarichi del buffer o `CheckVideoInfoType` overflow di [](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) interi.

> [!Note]  
> Questa funzione non garantisce che il tipo di supporto sia valido o che il codice che usa la struttura sia sicuro.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore alla [**struttura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convalidare

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                                | Descrizione                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                  | Valore del puntatore **NULL.**<br/> |
| <dl> <dt>**TIPO E VFW \_ \_ NON \_ \_ ACCETTATO**</dt> </dl> | Tipo di supporto non valido.<br/>     |



 

## <a name="remarks"></a>Commenti

Questa funzione chiama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) per convalidare la [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel tipo di supporto. Se il tipo di formato non è FORMAT \_ VideoInfo, la funzione restituisce VFW \_ E TYPE NOT \_ \_ \_ ACCEPTED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




