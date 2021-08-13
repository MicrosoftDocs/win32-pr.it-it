---
title: Metodi ID2D1RenderTarget CreateBitmapFromWicBitmap
description: Crea un oggetto ID2D1Bitmap copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Metodi CreateBitmapFromWicBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 3d023db69afdc3cc69535d310cb21fb841c2f1bbe981df98e0aaa22074a46db0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304341"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>Metodi ID2D1RenderTarget::CreateBitmapFromWicBitmap

Crea un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                                                                                              | Descrizione                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap \* \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Crea un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.<br/>  |
| [**CreateBitmapFromWicBitmap(IWICBitmapSource,D2D1 \* \_ BITMAP PROPERTIES \_&,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Crea un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.<br/> |
| [**CreateBitmapFromWicBitmap(IWICBitmapSource,D2D1 \* \_ BITMAP \_ \* PROPERTIES,ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Crea un [**oggetto ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) copiando la bitmap di Microsoft Windows Imaging Component (WIC) specificata.<br/> |



## <a name="remarks"></a>Commenti

Prima che Direct2D possa caricare un'immagine WIC, deve essere convertita in un formato pixel e in modalità alfa supportati. Per un elenco dei formati pixel supportati e delle modalità alfa, vedere [Formati di pixel supportati e modalità alfa](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Esempio

Per esempi, [vedere Come caricare una bitmap da un file](how-to-load-a-direct2d-bitmap-from-a-file.md) e Come caricare una bitmap da una [risorsa](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
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

 

