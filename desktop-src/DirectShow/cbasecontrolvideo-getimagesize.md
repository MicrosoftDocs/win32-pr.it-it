---
description: Il metodo GetImageSize recupera le informazioni sulle dimensioni dell'immagine video.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Metodo CBaseControlVideo.GetImageSize (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a7e0d970e06186ced3800d4b1f4dc4190778834941b69ac17402e2294312b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057061"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>Metodo CBaseControlVideo.GetImageSize

Il `GetImageSize` metodo recupera informazioni sulle dimensioni dell'immagine video.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore a [**una struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da riempire.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Puntatore alla dimensione del buffer video.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore alle dimensioni del rettangolo del video di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione. può essere uno dei valori seguenti o altri valori non elencati.



| Codice restituito                                                                                  | Descrizione                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Esito negativo.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido. Il formato dei dati non è compatibile.<br/>           |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Si è verificato un errore imprevisto. Uno o più argomenti sono **NULL.**<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Operazione completata.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Questa funzione membro è una funzione helper usata per creare rendering di immagini di memoria di immagini DIB. Viene chiamato dall'implementazione della classe di base [**di CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) quando **un** parametro null _pVideoImage_ viene passato a tale funzione membro. Di conseguenza, questa funzione membro costruisce e restituisce una struttura [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) usando le informazioni in *pBufferSize* *e pSourceRect.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




