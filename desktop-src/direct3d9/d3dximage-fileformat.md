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
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="e2e3f-104">\_Enumerazione FILEformat D3DXIMAGE</span><span class="sxs-lookup"><span data-stu-id="e2e3f-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="e2e3f-105">Descrive i formati di file di immagine supportati.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-105">Describes the supported image file formats.</span></span> <span data-ttu-id="e2e3f-106">Per le descrizioni di questi formati, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e3f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2e3f-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="e2e3f-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="e2e3f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e2e3f-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-110">Formato di file bitmap di Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**\_Jpg D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-112">Formato di file compresso JPEG (Joint Photographics Experts Group).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-114">Formato file di immagine TrueVision (targa o TGA).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**\_Png D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-116">Formato di file Portable Network Graphics (PNG).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**\_DDS D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-118">Formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-120">Formato di file pixmap (PPM) portatile.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**\_DIB D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-122">Formato file DIB (Device-Independent Bitmap) Windows.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF \_ HDR**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-124">Formato di file HDR (High Dynamic Range).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-126">Formato del file di mapping float portatile.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="e2e3f-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e2e3f-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e2e3f-128">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e2e3f-129">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e2e3f-130">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2e3f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2e3f-131">Remarks</span></span>

<span data-ttu-id="e2e3f-132">Le funzioni che iniziano con D3DXLoadxxx supportano tutti i formati elencati.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="e2e3f-133">Le funzioni che iniziano con D3DXSavexxx supportano tutti i formati elencati ad eccezione dei formati TrueVision (. tga) e Portable Pixmap (. ppm).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="e2e3f-134">Nella tabella seguente sono elencati i formati di input e output disponibili.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="e2e3f-135">Estensione nome del file</span><span class="sxs-lookup"><span data-stu-id="e2e3f-135">File Extension</span></span> | <span data-ttu-id="e2e3f-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2e3f-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e3f-137">bmp</span><span class="sxs-lookup"><span data-stu-id="e2e3f-137">.bmp</span></span>           | <span data-ttu-id="e2e3f-138">Formato bitmap di Windows.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-138">Windows bitmap format.</span></span> <span data-ttu-id="e2e3f-139">Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="e2e3f-140">.dds</span><span class="sxs-lookup"><span data-stu-id="e2e3f-140">.dds</span></span>           | <span data-ttu-id="e2e3f-141">Formato del file di superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="e2e3f-142">Archivia trame, trame di volumi e mappe di ambienti cubici, con o senza livelli di mipmap e con o senza compressione pixel.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="e2e3f-143">Vedere [DDS](../direct3ddds/dx-graphics-dds.md).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="e2e3f-144">dib</span><span class="sxs-lookup"><span data-stu-id="e2e3f-144">.dib</span></span>           | <span data-ttu-id="e2e3f-145">DIB di Windows.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-145">Windows DIB.</span></span> <span data-ttu-id="e2e3f-146">Contiene una matrice di bit combinati con strutture che specificano la larghezza e l'altezza dell'immagine bitmap, il formato colori del dispositivo in cui è stata creata l'immagine e la risoluzione del dispositivo usato per creare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="e2e3f-147">. HDR</span><span class="sxs-lookup"><span data-stu-id="e2e3f-147">.hdr</span></span>           | <span data-ttu-id="e2e3f-148">Formato HDR.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-148">HDR format.</span></span> <span data-ttu-id="e2e3f-149">Codifica ogni pixel come colore RGBE a 32 bit, con 8 bit di mantissa per rosso, verde e blu e un esponente a 8 bit condiviso.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="e2e3f-150">Ogni canale viene compresso separatamente con la codifica di lunghezza di esecuzione (RLE).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="e2e3f-151">jpg</span><span class="sxs-lookup"><span data-stu-id="e2e3f-151">.jpg</span></span>           | <span data-ttu-id="e2e3f-152">Standard JPEG.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-152">JPEG standard.</span></span> <span data-ttu-id="e2e3f-153">Specifica la compressione di variabili di colori RGB a 24 bit e file di documento di immagine TIFF (grigio a 8 bit Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="e2e3f-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="e2e3f-154">. PFM</span><span class="sxs-lookup"><span data-stu-id="e2e3f-154">.pfm</span></span>           | <span data-ttu-id="e2e3f-155">Formato della mappa float portatile.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-155">Portable float map format.</span></span> <span data-ttu-id="e2e3f-156">Formato di immagine A virgola mobile non elaborato, senza compressione.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="e2e3f-157">L'intestazione del file specifica la larghezza dell'immagine, l'altezza, il monocromatico o il colore e l'ordine delle parole del computer.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="e2e3f-158">I dati pixel vengono archiviati come valori a virgola mobile a 32 bit, con 3 valori per pixel per il colore e un valore per pixel per il monocromatico.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="e2e3f-159">png</span><span class="sxs-lookup"><span data-stu-id="e2e3f-159">.png</span></span>           | <span data-ttu-id="e2e3f-160">Formato PNG.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-160">PNG format.</span></span> <span data-ttu-id="e2e3f-161">Formato bitmap non proprietario con compressione senza perdita di pagina.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="e2e3f-162">. ppm</span><span class="sxs-lookup"><span data-stu-id="e2e3f-162">.ppm</span></span>           | <span data-ttu-id="e2e3f-163">Formato pixmap portatile.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-163">Portable Pixmap format.</span></span> <span data-ttu-id="e2e3f-164">Formato di file binario o ASCII per le immagini a colori che includono l'altezza e la larghezza dell'immagine e il valore del componente colore massimo.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="e2e3f-165">.tga</span><span class="sxs-lookup"><span data-stu-id="e2e3f-165">.tga</span></span>           | <span data-ttu-id="e2e3f-166">Formato scheda grafica targa o Truevision.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="e2e3f-167">Supporta le profondità di 8, 15, 16, 24 e 32 bit, inclusa la scala di grigi a 8 bit, e contiene dati facoltativi per la tavolozza dei colori, l'immagine (x, y) e i dati di dimensioni e i dati pixel.</span><span class="sxs-lookup"><span data-stu-id="e2e3f-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="e2e3f-168">Per ulteriori informazioni su alcuni di questi formati, vedere [tipi di bitmap](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="e2e3f-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e3f-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2e3f-169">Requirements</span></span>



| <span data-ttu-id="e2e3f-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2e3f-170">Requirement</span></span> | <span data-ttu-id="e2e3f-171">Valore</span><span class="sxs-lookup"><span data-stu-id="e2e3f-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e3f-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2e3f-172">Header</span></span><br/> | <dl> <span data-ttu-id="e2e3f-173"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3f-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e3f-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2e3f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e3f-175">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="e2e3f-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
