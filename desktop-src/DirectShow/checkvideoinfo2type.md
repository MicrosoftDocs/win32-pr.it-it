---
description: La funzione CheckVideoInfo2Type controlla un tipo di supporto che contiene una struttura di formato VIDEOINFOHEADER2 per verificare la presenza di alcuni errori comuni che possono causare sovraccarichi del buffer o overflow di interi.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Funzione CheckVideoInfo2Type (Checkbmi.h)
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
ms.openlocfilehash: 48d9deab4d87868cbc9e5418ccd6b7e2c7e9ecf93350ad70cb6c934d365e4655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074185"
---
# <a name="checkvideoinfo2type-function"></a>Funzione CheckVideoInfo2Type

La funzione controlla un tipo di supporto che contiene una struttura di `CheckVideoInfo2Type` [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) per verificare la presenza di alcuni errori comuni che possono causare sovraccarichi del buffer o overflow di interi.

> [!Note]  
> Questa funzione non garantisce che il tipo di supporto sia valido o che il codice che usa la struttura sia sicuro.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore alla [**struttura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convalidare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti.



| Codice restituito                                                                                                | Descrizione                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione riuscita<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                  | **Valore del** puntatore NULL<br/> |
| <dl> <dt>**TIPO E VFW \_ \_ NON \_ \_ ACCETTATO**</dt> </dl> | Tipo di supporto non valido<br/>     |



 

## <a name="remarks"></a>Commenti

Questa funzione chiama [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) per convalidare la [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel tipo di supporto. Se il tipo di formato non **è FORMAT \_ VideoInfo2,** la funzione restituisce **VFW \_ E TYPE NOT \_ \_ \_ ACCEPTED**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




