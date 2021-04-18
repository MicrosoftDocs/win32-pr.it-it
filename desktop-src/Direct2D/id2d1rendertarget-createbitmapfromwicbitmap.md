---
title: Metodi CreateBitmapFromWicBitmap di ID2D1RenderTarget
description: Crea un ID2D1Bitmap copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Metodo CreateBitmapFromWicBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324430"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>Metodi ID2D1RenderTarget:: CreateBitmapFromWicBitmap

Crea un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                              | Descrizione                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Crea un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.<br/>  |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* , d2d1 \_ BITMAP \_ Properties&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Crea un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.<br/> |
| [**CreateBitmapFromWicBitmap ( \* proprietà bitmap IWICBitmapSource, d2d1 \_ \_ \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Crea un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.<br/> |



## <a name="remarks"></a>Commenti

Prima che Direct2D possa caricare un'immagine WIC, è necessario convertirla in un formato pixel supportato e in modalità Alpha. Per un elenco dei formati pixel supportati e delle modalità Alpha, vedere [formati di pixel supportati e modalità Alpha](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Esempio

Per esempi, vedere [come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md) e [come caricare una bitmap da una risorsa](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Formati pixel e modalità alfa supportati](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

