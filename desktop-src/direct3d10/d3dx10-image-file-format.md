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
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="7033c-103">\_Enumerazione del \_ formato del file di immagine d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="7033c-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="7033c-104">Formati di file di immagine supportati dalle funzioni D3DXCreatexxx e D3DX10Savexxx.</span><span class="sxs-lookup"><span data-stu-id="7033c-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7033c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7033c-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="7033c-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7033c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7033c-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF ( \_ BMP)**</span><span class="sxs-lookup"><span data-stu-id="7033c-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-108">Formato di file bitmap di Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="7033c-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="7033c-109">Contiene un'intestazione che descrive la risoluzione del dispositivo in cui è stato creato il rettangolo di pixel, le dimensioni del rettangolo, le dimensioni della matrice di bit, una tavolozza logica e una matrice di bit che definisce la relazione tra i pixel nell'immagine bitmap e le voci della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="7033c-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="7033c-110">L'estensione del file per questo formato è BMP.</span><span class="sxs-lookup"><span data-stu-id="7033c-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**\_Jpg d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="7033c-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-112">Formato file compresso Joint Photographic Experts Group (JPEG).</span><span class="sxs-lookup"><span data-stu-id="7033c-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="7033c-113">Specifica la compressione di variabili di colori RGB a 24 bit e file di documento di immagine TIFF (grigio a 8 bit Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="7033c-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="7033c-114">L'estensione di file per questo formato è. jpg.</span><span class="sxs-lookup"><span data-stu-id="7033c-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF ( \_ png)**</span><span class="sxs-lookup"><span data-stu-id="7033c-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-116">Formato di file Portable Network Graphics (PNG).</span><span class="sxs-lookup"><span data-stu-id="7033c-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="7033c-117">Formato bitmap non proprietario con compressione senza perdita di pagina.</span><span class="sxs-lookup"><span data-stu-id="7033c-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="7033c-118">L'estensione di file per questo formato è. png.</span><span class="sxs-lookup"><span data-stu-id="7033c-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF ( \_ DDS)**</span><span class="sxs-lookup"><span data-stu-id="7033c-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-120">Formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="7033c-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="7033c-121">Archivia trame, trame di volumi e mappe di ambienti cubici, con o senza livelli di mipmap e con o senza compressione pixel.</span><span class="sxs-lookup"><span data-stu-id="7033c-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="7033c-122">L'estensione di file per questo formato è. DDS.</span><span class="sxs-lookup"><span data-stu-id="7033c-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**\_TIFF d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="7033c-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-124">Tagged Image File Format (TIFF).</span><span class="sxs-lookup"><span data-stu-id="7033c-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="7033c-125">Le estensioni di file per questo formato sono TIF e TIFF.</span><span class="sxs-lookup"><span data-stu-id="7033c-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**\_Gif d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="7033c-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-127">Graphics Interchange Format (GIF). L'estensione di file per questo formato è. gif.</span><span class="sxs-lookup"><span data-stu-id="7033c-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**</span><span class="sxs-lookup"><span data-stu-id="7033c-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-129">Windows Media Photo Format (WMP).</span><span class="sxs-lookup"><span data-stu-id="7033c-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="7033c-130">Questo formato è noto anche come HD Photo e JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="7033c-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="7033c-131">Le estensioni di file per questo formato sono. HDP,. JXR e. wdp.</span><span class="sxs-lookup"><span data-stu-id="7033c-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="7033c-132">Per funzionare correttamente, **d3dx10 \_ IFF \_ WMP** richiede l'inizializzazione di com.</span><span class="sxs-lookup"><span data-stu-id="7033c-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="7033c-133">Chiamare quindi [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) nell'applicazione prima di chiamare D3DX.</span><span class="sxs-lookup"><span data-stu-id="7033c-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="7033c-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7033c-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7033c-135">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7033c-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7033c-136">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="7033c-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7033c-137">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7033c-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7033c-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="7033c-138">Remarks</span></span>

<span data-ttu-id="7033c-139">Per ulteriori informazioni su alcuni di questi formati, vedere [tipi di bitmap (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="7033c-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="7033c-140">D3DX10 usa il componente Windows Imaging per implementare la maggior parte dei tipi di file bitmap supportati.</span><span class="sxs-lookup"><span data-stu-id="7033c-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="7033c-141">Per ulteriori informazioni, vedere [Cenni preliminari sui componenti Windows Imaging](https://msdn.microsoft.com/library/ms737408.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7033c-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7033c-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7033c-142">Requirements</span></span>



| <span data-ttu-id="7033c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7033c-143">Requirement</span></span> | <span data-ttu-id="7033c-144">Valore</span><span class="sxs-lookup"><span data-stu-id="7033c-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7033c-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7033c-145">Header</span></span><br/> | <dl> <span data-ttu-id="7033c-146"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7033c-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7033c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7033c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7033c-148">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="7033c-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
