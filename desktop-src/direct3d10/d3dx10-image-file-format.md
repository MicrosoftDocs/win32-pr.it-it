---
description: Formati di file di immagine supportati dalle funzioni D3DXCreatexxx e D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: D3DX10_IMAGE_FILE_FORMAT enumerazione (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 597f929a2a5f2800b1761fdba377f2ed022460e7585e1a9d0131d3e6e21127e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303496"
---
# <a name="d3dx10_image_file_format-enumeration"></a>Enumerazione D3DX10 \_ IMAGE \_ FILE \_ FORMAT

Formati di file di immagine supportati dalle funzioni D3DXCreatexxx e D3DX10Savexxx.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**
</dt> <dd>

Windows di file bitmap (BMP). Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo dei pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci nella tavolozza logica. L'estensione di file per questo formato è .bmp.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ JPG**
</dt> <dd>

Joint Photographic Experts Group file compresso (JPEG). Specifica la compressione variabile del colore RGB a 24 bit e dei file di documento di immagine tiFF (Gray Scale Tagged Image File Format) a 8 bit. L'estensione di file per questo formato è .jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF \_ PNG**
</dt> <dd>

Portable Network Graphics (PNG). Formato bitmap non proprietario che usa la compressione senza perdita di dati. L'estensione di file per questo formato è .png.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**
</dt> <dd>

Formato di file DDS (DirectDraw Surface). Archivia trame, trame di volume e mappe dell'ambiente cubico, con o senza livelli mipmap e con o senza compressione dei pixel. L'estensione di file per questo formato è dds.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ IFF \_ TIFF**
</dt> <dd>

Tagged Image File Format (TIFF). Le estensioni di file per questo formato sono tif e tiff.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ IFF \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). L'estensione di file per questo formato è .gif.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**
</dt> <dd>

Windows Formato foto multimediale (WMP). Questo formato è noto anche come HD Photo e JPEG XR. Le estensioni di file per questo formato sono hdp, jxr e wdp.

Per il corretto funzionamento, **D3DX10 \_ IFF \_ WMP** richiede l'inizializzazione di COM. Chiamare quindi [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) nell'applicazione prima di chiamare D3DX.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Vedere [Tipi di bitmap (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) per altre informazioni su alcuni di questi formati.

D3DX10 usa il Windows imaging per implementare la maggior parte dei tipi di file bitmap supportati. Per [altre informazioni, Windows panoramica del componente di](https://msdn.microsoft.com/library/ms737408.aspx) imaging.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
