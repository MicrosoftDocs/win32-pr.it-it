---
title: Enumerazione D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Formati di file di immagine supportati dalle funzioni D3DX11Createxxx e D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- Enumerazione D3DX11_IMAGE_FILE_FORMAT Direct3D 11
- Puntatore di enumerazione LPD3DX11_IMAGE_FILE_FORMAT Direct3D 11
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
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982571"
---
# <a name="d3dx11_image_file_format-enumeration"></a>\_Enumerazione del \_ formato del file di immagine D3DX11 \_

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

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF ( \_ BMP)**
</dt> <dd>

Formato di file bitmap di Windows (BMP). Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica. L'estensione del file per questo formato è BMP.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**\_Jpg D3DX11 IFF \_**
</dt> <dd>

Formato file compresso Joint Photographic Experts Group (JPEG). Specifica la compressione di variabili di colori RGB a 24 bit e file di documento di immagine TIFF (grigio a 8 bit Tagged Image File Format). L'estensione di file per questo formato è. jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ IFF ( \_ png)**
</dt> <dd>

Formato di file Portable Network Graphics (PNG). Formato bitmap non proprietario con compressione senza perdita di pagina. L'estensione di file per questo formato è. png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF ( \_ DDS)**
</dt> <dd>

Formato di file DirectDraw Surface (DDS). Archivia trame, trame di volumi e mappe di ambienti cubici, con o senza livelli di mipmap e con o senza compressione pixel. L'estensione di file per questo formato è. DDS.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**\_TIFF D3DX11 IFF \_**
</dt> <dd>

Tagged Image File Format (TIFF). Le estensioni di file per questo formato sono TIF e TIFF.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**\_Gif D3DX11 IFF \_**
</dt> <dd>

Graphics Interchange Format (GIF). L'estensione di file per questo formato è. gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ IFF \_ WMP**
</dt> <dd>

Windows Media Photo Format (WMP). Questo formato è noto anche come HD Photo e JPEG XR. Le estensioni di file per questo formato sono. HDP,. JXR e. wdp.

Per funzionare correttamente, **D3DX11 \_ IFF \_ WMP** richiede l'inizializzazione di com. Chiamare quindi [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) nell'applicazione prima di chiamare D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su alcuni di questi formati, vedere [tipi di bitmap (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

