---
title: Esempio di trama DDS
description: Per una trama non compressa, usare i \_ flag DDSD pitch e DDPF \_ RGB. per una trama compressa, usare i \_ flag DDSD LINEARSIZE e DDPF \_ fourcc.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298364"
---
# <a name="dds-texture-example"></a><span data-ttu-id="59e20-103">Esempio di trama DDS</span><span class="sxs-lookup"><span data-stu-id="59e20-103">DDS Texture Example</span></span>

<span data-ttu-id="59e20-104">Per una trama non compressa, usare i \_ flag DDSD pitch e DDPF \_ RGB. per una trama compressa, usare i \_ flag DDSD LINEARSIZE e DDPF \_ fourcc.</span><span class="sxs-lookup"><span data-stu-id="59e20-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="59e20-105">Per una trama mipmap, usare i \_ flag complessi DDSD MIPMAPCOUNT, ddsCaps \_ MIPMAP e ddsCaps, oltre \_ al membro MIPMAP Count.</span><span class="sxs-lookup"><span data-stu-id="59e20-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="59e20-106">Se vengono generati mipmap, tutti i livelli fino a 1 per 1 vengono in genere scritti.</span><span class="sxs-lookup"><span data-stu-id="59e20-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="59e20-107">Per una trama compressa, le dimensioni di ogni immagine a livello di mipmap sono in genere pari a un quarto della dimensione precedente, con un minimo di 8 (DXT1) o 16 (DXT2-5) byte (per le trame quadre).</span><span class="sxs-lookup"><span data-stu-id="59e20-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="59e20-108">Utilizzare la formula seguente per calcolare le dimensioni di ogni livello per una trama non quadrata:</span><span class="sxs-lookup"><span data-stu-id="59e20-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="59e20-109">Questa tabella elenca la quantità di spazio occupata da ogni livello per una trama R8G8B8 256 per 256, senza usare la compressione.</span><span class="sxs-lookup"><span data-stu-id="59e20-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="59e20-110">Componenti DDS</span><span class="sxs-lookup"><span data-stu-id="59e20-110">DDS Components</span></span>          | <span data-ttu-id="59e20-111">\# Byte</span><span class="sxs-lookup"><span data-stu-id="59e20-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="59e20-112">header</span><span class="sxs-lookup"><span data-stu-id="59e20-112">header</span></span>                  | <span data-ttu-id="59e20-113">128</span><span class="sxs-lookup"><span data-stu-id="59e20-113">128</span></span>      |
| <span data-ttu-id="59e20-114">immagine principale 256 per 256</span><span class="sxs-lookup"><span data-stu-id="59e20-114">256-by-256 main image</span></span>   | <span data-ttu-id="59e20-115">196608</span><span class="sxs-lookup"><span data-stu-id="59e20-115">196608</span></span>   |
| <span data-ttu-id="59e20-116">immagine mipmap 128 per 128</span><span class="sxs-lookup"><span data-stu-id="59e20-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="59e20-117">49152</span><span class="sxs-lookup"><span data-stu-id="59e20-117">49152</span></span>    |
| <span data-ttu-id="59e20-118">immagine mipmap 64 per 64</span><span class="sxs-lookup"><span data-stu-id="59e20-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="59e20-119">12288</span><span class="sxs-lookup"><span data-stu-id="59e20-119">12288</span></span>    |
| <span data-ttu-id="59e20-120">immagine mipmap 32 per 32</span><span class="sxs-lookup"><span data-stu-id="59e20-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="59e20-121">3072</span><span class="sxs-lookup"><span data-stu-id="59e20-121">3072</span></span>     |
| <span data-ttu-id="59e20-122">immagine mipmap 16 per 16</span><span class="sxs-lookup"><span data-stu-id="59e20-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="59e20-123">768</span><span class="sxs-lookup"><span data-stu-id="59e20-123">768</span></span>      |
| <span data-ttu-id="59e20-124">immagine mipmap 8 per 8</span><span class="sxs-lookup"><span data-stu-id="59e20-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="59e20-125">192</span><span class="sxs-lookup"><span data-stu-id="59e20-125">192</span></span>      |
| <span data-ttu-id="59e20-126">immagine mipmap 4 per 4</span><span class="sxs-lookup"><span data-stu-id="59e20-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="59e20-127">48</span><span class="sxs-lookup"><span data-stu-id="59e20-127">48</span></span>       |
| <span data-ttu-id="59e20-128">immagine mipmap 2 per 2</span><span class="sxs-lookup"><span data-stu-id="59e20-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="59e20-129">12</span><span class="sxs-lookup"><span data-stu-id="59e20-129">12</span></span>       |
| <span data-ttu-id="59e20-130">immagine mipmap 1 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="59e20-131">3</span><span class="sxs-lookup"><span data-stu-id="59e20-131">3</span></span>        |



 

<span data-ttu-id="59e20-132">Questa tabella elenca la quantità di spazio occupata da ogni livello per la stessa trama usando la compressione (DXT1).</span><span class="sxs-lookup"><span data-stu-id="59e20-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="59e20-133">Componenti DDS</span><span class="sxs-lookup"><span data-stu-id="59e20-133">DDS Components</span></span>         | <span data-ttu-id="59e20-134">\# Byte</span><span class="sxs-lookup"><span data-stu-id="59e20-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="59e20-135">header</span><span class="sxs-lookup"><span data-stu-id="59e20-135">header</span></span>                 | <span data-ttu-id="59e20-136">128</span><span class="sxs-lookup"><span data-stu-id="59e20-136">128</span></span>      |
| <span data-ttu-id="59e20-137">immagine principale 256 per 64</span><span class="sxs-lookup"><span data-stu-id="59e20-137">256-by-64 main image</span></span>   | <span data-ttu-id="59e20-138">8192</span><span class="sxs-lookup"><span data-stu-id="59e20-138">8192</span></span>     |
| <span data-ttu-id="59e20-139">immagine mipmap 128 per 32</span><span class="sxs-lookup"><span data-stu-id="59e20-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="59e20-140">2048</span><span class="sxs-lookup"><span data-stu-id="59e20-140">2048</span></span>     |
| <span data-ttu-id="59e20-141">immagine mipmap 64 per 16</span><span class="sxs-lookup"><span data-stu-id="59e20-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="59e20-142">512</span><span class="sxs-lookup"><span data-stu-id="59e20-142">512</span></span>      |
| <span data-ttu-id="59e20-143">immagine mipmap 32 per 8</span><span class="sxs-lookup"><span data-stu-id="59e20-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="59e20-144">128</span><span class="sxs-lookup"><span data-stu-id="59e20-144">128</span></span>      |
| <span data-ttu-id="59e20-145">immagine mipmap 16 per 4</span><span class="sxs-lookup"><span data-stu-id="59e20-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="59e20-146">32</span><span class="sxs-lookup"><span data-stu-id="59e20-146">32</span></span>       |
| <span data-ttu-id="59e20-147">immagine mipmap 8 per 2</span><span class="sxs-lookup"><span data-stu-id="59e20-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="59e20-148">16</span><span class="sxs-lookup"><span data-stu-id="59e20-148">16</span></span>       |
| <span data-ttu-id="59e20-149">immagine di mipmap 4 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="59e20-150">8</span><span class="sxs-lookup"><span data-stu-id="59e20-150">8</span></span>        |
| <span data-ttu-id="59e20-151">immagine mipmap 2 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="59e20-152">8</span><span class="sxs-lookup"><span data-stu-id="59e20-152">8</span></span>        |
| <span data-ttu-id="59e20-153">immagine mipmap 1 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="59e20-154">8</span><span class="sxs-lookup"><span data-stu-id="59e20-154">8</span></span>        |



 

<span data-ttu-id="59e20-155">Questa tabella elenca la quantità di spazio occupata da ogni livello per la stessa trama usando un formato di compressione DXGI (in questo caso BC3 \_ UNORM) che richiede pertanto l'intestazione estesa:</span><span class="sxs-lookup"><span data-stu-id="59e20-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="59e20-156">Componenti DDS</span><span class="sxs-lookup"><span data-stu-id="59e20-156">DDS Components</span></span>                                                | <span data-ttu-id="59e20-157">\# Byte</span><span class="sxs-lookup"><span data-stu-id="59e20-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="59e20-158">Header (FourCC impostato su "DX10")</span><span class="sxs-lookup"><span data-stu-id="59e20-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="59e20-159">128</span><span class="sxs-lookup"><span data-stu-id="59e20-159">128</span></span>      |
| <span data-ttu-id="59e20-160">intestazione estesa (formato DXGI impostato sul \_ formato DXGI \_ BC3 \_ UNORM)</span><span class="sxs-lookup"><span data-stu-id="59e20-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="59e20-161">20</span><span class="sxs-lookup"><span data-stu-id="59e20-161">20</span></span>       |
| <span data-ttu-id="59e20-162">immagine principale 256 per 64</span><span class="sxs-lookup"><span data-stu-id="59e20-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="59e20-163">16384</span><span class="sxs-lookup"><span data-stu-id="59e20-163">16384</span></span>    |
| <span data-ttu-id="59e20-164">immagine mipmap 128 per 32</span><span class="sxs-lookup"><span data-stu-id="59e20-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="59e20-165">4096</span><span class="sxs-lookup"><span data-stu-id="59e20-165">4096</span></span>     |
| <span data-ttu-id="59e20-166">immagine mipmap 64 per 16</span><span class="sxs-lookup"><span data-stu-id="59e20-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="59e20-167">1024</span><span class="sxs-lookup"><span data-stu-id="59e20-167">1024</span></span>     |
| <span data-ttu-id="59e20-168">immagine mipmap 32 per 8</span><span class="sxs-lookup"><span data-stu-id="59e20-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="59e20-169">256</span><span class="sxs-lookup"><span data-stu-id="59e20-169">256</span></span>      |
| <span data-ttu-id="59e20-170">immagine mipmap 16 per 4</span><span class="sxs-lookup"><span data-stu-id="59e20-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="59e20-171">64</span><span class="sxs-lookup"><span data-stu-id="59e20-171">64</span></span>       |
| <span data-ttu-id="59e20-172">immagine mipmap 8 per 2</span><span class="sxs-lookup"><span data-stu-id="59e20-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="59e20-173">32</span><span class="sxs-lookup"><span data-stu-id="59e20-173">32</span></span>       |
| <span data-ttu-id="59e20-174">immagine di mipmap 4 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="59e20-175">16</span><span class="sxs-lookup"><span data-stu-id="59e20-175">16</span></span>       |
| <span data-ttu-id="59e20-176">immagine mipmap 2 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="59e20-177">16</span><span class="sxs-lookup"><span data-stu-id="59e20-177">16</span></span>       |
| <span data-ttu-id="59e20-178">immagine mipmap 1 per 1</span><span class="sxs-lookup"><span data-stu-id="59e20-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="59e20-179">16</span><span class="sxs-lookup"><span data-stu-id="59e20-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="59e20-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59e20-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e20-181">Guida alla programmazione per DDS</span><span class="sxs-lookup"><span data-stu-id="59e20-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




