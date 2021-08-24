---
description: Descrive i formati di file di immagine supportati. Per le descrizioni di questi formati, vedere Note.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: D3DXIMAGE_FILEFORMAT enumerazione (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 715b9f0f6d8c56153d51c9c19b70ba253e508619229f52201a28f23c1902d26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123167"
---
# <a name="d3dximage_fileformat-enumeration"></a>Enumerazione D3DXIMAGE \_ FILEFORMAT

Descrive i formati di file di immagine supportati. Per le descrizioni di questi formati, vedere Note.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**
</dt> <dd>

Windows di file bitmap (BMP).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ JPG**
</dt> <dd>

Formato di file compresso JPEG (Joint Photographics Experts Group).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Formato di file di immagine Truevision (Tutto, O TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**
</dt> <dd>

Portable Network Graphics (PNG).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

Formato di file DDS (DirectDraw Surface).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ PPM**
</dt> <dd>

Formato di file pixmap portabile (PPM).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Windows di file bitmap indipendente dal dispositivo (DIB).

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

Formato di file HDR (High Dynamic Range).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Formato di file mappa float portabile.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le funzioni che iniziano con D3DXLoadxxx supportano tutti i formati elencati. Le funzioni che iniziano con D3DXSavexxx supportano tutti i formati elencati tranne i formati Truevision (con estensione tga) e pixmap portabile (con estensione ppm).

Nella tabella seguente sono elencati i formati di input e output disponibili.



| Estensione nome del file | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bmp           | Windows bitmap. Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo dei pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci nella tavolozza logica. |
| .dds           | Formato di file DirectDraw Surface. Archivia trame, trame di volume e mappe dell'ambiente cubico, con o senza livelli mipmap e con o senza compressione dei pixel. Vedere [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| dib           | Windows Dib. Contiene una matrice di bit combinati con strutture che specificano larghezza e altezza dell'immagine bitmap, il formato del colore del dispositivo in cui è stata creata l'immagine e la risoluzione del dispositivo usato per creare l'immagine.                                                                                                              |
| .hdr           | Formato HDR. Codifica ogni pixel come colore RGBE a 32 bit, con 8 bit di mantissa per rosso, verde e blu e un esponente condiviso a 8 bit. Ogni canale viene compresso separatamente con la codifica RLE (Run-Length Encoding).                                                                                                                                       |
| jpg           | Standard JPEG. Specifica la compressione variabile dei file di documento di immagine TIFF (Gray Scale Tagged Image File Format) a 24 bit e RGB a 24 bit.                                                                                                                                                                                                       |
| .pfm           | Formato mappa float portabile. Formato di immagine a virgola mobile non elaborato, senza alcuna compressione. L'intestazione del file specifica la larghezza, l'altezza, la monocromatica o il colore dell'immagine e l'ordine delle parole macchina. I dati pixel vengono archiviati come valori a virgola mobile a 32 bit, con 3 valori per pixel per colore e un valore per pixel per monocromatico.                                |
| png           | Formato PNG. Formato bitmap non proprietario che usa la compressione senza perdita di dati.                                                                                                                                                                                                                                                                            |
| PPM           | Formato Pixmap portabile. Formato di file binario o ASCII per le immagini a colori che include l'altezza e la larghezza dell'immagine e il valore massimo del componente colore.                                                                                                                                                                                                 |
| .tga           | Formato di Adattatore grafica Diass o Truevision. Supporta profondità di 8, 15, 16, 24 e 32 bit, tra cui scala di grigi a 8 bit e contiene dati facoltativi della tavolozza dei colori, dati di origine e dimensioni delle immagini (x, y) e pixel.                                                                                                                               |



 

Per altre informazioni su alcuni di questi [formati,](../gdiplus/-gdiplus-types-of-bitmaps-about.md) vedere Tipi di bitmap.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9tex.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
