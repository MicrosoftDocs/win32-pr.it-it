---
description: Formati di file di immagine supportati dalle funzioni D3DXCreatexxx e D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: Enumerazione D3DX10_IMAGE_FILE_FORMAT (D3DX10Tex. h)
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
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762262"
---
# <a name="d3dx10_image_file_format-enumeration"></a>\_Enumerazione del \_ formato del file di immagine d3dx10 \_

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

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF ( \_ BMP)**
</dt> <dd>

Formato di file bitmap di Windows (BMP). Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica. L'estensione del file per questo formato è BMP.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**\_Jpg d3dx10 IFF \_**
</dt> <dd>

Formato file compresso Joint Photographic Experts Group (JPEG). Specifica la compressione di variabili di colori RGB a 24 bit e file di documento di immagine TIFF (grigio a 8 bit Tagged Image File Format). L'estensione di file per questo formato è. jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF ( \_ png)**
</dt> <dd>

Formato di file Portable Network Graphics (PNG). Formato bitmap non proprietario con compressione senza perdita di pagina. L'estensione di file per questo formato è. png.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF ( \_ DDS)**
</dt> <dd>

Formato di file DirectDraw Surface (DDS). Archivia trame, trame di volumi e mappe di ambienti cubici, con o senza livelli di mipmap e con o senza compressione pixel. L'estensione di file per questo formato è. DDS.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**\_TIFF d3dx10 IFF \_**
</dt> <dd>

Tagged Image File Format (TIFF). Le estensioni di file per questo formato sono TIF e TIFF.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**\_Gif d3dx10 IFF \_**
</dt> <dd>

Graphics Interchange Format (GIF). L'estensione di file per questo formato è. gif.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**
</dt> <dd>

Windows Media Photo Format (WMP). Questo formato è noto anche come HD Photo e JPEG XR. Le estensioni di file per questo formato sono. HDP,. JXR e. wdp.

Per funzionare correttamente, **d3dx10 \_ IFF \_ WMP** richiede l'inizializzazione di com. Chiamare quindi [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) nell'applicazione prima di chiamare D3DX.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su alcuni di questi formati, vedere [tipi di bitmap (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

D3DX10 usa il componente Windows Imaging per implementare la maggior parte dei tipi di file bitmap supportati. Per ulteriori informazioni, vedere [Cenni preliminari sui componenti Windows Imaging](https://msdn.microsoft.com/library/ms737408.aspx) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
