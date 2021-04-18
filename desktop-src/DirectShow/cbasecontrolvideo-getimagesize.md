---
description: Il metodo GetImageSize recupera le informazioni sulle dimensioni dell'immagine video.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Metodo CBaseControlVideo. GetImageSize (Ctlutil. h)
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
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333800"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>CBaseControlVideo. GetImageSize, metodo

Il `GetImageSize` metodo recupera le informazioni sulle dimensioni dell'immagine video.

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

Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da compilare.

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

Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.



| Codice restituito                                                                                  | Descrizione                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Esito negativo.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido. Il formato dei dati non è compatibile.<br/>           |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Si è verificato un errore imprevisto. Uno o più argomenti sono **null**.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Esito positivo.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Questa funzione membro è una funzione helper usata per la creazione di rendering di immagini di memoria per immagini DIB. Viene chiamato dall'implementazione della classe di base di [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) quando un parametro _pVideoImage_ **null** viene passato a tale funzione membro. Di conseguenza, questa funzione membro costruisce e restituisce una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , usando le informazioni in *pBufferSize* e *pSourceRect*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




