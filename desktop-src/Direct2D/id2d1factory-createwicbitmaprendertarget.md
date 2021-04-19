---
title: Metodi CreateWicBitmapRenderTarget di ID2D1Factory
description: Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Metodo CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325791"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>Metodi ID2D1Factory:: CreateWicBitmapRenderTarget

Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                            | Descrizione                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ \_ proprietà della destinazione \_ di rendering \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).<br/> |
| [**CreateWicBitmapRenderTarget (IWICBitmap \* , d2d1 \_ proprietà della destinazione di rendering \_ \_&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Crea una destinazione di rendering che esegue il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).<br/> |



## <a name="remarks"></a>Commenti

L'applicazione deve creare le destinazioni di rendering una volta e mantenerle per la durata dell'applicazione o fino a quando non viene ricevuto l'errore di [**\_ \_ destinazione D2DERR ricreate**](direct2d-error-codes.md) . Quando si riceve questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).

**Nota**   Questo metodo non è supportato in Windows Phone e avrà esito negativo quando viene chiamato su un dispositivo con codice di errore 0x8899000b (nessun dispositivo di rendering hardware disponibile per questa operazione). Poiché l'emulatore Windows Phone supporta il rendering WARP, questo metodo avrà esito negativo quando viene chiamato sull'emulatore con un codice di errore diverso, 0x88982f80 (WinCoDec \_ Err \_ unsupportedpixelformat).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

