---
description: Descrive i formati di file di immagine supportati. Per le descrizioni di questi formati, vedere la sezione Osservazioni.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Enumerazione D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
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
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354829"
---
# <a name="d3dximage_fileformat-enumeration"></a>\_Enumerazione FILEformat D3DXIMAGE

Descrive i formati di file di immagine supportati. Per le descrizioni di questi formati, vedere la sezione Osservazioni.

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

Formato di file bitmap di Windows (BMP).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**\_Jpg D3DXIFF**
</dt> <dd>

Formato di file compresso JPEG (Joint Photographics Experts Group).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Formato file di immagine TrueVision (targa o TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**\_Png D3DXIFF**
</dt> <dd>

Formato di file Portable Network Graphics (PNG).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**\_DDS D3DXIFF**
</dt> <dd>

Formato di file DirectDraw Surface (DDS).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**
</dt> <dd>

Formato di file pixmap (PPM) portatile.

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**\_DIB D3DXIFF**
</dt> <dd>

Formato file DIB (Device-Independent Bitmap) Windows.

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**
</dt> <dd>

Formato di file HDR (High Dynamic Range).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Formato del file di mapping float portatile.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le funzioni che iniziano con D3DXLoadxxx supportano tutti i formati elencati. Le funzioni che iniziano con D3DXSavexxx supportano tutti i formati elencati ad eccezione dei formati TrueVision (. tga) e Portable Pixmap (. ppm).

Nella tabella seguente sono elencati i formati di input e output disponibili.



| Estensione nome del file | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bmp           | Formato bitmap di Windows. Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica. |
| .dds           | Formato del file di superficie DirectDraw. Archivia trame, trame di volumi e mappe di ambienti cubici, con o senza livelli di mipmap e con o senza compressione pixel. Vedere [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| dib           | DIB di Windows. Contiene una matrice di bit combinati con strutture che specificano la larghezza e l'altezza dell'immagine bitmap, il formato colori del dispositivo in cui è stata creata l'immagine e la risoluzione del dispositivo usato per creare l'immagine.                                                                                                              |
| . HDR           | Formato HDR. Codifica ogni pixel come colore RGBE a 32 bit, con 8 bit di mantissa per rosso, verde e blu e un esponente a 8 bit condiviso. Ogni canale viene compresso separatamente con la codifica di lunghezza di esecuzione (RLE).                                                                                                                                       |
| jpg           | Standard JPEG. Specifica la compressione di variabili di colori RGB a 24 bit e file di documento di immagine TIFF (grigio a 8 bit Tagged Image File Format).                                                                                                                                                                                                       |
| . PFM           | Formato della mappa float portatile. Formato di immagine A virgola mobile non elaborato, senza compressione. L'intestazione del file specifica la larghezza dell'immagine, l'altezza, il monocromatico o il colore e l'ordine delle parole del computer. I dati pixel vengono archiviati come valori a virgola mobile a 32 bit, con 3 valori per pixel per il colore e un valore per pixel per il monocromatico.                                |
| png           | Formato PNG. Formato bitmap non proprietario con compressione senza perdita di pagina.                                                                                                                                                                                                                                                                            |
| . ppm           | Formato pixmap portatile. Formato di file binario o ASCII per le immagini a colori che includono l'altezza e la larghezza dell'immagine e il valore del componente colore massimo.                                                                                                                                                                                                 |
| .tga           | Formato scheda grafica targa o Truevision. Supporta le profondità di 8, 15, 16, 24 e 32 bit, inclusa la scala di grigi a 8 bit, e contiene dati facoltativi per la tavolozza dei colori, l'immagine (x, y) e i dati di dimensioni e i dati pixel.                                                                                                                               |



 

Per ulteriori informazioni su alcuni di questi formati, vedere [tipi di bitmap](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
