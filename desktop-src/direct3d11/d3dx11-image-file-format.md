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
# <a name="d3dx11_image_file_format-enumeration"></a><span data-ttu-id="00609-106">\_Enumerazione del \_ formato del file di immagine D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="00609-106">D3DX11\_IMAGE\_FILE\_FORMAT enumeration</span></span>

> [!Note]  
> <span data-ttu-id="00609-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="00609-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="00609-108">Formati di file di immagine supportati dalle funzioni D3DX11Createxxx e D3DX11Savexxx.</span><span class="sxs-lookup"><span data-stu-id="00609-108">Image file formats supported by D3DX11Createxxx and D3DX11Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="00609-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00609-109">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="00609-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="00609-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="00609-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF ( \_ BMP)**</span><span class="sxs-lookup"><span data-stu-id="00609-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="00609-112">Formato di file bitmap di Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="00609-112">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="00609-113">Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="00609-113">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="00609-114">L'estensione del file per questo formato è BMP.</span><span class="sxs-lookup"><span data-stu-id="00609-114">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="00609-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**\_Jpg D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="00609-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="00609-116">Formato file compresso Joint Photographic Experts Group (JPEG).</span><span class="sxs-lookup"><span data-stu-id="00609-116">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="00609-117">Specifica la compressione di variabili di colori RGB a 24 bit e file di documento di immagine TIFF (grigio a 8 bit Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="00609-117">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="00609-118">L'estensione di file per questo formato è. jpg.</span><span class="sxs-lookup"><span data-stu-id="00609-118">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="00609-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ IFF ( \_ png)**</span><span class="sxs-lookup"><span data-stu-id="00609-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="00609-120">Formato di file Portable Network Graphics (PNG).</span><span class="sxs-lookup"><span data-stu-id="00609-120">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="00609-121">Formato bitmap non proprietario con compressione senza perdita di pagina.</span><span class="sxs-lookup"><span data-stu-id="00609-121">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="00609-122">L'estensione di file per questo formato è. png.</span><span class="sxs-lookup"><span data-stu-id="00609-122">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="00609-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF ( \_ DDS)**</span><span class="sxs-lookup"><span data-stu-id="00609-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="00609-124">Formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="00609-124">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="00609-125">Archivia trame, trame di volumi e mappe di ambienti cubici, con o senza livelli di mipmap e con o senza compressione pixel.</span><span class="sxs-lookup"><span data-stu-id="00609-125">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="00609-126">L'estensione di file per questo formato è. DDS.</span><span class="sxs-lookup"><span data-stu-id="00609-126">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="00609-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**\_TIFF D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="00609-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="00609-128">Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="00609-128">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="00609-129">Le estensioni di file per questo formato sono TIF e TIFF.</span><span class="sxs-lookup"><span data-stu-id="00609-129">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="00609-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**\_Gif D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="00609-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="00609-131">Graphics Interchange Format (GIF).</span><span class="sxs-lookup"><span data-stu-id="00609-131">Graphics Interchange Format (GIF).</span></span> <span data-ttu-id="00609-132">L'estensione di file per questo formato è. gif.</span><span class="sxs-lookup"><span data-stu-id="00609-132">The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="00609-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ IFF \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="00609-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="00609-134">Windows Media Photo Format (WMP).</span><span class="sxs-lookup"><span data-stu-id="00609-134">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="00609-135">Questo formato è noto anche come HD Photo e JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="00609-135">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="00609-136">Le estensioni di file per questo formato sono. HDP,. JXR e. wdp.</span><span class="sxs-lookup"><span data-stu-id="00609-136">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="00609-137">Per funzionare correttamente, **D3DX11 \_ IFF \_ WMP** richiede l'inizializzazione di com.</span><span class="sxs-lookup"><span data-stu-id="00609-137">To work properly, **D3DX11\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="00609-138">Chiamare quindi [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) nell'applicazione prima di chiamare D3DX.</span><span class="sxs-lookup"><span data-stu-id="00609-138">Therefore, call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="00609-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="00609-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="00609-140">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="00609-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="00609-141">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="00609-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="00609-142">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="00609-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00609-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="00609-143">Remarks</span></span>

<span data-ttu-id="00609-144">Per ulteriori informazioni su alcuni di questi formati, vedere [tipi di bitmap (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="00609-144">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="00609-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00609-145">Requirements</span></span>



| <span data-ttu-id="00609-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="00609-146">Requirement</span></span> | <span data-ttu-id="00609-147">Valore</span><span class="sxs-lookup"><span data-stu-id="00609-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00609-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00609-148">Header</span></span><br/> | <dl> <span data-ttu-id="00609-149"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="00609-149"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00609-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00609-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00609-151">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="00609-151">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

