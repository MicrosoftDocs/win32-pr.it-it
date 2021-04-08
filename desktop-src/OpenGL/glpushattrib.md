---
title: funzione glPushAttrib (GL. h)
description: Inserisce lo stack dell'attributo.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- funzione glPushAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048047"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="34e81-104">glPushAttrib (funzione)</span><span class="sxs-lookup"><span data-stu-id="34e81-104">glPushAttrib function</span></span>

<span data-ttu-id="34e81-105">Inserisce lo stack dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="34e81-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e81-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34e81-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="34e81-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="34e81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e81-108">*maschera*</span><span class="sxs-lookup"><span data-stu-id="34e81-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="34e81-109">Maschera che indica gli attributi da salvare.</span><span class="sxs-lookup"><span data-stu-id="34e81-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="34e81-110">Le costanti di maschera simbolica e il relativo stato OpenGL associato sono le seguenti, ovvero l'elenco dei paragrafi rientrati in cui vengono salvati gli attributi:</span><span class="sxs-lookup"><span data-stu-id="34e81-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="34e81-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_bit del buffer di accut GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="34e81-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="34e81-112">Valore Clear buffer accumulo</span><span class="sxs-lookup"><span data-stu-id="34e81-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="34e81-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit del \_ buffer dei colori GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-114">\_Bit di \_ Abilitazione test GL Alpha</span><span class="sxs-lookup"><span data-stu-id="34e81-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="34e81-115">Funzione di test Alpha e valore di riferimento</span><span class="sxs-lookup"><span data-stu-id="34e81-115">Alpha test function and reference value</span></span>

<span data-ttu-id="34e81-116">\_Bit di abilitazione di Blend GL</span><span class="sxs-lookup"><span data-stu-id="34e81-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="34e81-117">Fusione di funzioni di origine e destinazione</span><span class="sxs-lookup"><span data-stu-id="34e81-117">Blending source and destination functions</span></span>

<span data-ttu-id="34e81-118">\_Bit di abilitazione dithering GL</span><span class="sxs-lookup"><span data-stu-id="34e81-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="34e81-119">Impostazione del buffer di \_ estrazione GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="34e81-120">\_Bit di \_ Abilitazione della logica GL</span><span class="sxs-lookup"><span data-stu-id="34e81-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="34e81-121">Funzione logica op</span><span class="sxs-lookup"><span data-stu-id="34e81-121">Logic op function</span></span>

<span data-ttu-id="34e81-122">Valori cancellati in modalità colore e indice</span><span class="sxs-lookup"><span data-stu-id="34e81-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="34e81-123">Writemasks modalità colore e indice</span><span class="sxs-lookup"><span data-stu-id="34e81-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="34e81-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_bit corrente \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-125">Colore RGBA corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-125">Current RGBA color</span></span>

<span data-ttu-id="34e81-126">Indice colori corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-126">Current color index</span></span>

<span data-ttu-id="34e81-127">Vettore normale corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-127">Current normal vector</span></span>

<span data-ttu-id="34e81-128">Coordinate di trama correnti</span><span class="sxs-lookup"><span data-stu-id="34e81-128">Current texture coordinates</span></span>

<span data-ttu-id="34e81-129">Flag di posizione corrente della posizione raster corrente GL \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="34e81-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="34e81-130">Colore RGBA associato alla posizione raster corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="34e81-131">Indice dei colori associato alla posizione raster corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-131">Color index associated with current raster position</span></span>

<span data-ttu-id="34e81-132">Coordinate di trama associate alla posizione raster corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="34e81-133">\_Flag di \_ flag Edge GL</span><span class="sxs-lookup"><span data-stu-id="34e81-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="34e81-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_ \_ bit buffer di profondità GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-135">\_Bit di \_ Abilitazione test di profondità GL</span><span class="sxs-lookup"><span data-stu-id="34e81-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="34e81-136">Funzione di test del buffer di profondità</span><span class="sxs-lookup"><span data-stu-id="34e81-136">Depth buffer test function</span></span>

<span data-ttu-id="34e81-137">Valore Clear buffer Depth</span><span class="sxs-lookup"><span data-stu-id="34e81-137">Depth buffer clear value</span></span>

<span data-ttu-id="34e81-138">\_Bit di \_ Abilitazione WRITEMASK Depth</span><span class="sxs-lookup"><span data-stu-id="34e81-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="34e81-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit di abilitazione GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-140">\_Flag di \_ test GL Alpha</span><span class="sxs-lookup"><span data-stu-id="34e81-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="34e81-141">\_Flag di \_ normalizzazione automatica GL</span><span class="sxs-lookup"><span data-stu-id="34e81-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="34e81-142">\_Flag di Blend GL</span><span class="sxs-lookup"><span data-stu-id="34e81-142">GL\_BLEND flag</span></span>

<span data-ttu-id="34e81-143">Abilita BITS per i piani di ritaglio definibili dall'utente</span><span class="sxs-lookup"><span data-stu-id="34e81-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="34e81-144">\_materiale colore \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="34e81-145">\_Flag della faccia di abbattimento GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="34e81-146">\_Flag di \_ test profondità GL</span><span class="sxs-lookup"><span data-stu-id="34e81-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="34e81-147">\_Flag di dithering GL</span><span class="sxs-lookup"><span data-stu-id="34e81-147">GL\_DITHER flag</span></span>

<span data-ttu-id="34e81-148">\_Flag di nebbia GL</span><span class="sxs-lookup"><span data-stu-id="34e81-148">GL\_FOG flag</span></span>

<span data-ttu-id="34e81-149">GL \_ Light *i* where 0 <= *i* < GL \_ Max \_ Lights</span><span class="sxs-lookup"><span data-stu-id="34e81-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="34e81-150">\_Flag di illuminazione GL</span><span class="sxs-lookup"><span data-stu-id="34e81-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="34e81-151">\_ \_ Flag uniforme linea GL</span><span class="sxs-lookup"><span data-stu-id="34e81-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="34e81-152">\_ \_ Flag stipple linea GL</span><span class="sxs-lookup"><span data-stu-id="34e81-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="34e81-153">\_ \_ Flag op della logica colori GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="34e81-154">\_ \_ Flag op logica indice GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="34e81-155">GL \_ Mappa1 \_ x dove x è un tipo di mappa</span><span class="sxs-lookup"><span data-stu-id="34e81-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="34e81-156">GL \_ map2 \_ x dove x è un tipo di mappa</span><span class="sxs-lookup"><span data-stu-id="34e81-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="34e81-157">\_Flag di normalizzazione GL</span><span class="sxs-lookup"><span data-stu-id="34e81-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="34e81-158">\_Flag uniforme del punto GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="34e81-159">\_Flag di \_ linea offset POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="34e81-160">\_Flag di \_ riempimento offset POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="34e81-161">\_Flag del \_ punto di offset del POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="34e81-162">\_Flag uniforme poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="34e81-163">\_Flag GL poligono \_ stipple</span><span class="sxs-lookup"><span data-stu-id="34e81-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="34e81-164">\_Flag di test della forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="34e81-165">\_Flag di \_ test stencil GL</span><span class="sxs-lookup"><span data-stu-id="34e81-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="34e81-166">\_Flag di trama GL \_ 1D</span><span class="sxs-lookup"><span data-stu-id="34e81-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="34e81-167">\_ \_ Flag 2D trama GL</span><span class="sxs-lookup"><span data-stu-id="34e81-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="34e81-168">Flag GL \_ trama \_ gen \_ x dove x è S, T, R o Q</span><span class="sxs-lookup"><span data-stu-id="34e81-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="34e81-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>BIT valutazione GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="34e81-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-170">GL \_ Mappa1 \_ x Abilita BITS, dove x è un tipo di mappa</span><span class="sxs-lookup"><span data-stu-id="34e81-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="34e81-171">GL \_ map2 \_ x Abilita BITS, dove x è un tipo di mappa</span><span class="sxs-lookup"><span data-stu-id="34e81-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="34e81-172">endpoint e divisioni della griglia da 1 a D</span><span class="sxs-lookup"><span data-stu-id="34e81-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="34e81-173">endpoint e divisioni della griglia 2D</span><span class="sxs-lookup"><span data-stu-id="34e81-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="34e81-174">\_Bit di \_ attivazione normale automatica GL</span><span class="sxs-lookup"><span data-stu-id="34e81-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="34e81-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit di nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-176">\_Flag di abilitazione della nebbia GL</span><span class="sxs-lookup"><span data-stu-id="34e81-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="34e81-177">Colore nebbia</span><span class="sxs-lookup"><span data-stu-id="34e81-177">Fog color</span></span>

<span data-ttu-id="34e81-178">Densità di nebbia</span><span class="sxs-lookup"><span data-stu-id="34e81-178">Fog density</span></span>

<span data-ttu-id="34e81-179">Inizio nebbia lineare</span><span class="sxs-lookup"><span data-stu-id="34e81-179">Linear fog start</span></span>

<span data-ttu-id="34e81-180">Fine nebbia lineare</span><span class="sxs-lookup"><span data-stu-id="34e81-180">Linear fog end</span></span>

<span data-ttu-id="34e81-181">Indice nebbia</span><span class="sxs-lookup"><span data-stu-id="34e81-181">Fog index</span></span>

<span data-ttu-id="34e81-182">Valore della modalità di \_ nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="34e81-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit suggerimento \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-184">\_Impostazione dell' \_ hint di correzione prospettiva GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="34e81-185">\_Impostazione del \_ Suggerimento smussato del punto GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="34e81-186">\_Impostazione dell' \_ hint uniforme linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="34e81-187">\_Impostazione dell' \_ hint Smooth POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="34e81-188">Impostazione del suggerimento di \_ nebbia GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="34e81-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit di illuminazione GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-190">\_Bit di \_ Abilitazione materiale colore GL</span><span class="sxs-lookup"><span data-stu-id="34e81-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="34e81-191">\_ \_ Valore viso materiale colore GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="34e81-192">Parametri del materiale colori che verificano il colore corrente</span><span class="sxs-lookup"><span data-stu-id="34e81-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="34e81-193">Colore della scena ambiente</span><span class="sxs-lookup"><span data-stu-id="34e81-193">Ambient scene color</span></span>

<span data-ttu-id="34e81-194">\_ \_ \_ Valore del visualizzatore locale per GL Light Model \_</span><span class="sxs-lookup"><span data-stu-id="34e81-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="34e81-195">\_ \_ \_ Impostazione lato due del modello GL Light \_</span><span class="sxs-lookup"><span data-stu-id="34e81-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="34e81-196">\_Bit di abilitazione dell'illuminazione GL</span><span class="sxs-lookup"><span data-stu-id="34e81-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="34e81-197">Abilita bit per ogni luce</span><span class="sxs-lookup"><span data-stu-id="34e81-197">Enable bit for each light</span></span>

<span data-ttu-id="34e81-198">Intensità di ambiente, diffusa e speculare per ogni luce</span><span class="sxs-lookup"><span data-stu-id="34e81-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="34e81-199">Direzione, posizione, esponente e angolo di taglio per ogni luce</span><span class="sxs-lookup"><span data-stu-id="34e81-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="34e81-200">Fattori di attenuazione costanti, lineari e quadratici per ogni luce</span><span class="sxs-lookup"><span data-stu-id="34e81-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="34e81-201">Colore di ambiente, diffuso, speculare e emissivo per ogni materiale</span><span class="sxs-lookup"><span data-stu-id="34e81-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="34e81-202">Indici di colore ambient, Diffusion e speculare per ogni materiale</span><span class="sxs-lookup"><span data-stu-id="34e81-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="34e81-203">Esponente speculare per ogni impostazione del modello GL \_ Shade del materiale \_</span><span class="sxs-lookup"><span data-stu-id="34e81-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="34e81-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit linea \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="34e81-205">\_ \_ Flag uniforme linea GL</span><span class="sxs-lookup"><span data-stu-id="34e81-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="34e81-206">\_Bit di \_ Abilitazione della riga GL stipple</span><span class="sxs-lookup"><span data-stu-id="34e81-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="34e81-207">Modello stipple linea e Ripeti contatore</span><span class="sxs-lookup"><span data-stu-id="34e81-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="34e81-208">Spessore linea</span><span class="sxs-lookup"><span data-stu-id="34e81-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="34e81-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit elenco \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-210">\_ \_ Impostazione base elenco GL</span><span class="sxs-lookup"><span data-stu-id="34e81-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="34e81-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit in \_ modalità GL pixel \_</span><span class="sxs-lookup"><span data-stu-id="34e81-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-212">\_Impostazioni della \_ \_ scala rossa e della distorsione GL rosse \_</span><span class="sxs-lookup"><span data-stu-id="34e81-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="34e81-213">Valori della scala verde GL \_ \_ e della distorsione GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="34e81-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="34e81-214">\_Bias blu GL \_ e \_ scala GL blu \_</span><span class="sxs-lookup"><span data-stu-id="34e81-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="34e81-215">\_ \_ Polarizzazione GL Alpha e \_ scala GL Alpha \_</span><span class="sxs-lookup"><span data-stu-id="34e81-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="34e81-216">\_ \_ Distorsione di profondità GL e \_ scala di profondità GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="34e81-217">\_Offset indice GL \_ e \_ \_ valori MAIUSC di indice GL</span><span class="sxs-lookup"><span data-stu-id="34e81-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="34e81-218">\_Colori della mappa GL \_ e \_ flag di stencil della mappa GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="34e81-219">\_Fattori zoom \_ X e GL \_ Zoom \_ Y</span><span class="sxs-lookup"><span data-stu-id="34e81-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="34e81-220">Impostazione del buffer di \_ lettura GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="34e81-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit punto \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-222">\_Flag uniforme del punto GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="34e81-223">Dimensioni dei punti</span><span class="sxs-lookup"><span data-stu-id="34e81-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="34e81-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-225">\_Bit di \_ Abilitazione della faccia di selezione GL</span><span class="sxs-lookup"><span data-stu-id="34e81-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="34e81-226">\_ \_ Valore modalità della faccia di selezione GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="34e81-227">\_ \_ Indicatore viso anteriore GL</span><span class="sxs-lookup"><span data-stu-id="34e81-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="34e81-228">\_Impostazione della modalità poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="34e81-229">\_Flag uniforme poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="34e81-230">\_Bit di \_ Abilitazione stipple POLIGONo GL</span><span class="sxs-lookup"><span data-stu-id="34e81-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="34e81-231">\_Flag di \_ riempimento offset POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="34e81-232">\_Flag di \_ linea offset POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="34e81-233">\_Flag del \_ punto di offset del POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="34e81-234">\_fattore di \_ offset POLIGONo GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="34e81-235">\_unità offset poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="34e81-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="34e81-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_bit stipple poligono GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="34e81-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-237">Immagine stipple poligono</span><span class="sxs-lookup"><span data-stu-id="34e81-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="34e81-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_bit a forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-239">\_Flag di test della forbice GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="34e81-240">Casella Scissor</span><span class="sxs-lookup"><span data-stu-id="34e81-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="34e81-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_ \_ bit buffer dello stencil GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-242">\_Bit di \_ Abilitazione test stencil GL</span><span class="sxs-lookup"><span data-stu-id="34e81-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="34e81-243">Funzione stencil e valore di riferimento</span><span class="sxs-lookup"><span data-stu-id="34e81-243">Stencil function and reference value</span></span>

<span data-ttu-id="34e81-244">Maschera valore stencil</span><span class="sxs-lookup"><span data-stu-id="34e81-244">Stencil value mask</span></span>

<span data-ttu-id="34e81-245">Azioni di passaggio del buffer di errore, passaggio e profondità dello stencil</span><span class="sxs-lookup"><span data-stu-id="34e81-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="34e81-246">Valore cancellazione buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="34e81-246">Stencil buffer clear value</span></span>

<span data-ttu-id="34e81-247">Writemask buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="34e81-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="34e81-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="34e81-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-249">Abilita BITS per le quattro coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="34e81-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="34e81-250">Colore del bordo per ogni immagine di trama</span><span class="sxs-lookup"><span data-stu-id="34e81-250">Border color for each texture image</span></span>

<span data-ttu-id="34e81-251">Funzione minification per ogni immagine di trama</span><span class="sxs-lookup"><span data-stu-id="34e81-251">Minification function for each texture image</span></span>

<span data-ttu-id="34e81-252">Funzione di ingrandimento per ogni immagine di trama</span><span class="sxs-lookup"><span data-stu-id="34e81-252">Magnification function for each texture image</span></span>

<span data-ttu-id="34e81-253">Coordinate di trama e modalità a capo per ogni immagine di trama</span><span class="sxs-lookup"><span data-stu-id="34e81-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="34e81-254">Colore e modalità per ogni ambiente di trama</span><span class="sxs-lookup"><span data-stu-id="34e81-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="34e81-255">Abilita BITS GL \_ texture \_ gen \_ *x*; *x* è S, T, R e Q</span><span class="sxs-lookup"><span data-stu-id="34e81-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="34e81-256">\_ \_ \_ Impostazione della modalità di generazione della trama GL per S, T, R e Q</span><span class="sxs-lookup"><span data-stu-id="34e81-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="34e81-257">equazioni del piano glTexGen per S, T, R e Q</span><span class="sxs-lookup"><span data-stu-id="34e81-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="34e81-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit di trasformazione GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-259">Coefficienti dei sei piani di ritaglio</span><span class="sxs-lookup"><span data-stu-id="34e81-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="34e81-260">Abilita BITS per i piani di ritaglio definibili dall'utente</span><span class="sxs-lookup"><span data-stu-id="34e81-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="34e81-261">\_Valore della \_ modalità matrice GL</span><span class="sxs-lookup"><span data-stu-id="34e81-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="34e81-262">\_Flag di normalizzazione GL</span><span class="sxs-lookup"><span data-stu-id="34e81-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="34e81-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit del viewport GL \_</span><span class="sxs-lookup"><span data-stu-id="34e81-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="34e81-264">Intervallo di profondità (quasi e lontano)</span><span class="sxs-lookup"><span data-stu-id="34e81-264">Depth range (near and far)</span></span>

<span data-ttu-id="34e81-265">Origine e extent del viewport</span><span class="sxs-lookup"><span data-stu-id="34e81-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e81-266">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34e81-266">Return value</span></span>

<span data-ttu-id="34e81-267">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="34e81-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="34e81-268">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="34e81-268">Error codes</span></span>

<span data-ttu-id="34e81-269">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="34e81-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="34e81-270">Nome</span><span class="sxs-lookup"><span data-stu-id="34e81-270">Name</span></span>                                                                                                  | <span data-ttu-id="34e81-271">Significato</span><span class="sxs-lookup"><span data-stu-id="34e81-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34e81-272"><dt>**\_overflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34e81-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="34e81-273">La funzione è stata chiamata mentre lo stack dell'attributo era pieno.</span><span class="sxs-lookup"><span data-stu-id="34e81-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="34e81-274"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34e81-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="34e81-275">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="34e81-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="34e81-276">Commenti</span><span class="sxs-lookup"><span data-stu-id="34e81-276">Remarks</span></span>

<span data-ttu-id="34e81-277">La funzione **glPushAttrib** accetta un argomento, una maschera che indica i gruppi di variabili di stato da salvare nello stack di attributi.</span><span class="sxs-lookup"><span data-stu-id="34e81-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="34e81-278">Le costanti simboliche vengono utilizzate per impostare i bit nella maschera.</span><span class="sxs-lookup"><span data-stu-id="34e81-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="34e81-279">Il parametro mask viene in genere costruito applicando l' **operazione or** logica a diverse di queste costanti.</span><span class="sxs-lookup"><span data-stu-id="34e81-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="34e81-280">È possibile utilizzare la speciale maschera GL \_ tutti \_ i \_ bit attrib per salvare tutti gli Stati impilabili.</span><span class="sxs-lookup"><span data-stu-id="34e81-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="34e81-281">La funzione [**glPopAttrib**](glpopattrib.md) Ripristina i valori delle variabili di stato salvate con l'ultimo comando **glPushAttrib** .</span><span class="sxs-lookup"><span data-stu-id="34e81-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="34e81-282">Quelli non salvati vengono lasciati invariati.</span><span class="sxs-lookup"><span data-stu-id="34e81-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="34e81-283">Non è possibile eseguire il push degli attributi in uno stack completo oppure per estrarre gli attributi da uno stack vuoto.</span><span class="sxs-lookup"><span data-stu-id="34e81-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="34e81-284">In entrambi i casi, viene impostato il flag di errore e non viene apportata alcuna modifica allo stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="34e81-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="34e81-285">Inizialmente, lo stack dell'attributo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="34e81-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="34e81-286">Non tutti i valori per lo stato OpenGL possono essere salvati nello stack di attributi.</span><span class="sxs-lookup"><span data-stu-id="34e81-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="34e81-287">Ad esempio, non è possibile salvare il pacchetto di pixel e decomprimere lo stato, la modalità di rendering e lo stato di selezione e di feedback.</span><span class="sxs-lookup"><span data-stu-id="34e81-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="34e81-288">La profondità dello stack di attributi dipende dall'implementazione, ma deve essere almeno 16.</span><span class="sxs-lookup"><span data-stu-id="34e81-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="34e81-289">Le funzioni seguenti recuperano informazioni relative a **glPushAttrib** e [**glPopAttrib**](glpopattrib.md):</span><span class="sxs-lookup"><span data-stu-id="34e81-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="34e81-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack \_ attrib</span><span class="sxs-lookup"><span data-stu-id="34e81-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="34e81-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ dello stack \_ attrib</span><span class="sxs-lookup"><span data-stu-id="34e81-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="34e81-292">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34e81-292">Requirements</span></span>



| <span data-ttu-id="34e81-293">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e81-293">Requirement</span></span> | <span data-ttu-id="34e81-294">Valore</span><span class="sxs-lookup"><span data-stu-id="34e81-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e81-295">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34e81-295">Minimum supported client</span></span><br/> | <span data-ttu-id="34e81-296">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="34e81-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34e81-297">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34e81-297">Minimum supported server</span></span><br/> | <span data-ttu-id="34e81-298">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="34e81-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34e81-299">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34e81-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="34e81-300"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e81-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="34e81-301">Libreria</span><span class="sxs-lookup"><span data-stu-id="34e81-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="34e81-302"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e81-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="34e81-303">DLL</span><span class="sxs-lookup"><span data-stu-id="34e81-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34e81-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e81-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e81-305">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34e81-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e81-306">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="34e81-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="34e81-307">**Remo**</span><span class="sxs-lookup"><span data-stu-id="34e81-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="34e81-308">**glGet**</span><span class="sxs-lookup"><span data-stu-id="34e81-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="34e81-309">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="34e81-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="34e81-310">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="34e81-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="34e81-311">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="34e81-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="34e81-312">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="34e81-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="34e81-313">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="34e81-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="34e81-314">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="34e81-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="34e81-315">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="34e81-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="34e81-316">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="34e81-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="34e81-317">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="34e81-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="34e81-318">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="34e81-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="34e81-319">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="34e81-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="34e81-320">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="34e81-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="34e81-321">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="34e81-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="34e81-322">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="34e81-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





