---
description: Le applicazioni utilizzano il buffer dello stencil per mascherare i pixel in un'immagine. La maschera controlla se il pixel viene disegnato o meno. Di seguito sono riportati alcuni degli effetti più comuni.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Tecniche di buffer di stencil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401340"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="bc6a1-105">Tecniche di buffer di stencil (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc6a1-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="bc6a1-106">Le applicazioni utilizzano il buffer dello stencil per mascherare i pixel in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="bc6a1-107">La maschera controlla se il pixel viene disegnato o meno.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="bc6a1-108">Di seguito sono riportati alcuni degli effetti più comuni.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="bc6a1-109">Composizione</span><span class="sxs-lookup"><span data-stu-id="bc6a1-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="bc6a1-110">Decaing</span><span class="sxs-lookup"><span data-stu-id="bc6a1-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="bc6a1-111">Dissolvenze, dissolvenze e scorrimenti</span><span class="sxs-lookup"><span data-stu-id="bc6a1-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="bc6a1-112">Strutture e sagome</span><span class="sxs-lookup"><span data-stu-id="bc6a1-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="bc6a1-113">Stencil a due lati</span><span class="sxs-lookup"><span data-stu-id="bc6a1-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="bc6a1-114">Il buffer dello stencil Abilita o Disabilita il disegno sulla superficie di destinazione del rendering in base a un pixel per pixel.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="bc6a1-115">Al livello più fondamentale, consente alle applicazioni di mascherare le sezioni dell'immagine di cui è stato eseguito il rendering in modo che non vengano visualizzate.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="bc6a1-116">Le applicazioni spesso utilizzano buffer di stencil per effetti speciali come dissolvenze, derivazione e struttura.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="bc6a1-117">Le informazioni sul buffer dello stencil sono incorporate nei dati del buffer z.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="bc6a1-118">L'applicazione può usare il metodo [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) per verificare il supporto degli stencil hardware, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="bc6a1-119">[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) consente di scegliere un dispositivo da creare in base alle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="bc6a1-120">In questo caso, i dispositivi che non supportano i buffer di stencil a 8 bit vengono rifiutati.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="bc6a1-121">Si noti che questo è solo un possibile uso di **IDirect3D9:: CheckDeviceFormat**; per informazioni dettagliate, vedere [determinazione del supporto hardware (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="bc6a1-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="bc6a1-122">Funzionamento del buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="bc6a1-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="bc6a1-123">Direct3D esegue un test sul contenuto del buffer dello stencil in base ai singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="bc6a1-124">Per ogni pixel nell'area di destinazione, viene eseguito un test utilizzando il valore corrispondente nel buffer dello stencil, un valore di riferimento dello stencil e un valore della maschera dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="bc6a1-125">Se il test viene superato, Direct3D esegue un'azione.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="bc6a1-126">Il test viene eseguito seguendo questa procedura.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="bc6a1-127">Eseguire un'operazione con AND bit per bit del valore di riferimento dello stencil con la maschera dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="bc6a1-128">Eseguire un'operazione con AND bit per bit del valore del buffer dello stencil per il pixel corrente con la maschera dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="bc6a1-129">Confrontare il risultato del passaggio 1 con il risultato del passaggio 2, usando la funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="bc6a1-130">Questi passaggi sono illustrati nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="bc6a1-131">contenuto del buffer dello stencil per il pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="bc6a1-132">Questo esempio di codice usa il simbolo e commerciale (&) per rappresentare l'operazione AND bit per bit.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="bc6a1-133">rappresenta il valore della maschera di stencil e</span><span class="sxs-lookup"><span data-stu-id="bc6a1-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="bc6a1-134">rappresenta il valore di riferimento dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="bc6a1-135">è la funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-135">is the comparison function.</span></span>

<span data-ttu-id="bc6a1-136">Il pixel corrente viene scritto nell'area di destinazione se il test di stencil viene superato e viene ignorato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="bc6a1-137">Il comportamento di confronto predefinito consiste nel scrivere il pixel, indipendentemente dal modo in cui ogni operazione bit per bit viene disattivata (D3DCMP \_ sempre).</span><span class="sxs-lookup"><span data-stu-id="bc6a1-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="bc6a1-138">È possibile modificare questo comportamento modificando il valore dello stato di \_ rendering STENCILFUNC di D3DRS, passando un membro del tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) per identificare la funzione di confronto desiderata.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="bc6a1-139">L'applicazione può personalizzare l'operazione del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="bc6a1-140">Può impostare la funzione di confronto, la maschera dello stencil e il valore di riferimento dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="bc6a1-141">È inoltre in grado di controllare l'azione eseguita da Direct3D quando il test di stencil ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="bc6a1-142">Per ulteriori informazioni, vedere [lo stato del buffer dello stencil (Direct3D 9)](stencil-buffer-state.md).</span><span class="sxs-lookup"><span data-stu-id="bc6a1-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bc6a1-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc6a1-143">Examples</span></span>

<span data-ttu-id="bc6a1-144">Negli esempi di codice seguenti viene illustrata la configurazione del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="bc6a1-145">Per impostazione predefinita, il valore di riferimento dello stencil è zero.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="bc6a1-146">Qualsiasi valore integer è valido.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-146">Any integer value is valid.</span></span> <span data-ttu-id="bc6a1-147">Direct3D esegue un AND bit per bit del valore di riferimento dello stencil e un valore della maschera dello stencil prima del test dello stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="bc6a1-148">È possibile controllare le informazioni sui pixel scritte in base al confronto tra stencil.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="bc6a1-149">È possibile scrivere una formula personalizzata per il valore che si desidera scrivere nel buffer dello stencil, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="bc6a1-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="bc6a1-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc6a1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc6a1-151">Pipeline pixel</span><span class="sxs-lookup"><span data-stu-id="bc6a1-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
