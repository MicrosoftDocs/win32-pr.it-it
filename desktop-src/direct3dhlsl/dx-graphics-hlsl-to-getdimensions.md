---
title: GetDimensions (oggetto Texture HLSL DirectX)
description: Ottiene informazioni sulle dimensioni della trama. Il blocco di sintassi mostra tutti i parametri possibili nella dichiarazione del metodo. La tabella nella sezione Osservazioni mostra i parametri implementati per ogni tipo di oggetto trama.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119837"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="8d6b3-105">GetDimensions (oggetto Texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="8d6b3-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="8d6b3-106">Ottiene informazioni sulle dimensioni della trama.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-106">Gets texture size information.</span></span> <span data-ttu-id="8d6b3-107">Il blocco di sintassi mostra tutti i parametri possibili nella dichiarazione del metodo.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="8d6b3-108">La tabella nella sezione Osservazioni mostra i parametri implementati per ogni tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>

<span data-ttu-id="8d6b3-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span><span class="sxs-lookup"><span data-stu-id="8d6b3-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span>



 

<span data-ttu-id="8d6b3-110">typeX indica che esistono due tipi possibili: **uint** o **float.**</span><span class="sxs-lookup"><span data-stu-id="8d6b3-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d6b3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d6b3-111">Parameters</span></span>



| <span data-ttu-id="8d6b3-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="8d6b3-112">Item</span></span>                                                                                                                               | <span data-ttu-id="8d6b3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d6b3-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d6b3-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="8d6b3-115">Qualsiasi [tipo di oggetto trama](dx-graphics-hlsl-to-type.md) ad eccezione di un oggetto **Buffer.**</span><span class="sxs-lookup"><span data-stu-id="8d6b3-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="8d6b3-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="8d6b3-117">\[in \] Un indice in base zero che identifica il livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="8d6b3-118">Se questo argomento non viene usato, viene usato il primo livello mip.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="8d6b3-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="8d6b3-120">\[out \] Larghezza della trama, in texel.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="8d6b3-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Altezza*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="8d6b3-122">\[out \] Altezza della trama, in texel.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="8d6b3-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementi*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="8d6b3-124">\[out \] Numero di elementi in una matrice.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="8d6b3-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondità*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="8d6b3-126">\[out \] Profondità della trama, in texel.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="8d6b3-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="8d6b3-128">\[out \] Numero di livelli mipmap.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="8d6b3-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="8d6b3-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="8d6b3-130">\[out \] Numero di campioni.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="8d6b3-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d6b3-131">Return Value</span></span>

<span data-ttu-id="8d6b3-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8d6b3-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="8d6b3-133">Metodi di overload</span><span class="sxs-lookup"><span data-stu-id="8d6b3-133">Overloaded Methods</span></span>

<span data-ttu-id="8d6b3-134">In questa tabella sono elencate tutte le diverse versioni del metodo . le versioni differiscono per il numero di parametri di input.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="8d6b3-135">Si noti che per ogni metodo che accetta parametri integer, esiste un metodo di overload che accetta parametri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="8d6b3-136">tipo Texture-Object</span><span class="sxs-lookup"><span data-stu-id="8d6b3-136">Texture-Object Type</span></span> | <span data-ttu-id="8d6b3-137">Parametri di input</span><span class="sxs-lookup"><span data-stu-id="8d6b3-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8d6b3-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-138">Texture1D</span></span>           | <span data-ttu-id="8d6b3-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="8d6b3-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-140">Texture1D</span></span>           | <span data-ttu-id="8d6b3-141">Larghezza UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="8d6b3-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-142">Texture1D</span></span>           | <span data-ttu-id="8d6b3-143">UINT MipLevel, float Width, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="8d6b3-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-144">Texture1D</span></span>           | <span data-ttu-id="8d6b3-145">Float Width</span><span class="sxs-lookup"><span data-stu-id="8d6b3-145">float Width</span></span>                                                                    |
| <span data-ttu-id="8d6b3-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-146">Texture1DArray</span></span>      | <span data-ttu-id="8d6b3-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="8d6b3-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-148">Texture1DArray</span></span>      | <span data-ttu-id="8d6b3-149">Larghezza UINT, elementi UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="8d6b3-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-150">Texture1DArray</span></span>      | <span data-ttu-id="8d6b3-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="8d6b3-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-152">Texture1DArray</span></span>      | <span data-ttu-id="8d6b3-153">float Width, float Elements</span><span class="sxs-lookup"><span data-stu-id="8d6b3-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="8d6b3-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-154">Texture2D</span></span>           | <span data-ttu-id="8d6b3-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="8d6b3-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-156">Texture2D</span></span>           | <span data-ttu-id="8d6b3-157">Larghezza UINT, Altezza UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="8d6b3-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-158">Texture2D</span></span>           | <span data-ttu-id="8d6b3-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="8d6b3-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-160">Texture2D</span></span>           | <span data-ttu-id="8d6b3-161">float Width, float Height</span><span class="sxs-lookup"><span data-stu-id="8d6b3-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="8d6b3-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-162">Texture2DArray</span></span>      | <span data-ttu-id="8d6b3-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="8d6b3-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-164">Texture2DArray</span></span>      | <span data-ttu-id="8d6b3-165">Larghezza UINT, Altezza UINT, Elementi UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="8d6b3-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-166">Texture2DArray</span></span>      | <span data-ttu-id="8d6b3-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="8d6b3-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-168">Texture2DArray</span></span>      | <span data-ttu-id="8d6b3-169">Float Width, float Height, float Elements</span><span class="sxs-lookup"><span data-stu-id="8d6b3-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="8d6b3-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-170">Texture3D</span></span>           | <span data-ttu-id="8d6b3-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="8d6b3-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-172">Texture3D</span></span>           | <span data-ttu-id="8d6b3-173">Larghezza UINT, Altezza UINT, Profondità UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="8d6b3-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-174">Texture3D</span></span>           | <span data-ttu-id="8d6b3-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="8d6b3-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8d6b3-176">Texture3D</span></span>           | <span data-ttu-id="8d6b3-177">float Width, float Height, float Depth</span><span class="sxs-lookup"><span data-stu-id="8d6b3-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="8d6b3-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="8d6b3-178">TextureCube</span></span>         | <span data-ttu-id="8d6b3-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="8d6b3-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="8d6b3-180">TextureCube</span></span>         | <span data-ttu-id="8d6b3-181">Larghezza UINT, Altezza UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="8d6b3-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="8d6b3-182">TextureCube</span></span>         | <span data-ttu-id="8d6b3-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="8d6b3-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="8d6b3-184">TextureCube</span></span>         | <span data-ttu-id="8d6b3-185">float Width, float Height</span><span class="sxs-lookup"><span data-stu-id="8d6b3-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="8d6b3-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-186">TextureCubeArray</span></span>    | <span data-ttu-id="8d6b3-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="8d6b3-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-188">TextureCubeArray</span></span>    | <span data-ttu-id="8d6b3-189">Larghezza UINT, Altezza UINT, Elementi UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="8d6b3-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-190">TextureCubeArray</span></span>    | <span data-ttu-id="8d6b3-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="8d6b3-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="8d6b3-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-192">TextureCubeArray</span></span>    | <span data-ttu-id="8d6b3-193">Float Width, float Height, float Elements</span><span class="sxs-lookup"><span data-stu-id="8d6b3-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="8d6b3-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="8d6b3-194">Texture2DMS</span></span>         | <span data-ttu-id="8d6b3-195">Esempi di UINT Width, UINT Height, UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="8d6b3-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="8d6b3-196">Texture2DMS</span></span>         | <span data-ttu-id="8d6b3-197">Esempi di float Width, float Height, float</span><span class="sxs-lookup"><span data-stu-id="8d6b3-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="8d6b3-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-198">Texture2DMSArray</span></span>    | <span data-ttu-id="8d6b3-199">Larghezza UINT, Altezza UINT, Elementi UINT, Esempi UINT</span><span class="sxs-lookup"><span data-stu-id="8d6b3-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="8d6b3-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8d6b3-200">Texture2DMSArray</span></span>    | <span data-ttu-id="8d6b3-201">Float Width, float Height, float Elements, float Samples</span><span class="sxs-lookup"><span data-stu-id="8d6b3-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d6b3-202">Modello shader minimo</span><span class="sxs-lookup"><span data-stu-id="8d6b3-202">Minimum Shader Model</span></span>

<span data-ttu-id="8d6b3-203">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8d6b3-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d6b3-204">vs\_4\_0</span></span> | <span data-ttu-id="8d6b3-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8d6b3-205">vs\_4\_1</span></span>  | <span data-ttu-id="8d6b3-206">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d6b3-206">ps\_4\_0</span></span> | <span data-ttu-id="8d6b3-207">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8d6b3-207">ps\_4\_1</span></span>  | <span data-ttu-id="8d6b3-208">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d6b3-208">gs\_4\_0</span></span> | <span data-ttu-id="8d6b3-209">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8d6b3-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="8d6b3-210">x</span><span class="sxs-lookup"><span data-stu-id="8d6b3-210">x</span></span>        | <span data-ttu-id="8d6b3-211">x</span><span class="sxs-lookup"><span data-stu-id="8d6b3-211">x</span></span>         | <span data-ttu-id="8d6b3-212">x</span><span class="sxs-lookup"><span data-stu-id="8d6b3-212">x</span></span>        | <span data-ttu-id="8d6b3-213">x</span><span class="sxs-lookup"><span data-stu-id="8d6b3-213">x</span></span>         | <span data-ttu-id="8d6b3-214">x</span><span class="sxs-lookup"><span data-stu-id="8d6b3-214">x</span></span>        | <span data-ttu-id="8d6b3-215">x</span><span class="sxs-lookup"><span data-stu-id="8d6b3-215">x</span></span>         |



 

1.  <span data-ttu-id="8d6b3-216">Restituisce le dimensioni per il livello mipmap più grande (zero).</span><span class="sxs-lookup"><span data-stu-id="8d6b3-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="8d6b3-217">TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="8d6b3-218">Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8d6b3-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d6b3-219">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d6b3-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d6b3-220">Oggetto texture</span><span class="sxs-lookup"><span data-stu-id="8d6b3-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





