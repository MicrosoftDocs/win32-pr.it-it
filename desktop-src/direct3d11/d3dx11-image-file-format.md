---
title: D3DX11_IMAGE_FILE_FORMAT enumerazione (D3DX11tex.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Formati di file di immagine supportati dalle funzioni D3DX11Createxxx e D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- D3DX11_IMAGE_FILE_FORMAT enumerazione Direct3D 11
- LPD3DX11_IMAGE_FILE_FORMAT puntatore di enumerazione Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34d3ab49987d499114c4b9eee695bfad02055fbbef785a955407e97843208f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536965"
---
# <a name="d3dx11_image_file_format-enumeration"></a>Enumerazione D3DX11 \_ IMAGE \_ FILE \_ FORMAT

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Formati di file di immagine supportati dalle funzioni D3DX11Createxxx e D3DX11Savexxx.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF \_ BMP**
</dt> <dd>

Windows di file bitmap (BMP). Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci nella tavolozza logica. L'estensione di file per questo formato è .bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ JPG**
</dt> <dd>

Joint Photographic Experts Group di file compresso JPEG (Jpeg). Specifica la compressione variabile dei file di documento di immagine TIFF (Gray-scale Tagged Image File Format) a 24 bit e di colore RGB a 24 bit. L'estensione di file per questo formato è .jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ IFF \_ PNG**
</dt> <dd>

Portable Network Graphics (PNG). Formato bitmap non proprietario che usa la compressione senza perdita di dati. L'estensione di file per questo formato è .png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF \_ DDS**
</dt> <dd>

Formato di file DDS (Surface Surface) DirectDraw. Archivia trame, trame di volume e mappe di ambiente cubiche, con o senza livelli mipmap e con o senza compressione pixel. L'estensione di file per questo formato è dds.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Le estensioni di file per questo formato sono tif e tiff.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ IFF \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). L'estensione di file per questo formato è .gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ IFF \_ WMP**
</dt> <dd>

Windows Formato Foto multimediale (WMP). Questo formato è noto anche come HD Photo e JPEG XR. Le estensioni di file per questo formato sono hdp, jxr e wdp.

Per il corretto funzionamento, **D3DX11 \_ IFF \_ WMP** richiede l'inizializzazione di COM. Pertanto, chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) nell'applicazione prima di chiamare D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Vedere [Tipi di bitmap (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) per altre informazioni su alcuni di questi formati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

