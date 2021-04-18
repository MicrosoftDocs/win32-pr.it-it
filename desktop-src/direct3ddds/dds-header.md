---
title: Struttura DDS_HEADER (DDS. h)
description: Descrive un'intestazione del file DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- Struttura DDS_HEADER DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322292"
---
# <a name="dds_header-structure"></a><span data-ttu-id="8f40d-104">\_Struttura dell'intestazione DDS</span><span class="sxs-lookup"><span data-stu-id="8f40d-104">DDS\_HEADER structure</span></span>

<span data-ttu-id="8f40d-105">Descrive un'intestazione del file DDS.</span><span class="sxs-lookup"><span data-stu-id="8f40d-105">Describes a DDS file header.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f40d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f40d-106">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a><span data-ttu-id="8f40d-107">Members</span><span class="sxs-lookup"><span data-stu-id="8f40d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f40d-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8f40d-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-109">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-110">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="8f40d-110">Size of structure.</span></span> <span data-ttu-id="8f40d-111">Questo membro deve essere impostato su 124.</span><span class="sxs-lookup"><span data-stu-id="8f40d-111">This member must be set to 124.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="8f40d-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-113">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-113">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-114">Flag per indicare quali membri contengono dati validi.</span><span class="sxs-lookup"><span data-stu-id="8f40d-114">Flags to indicate which members contain valid data.</span></span>



| <span data-ttu-id="8f40d-115">Flag</span><span class="sxs-lookup"><span data-stu-id="8f40d-115">Flag</span></span>              | <span data-ttu-id="8f40d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f40d-116">Description</span></span>                                                  | <span data-ttu-id="8f40d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8f40d-117">Value</span></span>    |
|-------------------|--------------------------------------------------------------|----------|
| <span data-ttu-id="8f40d-118">DDSD \_ Caps</span><span class="sxs-lookup"><span data-stu-id="8f40d-118">DDSD\_CAPS</span></span>        | <span data-ttu-id="8f40d-119">Obbligatorio in ogni file. DDS.</span><span class="sxs-lookup"><span data-stu-id="8f40d-119">Required in every .dds file.</span></span>                                 | <span data-ttu-id="8f40d-120">0x1</span><span class="sxs-lookup"><span data-stu-id="8f40d-120">0x1</span></span>      |
| <span data-ttu-id="8f40d-121">\_altezza DDSD</span><span class="sxs-lookup"><span data-stu-id="8f40d-121">DDSD\_HEIGHT</span></span>      | <span data-ttu-id="8f40d-122">Obbligatorio in ogni file. DDS.</span><span class="sxs-lookup"><span data-stu-id="8f40d-122">Required in every .dds file.</span></span>                                 | <span data-ttu-id="8f40d-123">0x2</span><span class="sxs-lookup"><span data-stu-id="8f40d-123">0x2</span></span>      |
| <span data-ttu-id="8f40d-124">\_larghezza DDSD</span><span class="sxs-lookup"><span data-stu-id="8f40d-124">DDSD\_WIDTH</span></span>       | <span data-ttu-id="8f40d-125">Obbligatorio in ogni file. DDS.</span><span class="sxs-lookup"><span data-stu-id="8f40d-125">Required in every .dds file.</span></span>                                 | <span data-ttu-id="8f40d-126">0x4</span><span class="sxs-lookup"><span data-stu-id="8f40d-126">0x4</span></span>      |
| <span data-ttu-id="8f40d-127">DDSD \_ pitch</span><span class="sxs-lookup"><span data-stu-id="8f40d-127">DDSD\_PITCH</span></span>       | <span data-ttu-id="8f40d-128">Obbligatorio quando viene fornito un pitch per una trama non compressa.</span><span class="sxs-lookup"><span data-stu-id="8f40d-128">Required when pitch is provided for an uncompressed texture.</span></span> | <span data-ttu-id="8f40d-129">0x8</span><span class="sxs-lookup"><span data-stu-id="8f40d-129">0x8</span></span>      |
| <span data-ttu-id="8f40d-130">DDSD \_ PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="8f40d-130">DDSD\_PIXELFORMAT</span></span> | <span data-ttu-id="8f40d-131">Obbligatorio in ogni file. DDS.</span><span class="sxs-lookup"><span data-stu-id="8f40d-131">Required in every .dds file.</span></span>                                 | <span data-ttu-id="8f40d-132">0x1000</span><span class="sxs-lookup"><span data-stu-id="8f40d-132">0x1000</span></span>   |
| <span data-ttu-id="8f40d-133">\_MIPMAPCOUNT DDSD</span><span class="sxs-lookup"><span data-stu-id="8f40d-133">DDSD\_MIPMAPCOUNT</span></span> | <span data-ttu-id="8f40d-134">Obbligatorio in una trama mipmap.</span><span class="sxs-lookup"><span data-stu-id="8f40d-134">Required in a mipmapped texture.</span></span>                             | <span data-ttu-id="8f40d-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="8f40d-135">0x20000</span></span>  |
| <span data-ttu-id="8f40d-136">\_LINEARSIZE DDSD</span><span class="sxs-lookup"><span data-stu-id="8f40d-136">DDSD\_LINEARSIZE</span></span>  | <span data-ttu-id="8f40d-137">Obbligatorio quando viene fornito un pitch per una trama compressa.</span><span class="sxs-lookup"><span data-stu-id="8f40d-137">Required when pitch is provided for a compressed texture.</span></span>    | <span data-ttu-id="8f40d-138">0x80000</span><span class="sxs-lookup"><span data-stu-id="8f40d-138">0x80000</span></span>  |
| <span data-ttu-id="8f40d-139">\_profondità DDSD</span><span class="sxs-lookup"><span data-stu-id="8f40d-139">DDSD\_DEPTH</span></span>       | <span data-ttu-id="8f40d-140">Obbligatorio in una trama di profondità.</span><span class="sxs-lookup"><span data-stu-id="8f40d-140">Required in a depth texture.</span></span>                                 | <span data-ttu-id="8f40d-141">0x800000</span><span class="sxs-lookup"><span data-stu-id="8f40d-141">0x800000</span></span> |



 

> [!Note]  
> <span data-ttu-id="8f40d-142">Quando si scrivono file con estensione DDS, è necessario impostare i \_ flag DDSD Caps e DDSD \_ PIXELFORMAT e per le trame mipmap è necessario impostare anche il \_ flag DDSD MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="8f40d-142">When you write .dds files, you should set the DDSD\_CAPS and DDSD\_PIXELFORMAT flags, and for mipmapped textures you should also set the DDSD\_MIPMAPCOUNT flag.</span></span> <span data-ttu-id="8f40d-143">Tuttavia, quando si legge un file con estensione DDS, è consigliabile non basarsi sui \_ flag DDSD Caps, DDSD \_ PIXELFORMAT e DDSD \_ MIPMAPCOUNT impostati in quanto alcuni writer di tale file potrebbero non impostare questi flag.</span><span class="sxs-lookup"><span data-stu-id="8f40d-143">However, when you read a .dds file, you should not rely on the DDSD\_CAPS, DDSD\_PIXELFORMAT, and DDSD\_MIPMAPCOUNT flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="8f40d-144">Il \_ \_ flag di trama dei flag di intestazione DDS \_ , definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDSD Caps, DDSD \_ Height, DDSD \_ Width e DDSD \_ PIXELFORMAT.</span><span class="sxs-lookup"><span data-stu-id="8f40d-144">The DDS\_HEADER\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSD\_CAPS, DDSD\_HEIGHT, DDSD\_WIDTH, and DDSD\_PIXELFORMAT flags.</span></span>

<span data-ttu-id="8f40d-145">Il flag di \_ intestazione DDS \_ flag \_ MIPMAP, che è definito in DDS. h, è uguale al \_ flag DDSD MIPMAPCOUNT.</span><span class="sxs-lookup"><span data-stu-id="8f40d-145">The DDS\_HEADER\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is equal to the DDSD\_MIPMAPCOUNT flag.</span></span>

<span data-ttu-id="8f40d-146">Il flag \_ del \_ volume dei flag di intestazione DDS \_ , definito in DDS. h, è uguale al \_ flag di profondità DDSD.</span><span class="sxs-lookup"><span data-stu-id="8f40d-146">The DDS\_HEADER\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSD\_DEPTH flag.</span></span>

<span data-ttu-id="8f40d-147">Il flag \_ di \_ pitch dei flag di intestazione DDS \_ , definito in DDS. h, è uguale al \_ flag di pitch DDSD.</span><span class="sxs-lookup"><span data-stu-id="8f40d-147">The DDS\_HEADER\_FLAGS\_PITCH flag, which is defined in Dds.h, is equal to the DDSD\_PITCH flag.</span></span>

<span data-ttu-id="8f40d-148">Il flag di \_ intestazione DDS \_ flag \_ LINEARSIZE, che è definito in DDS. h, è uguale al \_ flag DDSD LINEARSIZE.</span><span class="sxs-lookup"><span data-stu-id="8f40d-148">The DDS\_HEADER\_FLAGS\_LINEARSIZE flag, which is defined in Dds.h, is equal to the DDSD\_LINEARSIZE flag.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-149">**dwHeight**</span><span class="sxs-lookup"><span data-stu-id="8f40d-149">**dwHeight**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-150">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-150">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-151">Altezza della superficie (in pixel).</span><span class="sxs-lookup"><span data-stu-id="8f40d-151">Surface height (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-152">**dwWidth**</span><span class="sxs-lookup"><span data-stu-id="8f40d-152">**dwWidth**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-153">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-153">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-154">Larghezza della superficie (in pixel).</span><span class="sxs-lookup"><span data-stu-id="8f40d-154">Surface width (in pixels).</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-155">**dwPitchOrLinearSize**</span><span class="sxs-lookup"><span data-stu-id="8f40d-155">**dwPitchOrLinearSize**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-156">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-156">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-157">Il pitch o il numero di byte per riga di analisi in una trama non compressa; numero totale di byte nella trama di primo livello per una trama compressa.</span><span class="sxs-lookup"><span data-stu-id="8f40d-157">The pitch or number of bytes per scan line in an uncompressed texture; the total number of bytes in the top level texture for a compressed texture.</span></span> <span data-ttu-id="8f40d-158">Per informazioni su come calcolare il passo, vedere la sezione relativa al layout dei file DDS della [Guida alla programmazione per DDS](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="8f40d-158">For information about how to compute the pitch, see the DDS File Layout section of the [Programming Guide for DDS](dx-graphics-dds-pguide.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-159">**dwDepth**</span><span class="sxs-lookup"><span data-stu-id="8f40d-159">**dwDepth**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-160">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-160">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-161">Profondità di una trama del volume (in pixel), altrimenti inutilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f40d-161">Depth of a volume texture (in pixels), otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-162">**dwMipMapCount**</span><span class="sxs-lookup"><span data-stu-id="8f40d-162">**dwMipMapCount**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-163">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-163">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-164">Numero di livelli di mipmap, altrimenti non utilizzati.</span><span class="sxs-lookup"><span data-stu-id="8f40d-164">Number of mipmap levels, otherwise unused.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-165">**dwReserved1 \[ 11\]**</span><span class="sxs-lookup"><span data-stu-id="8f40d-165">**dwReserved1\[11\]**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-166">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-166">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-167">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8f40d-167">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-168">**ddspf**</span><span class="sxs-lookup"><span data-stu-id="8f40d-168">**ddspf**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-169">Tipo: **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-169">Type: **[**DDS\_PIXELFORMAT**](dds-pixelformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-170">Formato pixel (vedere [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).</span><span class="sxs-lookup"><span data-stu-id="8f40d-170">The pixel format (see [**DDS\_PIXELFORMAT**](dds-pixelformat.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-171">**dwCaps**</span><span class="sxs-lookup"><span data-stu-id="8f40d-171">**dwCaps**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-172">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-172">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-173">Specifica la complessità delle superfici archiviate.</span><span class="sxs-lookup"><span data-stu-id="8f40d-173">Specifies the complexity of the surfaces stored.</span></span>



| <span data-ttu-id="8f40d-174">Flag</span><span class="sxs-lookup"><span data-stu-id="8f40d-174">Flag</span></span>             | <span data-ttu-id="8f40d-175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f40d-175">Description</span></span>                                                                                                                              | <span data-ttu-id="8f40d-176">Valore</span><span class="sxs-lookup"><span data-stu-id="8f40d-176">Value</span></span>    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| <span data-ttu-id="8f40d-177">\_complesso DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="8f40d-177">DDSCAPS\_COMPLEX</span></span> | <span data-ttu-id="8f40d-178">Opzionale deve essere usato in qualsiasi file che contiene più di una superficie (un mipmap, una mappa dell'ambiente cubica o una trama del volume mipmap).</span><span class="sxs-lookup"><span data-stu-id="8f40d-178">Optional; must be used on any file that contains more than one surface (a mipmap, a cubic environment map, or mipmapped volume texture).</span></span> | <span data-ttu-id="8f40d-179">0x8</span><span class="sxs-lookup"><span data-stu-id="8f40d-179">0x8</span></span>      |
| <span data-ttu-id="8f40d-180">\_MIPMAP DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="8f40d-180">DDSCAPS\_MIPMAP</span></span>  | <span data-ttu-id="8f40d-181">Opzionale deve essere usato per un mipmap.</span><span class="sxs-lookup"><span data-stu-id="8f40d-181">Optional; should be used for a mipmap.</span></span>                                                                                                   | <span data-ttu-id="8f40d-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="8f40d-182">0x400000</span></span> |
| <span data-ttu-id="8f40d-183">\_trama DDSCAPS</span><span class="sxs-lookup"><span data-stu-id="8f40d-183">DDSCAPS\_TEXTURE</span></span> | <span data-ttu-id="8f40d-184">Necessario</span><span class="sxs-lookup"><span data-stu-id="8f40d-184">Required</span></span>                                                                                                                                 | <span data-ttu-id="8f40d-185">0x1000</span><span class="sxs-lookup"><span data-stu-id="8f40d-185">0x1000</span></span>   |



 

> [!Note]  
> <span data-ttu-id="8f40d-186">Quando si scrivono file con estensione DDS, è necessario impostare il \_ flag di trama ddsCaps e per più superfici è necessario impostare anche il \_ flag complesso ddsCaps.</span><span class="sxs-lookup"><span data-stu-id="8f40d-186">When you write .dds files, you should set the DDSCAPS\_TEXTURE flag, and for multiple surfaces you should also set the DDSCAPS\_COMPLEX flag.</span></span> <span data-ttu-id="8f40d-187">Tuttavia, quando si legge un file con estensione DDS, è consigliabile non basarsi sulla \_ trama ddsCaps e sui \_ flag complessi ddsCaps impostati, perché alcuni writer di tale file potrebbero non impostare questi flag.</span><span class="sxs-lookup"><span data-stu-id="8f40d-187">However, when you read a .dds file, you should not rely on the DDSCAPS\_TEXTURE and DDSCAPS\_COMPLEX flags being set because some writers of such a file might not set these flags.</span></span>

 

<span data-ttu-id="8f40d-188">Il \_ flag MIPMAP della superficie DDS \_ \_ , definito in DDS. h, è una combinazione OR bit per bit dei \_ flag ddsCaps Complex e ddsCaps \_ MIPMAP.</span><span class="sxs-lookup"><span data-stu-id="8f40d-188">The DDS\_SURFACE\_FLAGS\_MIPMAP flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS\_COMPLEX and DDSCAPS\_MIPMAP flags.</span></span>

<span data-ttu-id="8f40d-189">Il flag \_ di \_ trama dei flag di superficie DDS \_ , definito in DDS. h, è uguale al \_ flag di trama ddsCaps.</span><span class="sxs-lookup"><span data-stu-id="8f40d-189">The DDS\_SURFACE\_FLAGS\_TEXTURE flag, which is defined in Dds.h, is equal to the DDSCAPS\_TEXTURE flag.</span></span>

<span data-ttu-id="8f40d-190">Il flag \_ mappa cubi della superficie DDS \_ \_ , definito in DDS. h, equivale al \_ flag ddsCaps complesso.</span><span class="sxs-lookup"><span data-stu-id="8f40d-190">The DDS\_SURFACE\_FLAGS\_CUBEMAP flag, which is defined in Dds.h, is equal to the DDSCAPS\_COMPLEX flag.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-191">**dwCaps2**</span><span class="sxs-lookup"><span data-stu-id="8f40d-191">**dwCaps2**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-192">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-192">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-193">Ulteriori dettagli sulle superfici archiviate.</span><span class="sxs-lookup"><span data-stu-id="8f40d-193">Additional detail about the surfaces stored.</span></span>



| <span data-ttu-id="8f40d-194">Flag</span><span class="sxs-lookup"><span data-stu-id="8f40d-194">Flag</span></span>                         | <span data-ttu-id="8f40d-195">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f40d-195">Description</span></span>                                            | <span data-ttu-id="8f40d-196">Valore</span><span class="sxs-lookup"><span data-stu-id="8f40d-196">Value</span></span>    |
|------------------------------|--------------------------------------------------------|----------|
| <span data-ttu-id="8f40d-197">\_Mappa cubi DDSCAPS2</span><span class="sxs-lookup"><span data-stu-id="8f40d-197">DDSCAPS2\_CUBEMAP</span></span>            | <span data-ttu-id="8f40d-198">Obbligatorio per una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-198">Required for a cube map.</span></span>                               | <span data-ttu-id="8f40d-199">0x200</span><span class="sxs-lookup"><span data-stu-id="8f40d-199">0x200</span></span>    |
| <span data-ttu-id="8f40d-200">DDSCAPS2 \_ mappa cubi \_ POSITIVEX</span><span class="sxs-lookup"><span data-stu-id="8f40d-200">DDSCAPS2\_CUBEMAP\_POSITIVEX</span></span> | <span data-ttu-id="8f40d-201">Obbligatorio quando queste superfici vengono archiviate in una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-201">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="8f40d-202">0x400</span><span class="sxs-lookup"><span data-stu-id="8f40d-202">0x400</span></span>    |
| <span data-ttu-id="8f40d-203">DDSCAPS2 \_ mappa cubi \_ NEGATIVEX</span><span class="sxs-lookup"><span data-stu-id="8f40d-203">DDSCAPS2\_CUBEMAP\_NEGATIVEX</span></span> | <span data-ttu-id="8f40d-204">Obbligatorio quando queste superfici vengono archiviate in una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-204">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="8f40d-205">0x800</span><span class="sxs-lookup"><span data-stu-id="8f40d-205">0x800</span></span>    |
| <span data-ttu-id="8f40d-206">DDSCAPS2 \_ mappa cubi \_ positivo</span><span class="sxs-lookup"><span data-stu-id="8f40d-206">DDSCAPS2\_CUBEMAP\_POSITIVEY</span></span> | <span data-ttu-id="8f40d-207">Obbligatorio quando queste superfici vengono archiviate in una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-207">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="8f40d-208">0x1000</span><span class="sxs-lookup"><span data-stu-id="8f40d-208">0x1000</span></span>   |
| <span data-ttu-id="8f40d-209">DDSCAPS2 \_ mappa cubi \_ negativo</span><span class="sxs-lookup"><span data-stu-id="8f40d-209">DDSCAPS2\_CUBEMAP\_NEGATIVEY</span></span> | <span data-ttu-id="8f40d-210">Obbligatorio quando queste superfici vengono archiviate in una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-210">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="8f40d-211">0x2000</span><span class="sxs-lookup"><span data-stu-id="8f40d-211">0x2000</span></span>   |
| <span data-ttu-id="8f40d-212">DDSCAPS2 \_ mappa cubi \_ POSITIVEZ</span><span class="sxs-lookup"><span data-stu-id="8f40d-212">DDSCAPS2\_CUBEMAP\_POSITIVEZ</span></span> | <span data-ttu-id="8f40d-213">Obbligatorio quando queste superfici vengono archiviate in una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-213">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="8f40d-214">0x4000</span><span class="sxs-lookup"><span data-stu-id="8f40d-214">0x4000</span></span>   |
| <span data-ttu-id="8f40d-215">DDSCAPS2 \_ mappa cubi \_ NEGATIVEZ</span><span class="sxs-lookup"><span data-stu-id="8f40d-215">DDSCAPS2\_CUBEMAP\_NEGATIVEZ</span></span> | <span data-ttu-id="8f40d-216">Obbligatorio quando queste superfici vengono archiviate in una mappa cubo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-216">Required when these surfaces are stored in a cube map.</span></span> | <span data-ttu-id="8f40d-217">0x8000</span><span class="sxs-lookup"><span data-stu-id="8f40d-217">0x8000</span></span>   |
| <span data-ttu-id="8f40d-218">\_Volume DDSCAPS2</span><span class="sxs-lookup"><span data-stu-id="8f40d-218">DDSCAPS2\_VOLUME</span></span>             | <span data-ttu-id="8f40d-219">Obbligatorio per una trama del volume.</span><span class="sxs-lookup"><span data-stu-id="8f40d-219">Required for a volume texture.</span></span>                         | <span data-ttu-id="8f40d-220">0x200000</span><span class="sxs-lookup"><span data-stu-id="8f40d-220">0x200000</span></span> |



 

<span data-ttu-id="8f40d-221">Il \_ flag DDS mappa cubi \_ POSITIVEX, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi POSITIVEX \_ .</span><span class="sxs-lookup"><span data-stu-id="8f40d-221">The DDS\_CUBEMAP\_POSITIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEX flags.</span></span>

<span data-ttu-id="8f40d-222">Il \_ flag DDS mappa cubi \_ NEGATIVEX, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi NEGATIVEX \_ .</span><span class="sxs-lookup"><span data-stu-id="8f40d-222">The DDS\_CUBEMAP\_NEGATIVEX flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEX flags.</span></span>

<span data-ttu-id="8f40d-223">Il \_ \_ flag positivo mappa cubi DDS, definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi \_ positivo.</span><span class="sxs-lookup"><span data-stu-id="8f40d-223">The DDS\_CUBEMAP\_POSITIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEY flags.</span></span>

<span data-ttu-id="8f40d-224">Il \_ flag mappa cubi \_ , che è definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi \_ negative.</span><span class="sxs-lookup"><span data-stu-id="8f40d-224">The DDS\_CUBEMAP\_NEGATIVEY flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEY flags.</span></span>

<span data-ttu-id="8f40d-225">Il \_ flag DDS mappa cubi \_ POSITIVEZ, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi POSITIVEZ \_ .</span><span class="sxs-lookup"><span data-stu-id="8f40d-225">The DDS\_CUBEMAP\_POSITIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_POSITIVEZ flags.</span></span>

<span data-ttu-id="8f40d-226">Il \_ flag DDS mappa cubi \_ NEGATIVEZ, definito in DDS. h, è una combinazione bit per bit dei \_ flag DDSCAPS2 mappa cubi e DDSCAPS2 \_ mappa cubi NEGATIVEZ \_ .</span><span class="sxs-lookup"><span data-stu-id="8f40d-226">The DDS\_CUBEMAP\_NEGATIVEZ flag, which is defined in Dds.h, is a bitwise-OR combination of the DDSCAPS2\_CUBEMAP and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="8f40d-227">Il \_ flag DDS mappa cubi \_ ALLFACES, definito in DDS. h, è una combinazione OR bit per bit dei \_ flag DDS mappa cubi \_ POSITIVEX, DDS \_ mappa cubi \_ NEGATIVEX, DDS \_ mappa cubi \_ positivey, DDS \_ mappa cubi \_ negative, DDS \_ mappa cubi \_ POSITIVEZ e \_ \_ DDSCAPS2 mappa cubi NEGATIVEZ.</span><span class="sxs-lookup"><span data-stu-id="8f40d-227">The DDS\_CUBEMAP\_ALLFACES flag, which is defined in Dds.h, is a bitwise-OR combination of the DDS\_CUBEMAP\_POSITIVEX, DDS\_CUBEMAP\_NEGATIVEX, DDS\_CUBEMAP\_POSITIVEY, DDS\_CUBEMAP\_NEGATIVEY, DDS\_CUBEMAP\_POSITIVEZ, and DDSCAPS2\_CUBEMAP\_NEGATIVEZ flags.</span></span>

<span data-ttu-id="8f40d-228">Il flag del \_ volume dei flag DDS \_ , definito in DDS. h, è uguale al flag del \_ volume DDSCAPS2.</span><span class="sxs-lookup"><span data-stu-id="8f40d-228">The DDS\_FLAGS\_VOLUME flag, which is defined in Dds.h, is equal to the DDSCAPS2\_VOLUME flag.</span></span>

> [!Note]  
> <span data-ttu-id="8f40d-229">Sebbene Direct3D 9 supporti le mappe di cubi parziali, Direct3D 10, 10,1 e 11 richiedono la definizione di tutti e sei i visi della mappa cubo, ovvero è necessario impostare DDS \_ mappa cubi \_ ALLFACES.</span><span class="sxs-lookup"><span data-stu-id="8f40d-229">Although Direct3D 9 supports partial cube-maps, Direct3D 10, 10.1, and 11 require that you define all six cube-map faces (that is, you must set DDS\_CUBEMAP\_ALLFACES).</span></span>

 

</dd> <dt>

<span data-ttu-id="8f40d-230">**dwCaps3**</span><span class="sxs-lookup"><span data-stu-id="8f40d-230">**dwCaps3**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-231">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-231">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-232">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8f40d-232">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-233">**dwCaps4**</span><span class="sxs-lookup"><span data-stu-id="8f40d-233">**dwCaps4**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-234">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-234">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-235">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8f40d-235">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8f40d-236">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="8f40d-236">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="8f40d-237">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8f40d-237">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8f40d-238">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8f40d-238">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f40d-239">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f40d-239">Remarks</span></span>

<span data-ttu-id="8f40d-240">Includere i flag in **dwFlags** per i membri della struttura che contengono dati validi.</span><span class="sxs-lookup"><span data-stu-id="8f40d-240">Include flags in **dwFlags** for the members of the structure that contain valid data.</span></span>

<span data-ttu-id="8f40d-241">Usare questa struttura insieme a un' [**intestazione DDS \_ \_ DXT10**](dds-header-dxt10.md) per archiviare una matrice di risorse in un file DDS.</span><span class="sxs-lookup"><span data-stu-id="8f40d-241">Use this structure in combination with a [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) to store a resource array in a DDS file.</span></span> <span data-ttu-id="8f40d-242">Per altre informazioni, vedere [matrici di trame](dx-graphics-dds-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="8f40d-242">For more information, see [texture arrays](dx-graphics-dds-pguide.md).</span></span>

<span data-ttu-id="8f40d-243">**DDS \_ L'intestazione** è identica alla struttura DDSURFACEDESC2 di DirectDraw senza dipendenze di DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="8f40d-243">**DDS\_HEADER** is identical to the DirectDraw DDSURFACEDESC2 structure without DirectDraw dependencies.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f40d-244">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f40d-244">Requirements</span></span>



| <span data-ttu-id="8f40d-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f40d-245">Requirement</span></span> | <span data-ttu-id="8f40d-246">Valore</span><span class="sxs-lookup"><span data-stu-id="8f40d-246">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8f40d-247">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f40d-247">Header</span></span><br/> | <dl> <span data-ttu-id="8f40d-248"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f40d-248"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f40d-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f40d-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f40d-250">Informazioni di riferimento per DDS</span><span class="sxs-lookup"><span data-stu-id="8f40d-250">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

