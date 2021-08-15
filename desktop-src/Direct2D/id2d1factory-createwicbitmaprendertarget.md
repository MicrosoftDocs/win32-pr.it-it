---
title: Metodi ID2D1Factory CreateWicBitmapRenderTarget
description: Crea una destinazione di rendering di cui viene eseguito il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Metodi CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 177f5459d8245292e2962e502882bb86643f3f8b777efd8a336fde5f8c671897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698181"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>Metodi ID2D1Factory::CreateWicBitmapRenderTarget

Crea una destinazione di rendering di cui viene eseguito il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                                            | Descrizione                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET \_ \_ \* PROPERTIES,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | Crea una destinazione di rendering di cui viene eseguito il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).<br/> |
| [**CreateWicBitmapRenderTarget(IWICBitmap \* ,D2D1 \_ RENDER TARGET PROPERTIES \_ \_&,ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | Crea una destinazione di rendering di cui viene eseguito il rendering in una bitmap di Microsoft Windows Imaging Component (WIC).<br/> |



## <a name="remarks"></a>Commenti

L'applicazione deve creare le destinazioni di rendering una sola volta e tenerle per tutta la durata dell'applicazione o fino a quando non viene ricevuto l'errore [**D2DERR \_ RECREATE \_ TARGET.**](direct2d-error-codes.md) Quando viene visualizzato questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).

**Nota:**   Questo metodo non è supportato in Windows Phone e avrà esito negativo quando viene chiamato in un dispositivo con codice di errore 0x8899000b ( Non è disponibile alcun dispositivo di rendering hardware per questa operazione). Poiché il Windows Phone Emulator supporta il rendering WARP, questo metodo avrà esito negativo quando viene chiamato sull'emulatore con un codice di errore diverso, 0x88982f80 (wincodec \_ err \_ unsupportedpixelformat).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

