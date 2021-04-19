---
title: Struttura DDS_PIXELFORMAT (DDS. h)
description: Formato pixel superficie.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- Struttura DDS_PIXELFORMAT DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322291"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="75b97-104">\_Struttura PIXELFORMAT PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="75b97-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="75b97-105">Formato pixel superficie.</span><span class="sxs-lookup"><span data-stu-id="75b97-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b97-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75b97-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="75b97-107">Members</span><span class="sxs-lookup"><span data-stu-id="75b97-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="75b97-108">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="75b97-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-109">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-110">Dimensioni della struttura; impostare su 32 (byte).</span><span class="sxs-lookup"><span data-stu-id="75b97-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="75b97-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="75b97-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-112">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-113">Valori che indicano il tipo di dati presenti sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="75b97-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="75b97-114">Flag</span><span class="sxs-lookup"><span data-stu-id="75b97-114">Flag</span></span>              | <span data-ttu-id="75b97-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75b97-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="75b97-116">Valore</span><span class="sxs-lookup"><span data-stu-id="75b97-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="75b97-117">\_ALPHAPIXELS DDPF</span><span class="sxs-lookup"><span data-stu-id="75b97-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="75b97-118">La trama contiene dati alfa; **dwRGBAlphaBitMask** contiene dati validi.</span><span class="sxs-lookup"><span data-stu-id="75b97-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="75b97-119">0x1</span><span class="sxs-lookup"><span data-stu-id="75b97-119">0x1</span></span>     |
| <span data-ttu-id="75b97-120">DDPF \_ alfa</span><span class="sxs-lookup"><span data-stu-id="75b97-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="75b97-121">Usato in alcuni file DDS meno recenti per il canale alfa solo dati non compressi (dwRGBBitCount contiene il canale alfa bitCount; dwABitMask contiene dati validi)</span><span class="sxs-lookup"><span data-stu-id="75b97-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="75b97-122">0x2</span><span class="sxs-lookup"><span data-stu-id="75b97-122">0x2</span></span>     |
| <span data-ttu-id="75b97-123">\_fourcc DDPF</span><span class="sxs-lookup"><span data-stu-id="75b97-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="75b97-124">La trama contiene dati RGB compressi; **dwFourCC** contiene dati validi.</span><span class="sxs-lookup"><span data-stu-id="75b97-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="75b97-125">0x4</span><span class="sxs-lookup"><span data-stu-id="75b97-125">0x4</span></span>     |
| <span data-ttu-id="75b97-126">DDPF \_ RGB</span><span class="sxs-lookup"><span data-stu-id="75b97-126">DDPF\_RGB</span></span>         | <span data-ttu-id="75b97-127">La trama contiene dati RGB non compressi; **dwRGBBitCount** e le maschere RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contengono dati validi.</span><span class="sxs-lookup"><span data-stu-id="75b97-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="75b97-128">0x40</span><span class="sxs-lookup"><span data-stu-id="75b97-128">0x40</span></span>    |
| <span data-ttu-id="75b97-129">\_YUV DDPF</span><span class="sxs-lookup"><span data-stu-id="75b97-129">DDPF\_YUV</span></span>         | <span data-ttu-id="75b97-130">Usato in alcuni file DDS precedenti per i dati non compressi YUV (dwRGBBitCount contiene il numero di bit YUV; dwRBitMask contiene la maschera Y, dwGBitMask contiene l'U mask, dwBBitMask contiene V mask)</span><span class="sxs-lookup"><span data-stu-id="75b97-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="75b97-131">0x200</span><span class="sxs-lookup"><span data-stu-id="75b97-131">0x200</span></span>   |
| <span data-ttu-id="75b97-132">\_luminanza DDPF</span><span class="sxs-lookup"><span data-stu-id="75b97-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="75b97-133">Usato in alcuni file DDS meno recenti per i dati non compressi del colore a canale singolo (dwRGBBitCount contiene il numero di bit del canale di luminanza; dwRBitMask contiene la maschera del canale).</span><span class="sxs-lookup"><span data-stu-id="75b97-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="75b97-134">Può essere combinato con DDPF \_ ALPHAPIXELS per un file DDS con due canali.</span><span class="sxs-lookup"><span data-stu-id="75b97-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="75b97-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="75b97-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="75b97-136">**dwFourCC**</span><span class="sxs-lookup"><span data-stu-id="75b97-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-137">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-138">Codici di quattro caratteri per la specifica di formati compressi o personalizzati.</span><span class="sxs-lookup"><span data-stu-id="75b97-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="75b97-139">I valori possibili includono: *DXT1*, *DXT2*, *DXT3*, *DXT4* o *DXT5*.</span><span class="sxs-lookup"><span data-stu-id="75b97-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="75b97-140">Un FourCC di DX10 indica prescense dell'intestazione [**DDS \_ \_ DXT10**](dds-header-dxt10.md) intestazione estesa e il membro dxgiFormat di tale struttura indica il formato true.</span><span class="sxs-lookup"><span data-stu-id="75b97-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="75b97-141">Quando si utilizza un codice di quattro caratteri, dwFlags deve includere *DDPF \_ fourcc*.</span><span class="sxs-lookup"><span data-stu-id="75b97-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="75b97-142">**dwRGBBitCount**</span><span class="sxs-lookup"><span data-stu-id="75b97-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-143">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-144">Numero di bit in un formato RGB (possibilmente incluso Alpha).</span><span class="sxs-lookup"><span data-stu-id="75b97-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="75b97-145">Valido quando **dwFlags** include *DDPF \_ RGB*, *DDPF \_ Luminance* o *DDPF \_ YUV*.</span><span class="sxs-lookup"><span data-stu-id="75b97-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="75b97-146">**dwRBitMask**</span><span class="sxs-lookup"><span data-stu-id="75b97-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-147">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-148">Maschera rossa (o lumiannce o Y) per la lettura dei dati di colore.</span><span class="sxs-lookup"><span data-stu-id="75b97-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="75b97-149">Ad esempio, dato il formato A8R8G8B8, la maschera rossa è 0x00FF0000.</span><span class="sxs-lookup"><span data-stu-id="75b97-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="75b97-150">**dwGBitMask**</span><span class="sxs-lookup"><span data-stu-id="75b97-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-151">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-152">Maschera verde (o U) per la lettura dei dati di colore.</span><span class="sxs-lookup"><span data-stu-id="75b97-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="75b97-153">Ad esempio, dato il formato A8R8G8B8, la maschera verde è 0x0000ff00.</span><span class="sxs-lookup"><span data-stu-id="75b97-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="75b97-154">**dwBBitMask**</span><span class="sxs-lookup"><span data-stu-id="75b97-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-155">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-156">Maschera blu (o V) per la lettura dei dati di colore.</span><span class="sxs-lookup"><span data-stu-id="75b97-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="75b97-157">Ad esempio, dato il formato A8R8G8B8, la maschera blu è 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="75b97-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="75b97-158">**dwABitMask**</span><span class="sxs-lookup"><span data-stu-id="75b97-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="75b97-159">Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75b97-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="75b97-160">Maschera Alpha per la lettura di dati alfa.</span><span class="sxs-lookup"><span data-stu-id="75b97-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="75b97-161">dwFlags deve includere *DDPF \_ ALPHAPIXELS* o *DDPF \_ Alpha*.</span><span class="sxs-lookup"><span data-stu-id="75b97-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="75b97-162">Ad esempio, in base al formato A8R8G8B8, alpha mask è 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="75b97-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75b97-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="75b97-163">Remarks</span></span>

<span data-ttu-id="75b97-164">Per archiviare i formati DXGI, ad esempio i dati a virgola mobile, usare un **dwFlags** di DDPF \_ fourcc e impostare **dwFourCC** su',' X ',' 1',' 0'.</span><span class="sxs-lookup"><span data-stu-id="75b97-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="75b97-165">Usare l'intestazione [**DDS \_ header \_ DXT10**](dds-header-dxt10.md) Extension per archiviare il formato DXGI nel membro **dxgiFormat** .</span><span class="sxs-lookup"><span data-stu-id="75b97-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="75b97-166">Si noti che esistono varianti non standard dei file DDS in cui **dwFlags** ha DDPF \_ fourcc e il valore **dwFourCC** è impostato direttamente su un valore di enumerazione di formato D3DFORMAT o DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="75b97-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="75b97-167">Non è possibile evitare ambiguità tra i valori di formato D3DFORMAT e DXGI \_ usando questo schema non standard, quindi è invece consigliabile usare l'intestazione di estensione DX10.</span><span class="sxs-lookup"><span data-stu-id="75b97-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b97-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75b97-168">Requirements</span></span>



| <span data-ttu-id="75b97-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b97-169">Requirement</span></span> | <span data-ttu-id="75b97-170">Valore</span><span class="sxs-lookup"><span data-stu-id="75b97-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="75b97-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75b97-171">Header</span></span><br/> | <dl> <span data-ttu-id="75b97-172"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b97-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b97-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75b97-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b97-174">Informazioni di riferimento per DDS</span><span class="sxs-lookup"><span data-stu-id="75b97-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

