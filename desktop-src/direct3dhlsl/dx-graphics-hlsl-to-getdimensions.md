---
title: GetDimensions (oggetto trama DirectX HLSL)
description: Ottiene le informazioni sulle dimensioni della trama. Il blocco Syntax Mostra tutti i parametri possibili nella dichiarazione di metodo. La tabella nella sezione Osservazioni Mostra i parametri implementati per ogni tipo di oggetto trama.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857762"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="892dd-105">GetDimensions (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="892dd-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="892dd-106">Ottiene le informazioni sulle dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="892dd-106">Gets texture size information.</span></span> <span data-ttu-id="892dd-107">Il blocco Syntax Mostra tutti i parametri possibili nella dichiarazione di metodo.</span><span class="sxs-lookup"><span data-stu-id="892dd-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="892dd-108">La tabella nella sezione Osservazioni Mostra i parametri implementati per ogni tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="892dd-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892dd-109">void Object. GetDimensions (UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples);</span><span class="sxs-lookup"><span data-stu-id="892dd-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="892dd-110">typeX indica che esistono due tipi possibili: **uint** o **float**.</span><span class="sxs-lookup"><span data-stu-id="892dd-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="892dd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="892dd-111">Parameters</span></span>



| <span data-ttu-id="892dd-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="892dd-112">Item</span></span>                                                                                                                               | <span data-ttu-id="892dd-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="892dd-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892dd-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*</span><span class="sxs-lookup"><span data-stu-id="892dd-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="892dd-115">Qualsiasi tipo [di oggetto trama](dx-graphics-hlsl-to-type.md) ad eccezione di un oggetto **buffer** .</span><span class="sxs-lookup"><span data-stu-id="892dd-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="892dd-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="892dd-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="892dd-117">\[in \] un indice in base zero che identifica il livello di mipmap.</span><span class="sxs-lookup"><span data-stu-id="892dd-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="892dd-118">Se questo argomento non viene utilizzato, si presuppone il primo livello MIP.</span><span class="sxs-lookup"><span data-stu-id="892dd-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="892dd-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="892dd-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="892dd-120">\[\]larghezza della trama, in Texel.</span><span class="sxs-lookup"><span data-stu-id="892dd-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="892dd-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Altezza*</span><span class="sxs-lookup"><span data-stu-id="892dd-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="892dd-122">\[\]altezza della trama, in Texel.</span><span class="sxs-lookup"><span data-stu-id="892dd-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="892dd-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementi*</span><span class="sxs-lookup"><span data-stu-id="892dd-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="892dd-124">\[\]numero di elementi in una matrice.</span><span class="sxs-lookup"><span data-stu-id="892dd-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="892dd-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondità*</span><span class="sxs-lookup"><span data-stu-id="892dd-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="892dd-126">\[\]profondità della trama, in Texel.</span><span class="sxs-lookup"><span data-stu-id="892dd-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="892dd-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="892dd-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="892dd-128">\[\]il numero di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="892dd-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="892dd-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="892dd-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="892dd-130">\[\]numero di campioni.</span><span class="sxs-lookup"><span data-stu-id="892dd-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="892dd-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="892dd-131">Return Value</span></span>

<span data-ttu-id="892dd-132">nessuno</span><span class="sxs-lookup"><span data-stu-id="892dd-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="892dd-133">Metodi di overload</span><span class="sxs-lookup"><span data-stu-id="892dd-133">Overloaded Methods</span></span>

<span data-ttu-id="892dd-134">In questa tabella sono elencate tutte le diverse versioni del metodo. le versioni variano in base al numero di parametri di input.</span><span class="sxs-lookup"><span data-stu-id="892dd-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="892dd-135">Si noti che per ogni metodo che accetta parametri Integer esiste un metodo di overload che accetta parametri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="892dd-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="892dd-136">Tipo di Texture-Object</span><span class="sxs-lookup"><span data-stu-id="892dd-136">Texture-Object Type</span></span> | <span data-ttu-id="892dd-137">Parametri di input</span><span class="sxs-lookup"><span data-stu-id="892dd-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="892dd-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="892dd-138">Texture1D</span></span>           | <span data-ttu-id="892dd-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="892dd-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="892dd-140">Texture1D</span></span>           | <span data-ttu-id="892dd-141">Lunghezza UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="892dd-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="892dd-142">Texture1D</span></span>           | <span data-ttu-id="892dd-143">UINT MipLevel, float width, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="892dd-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="892dd-144">Texture1D</span></span>           | <span data-ttu-id="892dd-145">Larghezza float</span><span class="sxs-lookup"><span data-stu-id="892dd-145">float Width</span></span>                                                                    |
| <span data-ttu-id="892dd-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-146">Texture1DArray</span></span>      | <span data-ttu-id="892dd-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="892dd-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-148">Texture1DArray</span></span>      | <span data-ttu-id="892dd-149">Lunghezza UINT, elementi UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="892dd-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-150">Texture1DArray</span></span>      | <span data-ttu-id="892dd-151">UINT MipLevel, float width, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="892dd-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-152">Texture1DArray</span></span>      | <span data-ttu-id="892dd-153">float width, float Elements</span><span class="sxs-lookup"><span data-stu-id="892dd-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="892dd-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="892dd-154">Texture2D</span></span>           | <span data-ttu-id="892dd-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="892dd-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="892dd-156">Texture2D</span></span>           | <span data-ttu-id="892dd-157">Lunghezza UINT, altezza UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="892dd-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="892dd-158">Texture2D</span></span>           | <span data-ttu-id="892dd-159">UINT MipLevel, float width, float height, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="892dd-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="892dd-160">Texture2D</span></span>           | <span data-ttu-id="892dd-161">Larghezza float, altezza float</span><span class="sxs-lookup"><span data-stu-id="892dd-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="892dd-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-162">Texture2DArray</span></span>      | <span data-ttu-id="892dd-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="892dd-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-164">Texture2DArray</span></span>      | <span data-ttu-id="892dd-165">Lunghezza UINT, altezza UINT, elementi UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="892dd-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-166">Texture2DArray</span></span>      | <span data-ttu-id="892dd-167">UINT MipLevel, float width, float height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="892dd-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="892dd-168">Texture2DArray</span></span>      | <span data-ttu-id="892dd-169">Spessore float, altezza float, elementi float</span><span class="sxs-lookup"><span data-stu-id="892dd-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="892dd-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="892dd-170">Texture3D</span></span>           | <span data-ttu-id="892dd-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="892dd-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="892dd-172">Texture3D</span></span>           | <span data-ttu-id="892dd-173">Lunghezza UINT, altezza UINT, profondità UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="892dd-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="892dd-174">Texture3D</span></span>           | <span data-ttu-id="892dd-175">UINT MipLevel, float width, float height, float Depth, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="892dd-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="892dd-176">Texture3D</span></span>           | <span data-ttu-id="892dd-177">Larghezza float, altezza float, profondità a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="892dd-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="892dd-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="892dd-178">TextureCube</span></span>         | <span data-ttu-id="892dd-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="892dd-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="892dd-180">TextureCube</span></span>         | <span data-ttu-id="892dd-181">Lunghezza UINT, altezza UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="892dd-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="892dd-182">TextureCube</span></span>         | <span data-ttu-id="892dd-183">UINT MipLevel, float width, float height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="892dd-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="892dd-184">TextureCube</span></span>         | <span data-ttu-id="892dd-185">Larghezza float, altezza float</span><span class="sxs-lookup"><span data-stu-id="892dd-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="892dd-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="892dd-186">TextureCubeArray</span></span>    | <span data-ttu-id="892dd-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="892dd-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="892dd-188">TextureCubeArray</span></span>    | <span data-ttu-id="892dd-189">Lunghezza UINT, altezza UINT, elementi UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="892dd-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="892dd-190">TextureCubeArray</span></span>    | <span data-ttu-id="892dd-191">UINT MipLevel, float width, float height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="892dd-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="892dd-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="892dd-192">TextureCubeArray</span></span>    | <span data-ttu-id="892dd-193">Spessore float, altezza float, elementi float</span><span class="sxs-lookup"><span data-stu-id="892dd-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="892dd-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="892dd-194">Texture2DMS</span></span>         | <span data-ttu-id="892dd-195">UINT Width, UINT Height, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="892dd-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="892dd-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="892dd-196">Texture2DMS</span></span>         | <span data-ttu-id="892dd-197">float width, float height, float Samples</span><span class="sxs-lookup"><span data-stu-id="892dd-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="892dd-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="892dd-198">Texture2DMSArray</span></span>    | <span data-ttu-id="892dd-199">Lunghezza UINT, altezza UINT, elementi UINT, esempi UINT</span><span class="sxs-lookup"><span data-stu-id="892dd-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="892dd-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="892dd-200">Texture2DMSArray</span></span>    | <span data-ttu-id="892dd-201">float width, float height, float Elements, float Samples</span><span class="sxs-lookup"><span data-stu-id="892dd-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="892dd-202">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="892dd-202">Minimum Shader Model</span></span>

<span data-ttu-id="892dd-203">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="892dd-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="892dd-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="892dd-204">vs\_4\_0</span></span> | <span data-ttu-id="892dd-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="892dd-205">vs\_4\_1</span></span>  | <span data-ttu-id="892dd-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="892dd-206">ps\_4\_0</span></span> | <span data-ttu-id="892dd-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="892dd-207">ps\_4\_1</span></span>  | <span data-ttu-id="892dd-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="892dd-208">gs\_4\_0</span></span> | <span data-ttu-id="892dd-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="892dd-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="892dd-210">x</span><span class="sxs-lookup"><span data-stu-id="892dd-210">x</span></span>        | <span data-ttu-id="892dd-211">x</span><span class="sxs-lookup"><span data-stu-id="892dd-211">x</span></span>         | <span data-ttu-id="892dd-212">x</span><span class="sxs-lookup"><span data-stu-id="892dd-212">x</span></span>        | <span data-ttu-id="892dd-213">x</span><span class="sxs-lookup"><span data-stu-id="892dd-213">x</span></span>         | <span data-ttu-id="892dd-214">x</span><span class="sxs-lookup"><span data-stu-id="892dd-214">x</span></span>        | <span data-ttu-id="892dd-215">x</span><span class="sxs-lookup"><span data-stu-id="892dd-215">x</span></span>         |



 

1.  <span data-ttu-id="892dd-216">Restituisce le dimensioni per il livello mipmap più grande (zero).</span><span class="sxs-lookup"><span data-stu-id="892dd-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="892dd-217">TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="892dd-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="892dd-218">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="892dd-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="892dd-219">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="892dd-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892dd-220">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="892dd-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





