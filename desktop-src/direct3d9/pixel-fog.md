---
description: La nebbia dei pixel ottiene il nome dal fatto che viene calcolato in base ai singoli pixel nel driver di dispositivo.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Nebbia pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875962"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="c9021-103">Nebbia pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9021-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="c9021-104">La nebbia dei pixel ottiene il nome dal fatto che viene calcolato in base ai singoli pixel nel driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9021-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="c9021-105">Questa operazione è diversa dalla nebbia dei vertici, calcolata dalla pipeline durante i calcoli di trasformazione e illuminazione.</span><span class="sxs-lookup"><span data-stu-id="c9021-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="c9021-106">La nebbia dei pixel è talvolta denominata nebbia della tabella perché alcuni driver usano una tabella di ricerca precalcolata per determinare il fattore di nebbia, usando la profondità di ogni pixel da applicare ai calcoli di fusione.</span><span class="sxs-lookup"><span data-stu-id="c9021-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="c9021-107">Può essere applicato usando qualsiasi formula di nebbia identificata dai membri del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c9021-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="c9021-108">Le implementazioni di queste formule sono specifiche del driver.</span><span class="sxs-lookup"><span data-stu-id="c9021-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="c9021-109">Se un driver non supporta una formula di nebbia complessa, dovrebbe riportare una formula meno complessa.</span><span class="sxs-lookup"><span data-stu-id="c9021-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="c9021-110">Profondità basata su Eye-Relative rispetto a Z</span><span class="sxs-lookup"><span data-stu-id="c9021-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="c9021-111">Per alleviare gli artefatti grafici correlati alla nebbia causati da una distribuzione non uniforme di valori z in un buffer di profondità, la maggior parte dei dispositivi hardware usa la profondità relativa agli occhi anziché i valori di profondità basati su z per la nebbia dei pixel.</span><span class="sxs-lookup"><span data-stu-id="c9021-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="c9021-112">La profondità relativa agli occhi è essenzialmente l'elemento w da un set di coordinate omogeneo.</span><span class="sxs-lookup"><span data-stu-id="c9021-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="c9021-113">Microsoft Direct3D accetta il reciproco dell'elemento RHW da un set di coordinate dello spazio del dispositivo per riprodurre true w.</span><span class="sxs-lookup"><span data-stu-id="c9021-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="c9021-114">Se un dispositivo supporta la nebbia relativa agli occhi, imposta il flag **D3DPRASTERCAPS \_ WFOG** nel membro RasterCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando si chiama il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="c9021-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="c9021-115">Fatta eccezione per l'unità di rasterizzazione dei riferimenti, i dispositivi software utilizzano sempre z per calcolare gli effetti della nebbia dei pixel.</span><span class="sxs-lookup"><span data-stu-id="c9021-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="c9021-116">Quando la nebbia relativa agli occhi è supportata, il sistema usa automaticamente la profondità relativa agli occhi anziché la profondità basata sulla z Se la matrice di proiezione fornita produce valori z nello spazio globale equivalenti ai valori w nello spazio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9021-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="c9021-117">È possibile impostare la matrice di proiezione chiamando il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) , usando il \_ valore di proiezione D3DTS e passando una struttura [**D3DMATRIX**](d3dmatrix.md) che rappresenta la matrice desiderata.</span><span class="sxs-lookup"><span data-stu-id="c9021-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="c9021-118">Se la matrice di proiezione non è conforme a questo requisito, gli effetti di nebbia non vengono applicati correttamente.</span><span class="sxs-lookup"><span data-stu-id="c9021-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="c9021-119">Per informazioni dettagliate sulla creazione di una matrice conforme, vedere [trasformazione della proiezione (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="c9021-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="c9021-120">Direct3D usa la matrice di proiezione attualmente impostata nei calcoli di profondità basati su w.</span><span class="sxs-lookup"><span data-stu-id="c9021-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="c9021-121">Di conseguenza, un'applicazione deve impostare una matrice di proiezione conforme per ricevere le funzionalità basate su w desiderate, anche se non utilizza la pipeline di trasformazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c9021-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="c9021-122">Direct3D controlla la quarta colonna della matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="c9021-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="c9021-123">Se i coefficienti sono \[ 0, 0, 0, 1 \] (per una proiezione affine), il sistema utilizzerà valori di profondità basati su z per la nebbia.</span><span class="sxs-lookup"><span data-stu-id="c9021-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="c9021-124">In questo caso, è necessario specificare anche le distanze di inizio e fine per gli effetti di nebbia lineare nello spazio del dispositivo, che varia da 0,0 al punto più vicino all'utente e 1,0 al punto più lontano.</span><span class="sxs-lookup"><span data-stu-id="c9021-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="c9021-125">Uso della nebbia pixel</span><span class="sxs-lookup"><span data-stu-id="c9021-125">Using Pixel Fog</span></span>

<span data-ttu-id="c9021-126">Usare la procedura seguente per abilitare la nebbia dei pixel nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9021-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="c9021-127">Abilitare la fusione di nebbia impostando lo \_ stato di rendering FOGENABLE di D3DRS su **true**.</span><span class="sxs-lookup"><span data-stu-id="c9021-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="c9021-128">Impostare il colore di nebbia desiderato nello \_ stato di rendering FogColor di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="c9021-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="c9021-129">Scegliere la formula di nebbia da usare impostando lo \_ stato di rendering FOGTABLEMODE di D3DRS sul membro corrispondente del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c9021-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="c9021-130">Impostare i parametri di nebbia come desiderato per la modalità di nebbia selezionata negli Stati di rendering associati.</span><span class="sxs-lookup"><span data-stu-id="c9021-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="c9021-131">Sono incluse le distanze iniziale e finale per la nebbia lineare e la densità di nebbia per la modalità di nebbia esponenziale.</span><span class="sxs-lookup"><span data-stu-id="c9021-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="c9021-132">Nell'esempio seguente vengono illustrati i passaggi che possono essere simili nel codice.</span><span class="sxs-lookup"><span data-stu-id="c9021-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="c9021-133">Alcuni parametri di nebbia sono necessari come valori a virgola mobile, anche se il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta solo valori DWORD nel secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="c9021-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="c9021-134">Nell'esempio precedente vengono forniti i valori a virgola mobile in **IDirect3DDevice9:: SetRenderState** senza conversione dei dati eseguendo il cast degli indirizzi delle variabili a virgola mobile come puntatori DWORD, quindi dereferenziarli.</span><span class="sxs-lookup"><span data-stu-id="c9021-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9021-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9021-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9021-136">Tipi di nebbia</span><span class="sxs-lookup"><span data-stu-id="c9021-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
