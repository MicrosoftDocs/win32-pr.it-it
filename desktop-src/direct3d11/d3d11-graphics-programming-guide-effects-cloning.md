---
title: Clonazione di un effetto
description: La clonazione di un effetto crea una seconda copia pressoché identica dell'effetto.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711704"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="ca21e-103">Clonazione di un effetto</span><span class="sxs-lookup"><span data-stu-id="ca21e-103">Cloning an Effect</span></span>

<span data-ttu-id="ca21e-104">La clonazione di un effetto crea una seconda copia pressoché identica dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="ca21e-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="ca21e-105">Per una spiegazione del motivo per cui non è esatto, vedere il seguente qualificatore singolo.</span><span class="sxs-lookup"><span data-stu-id="ca21e-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="ca21e-106">Una seconda copia di un effetto è utile quando si desidera utilizzare il Framework degli effetti su più thread, poiché il runtime di effetto non è thread-safe per garantire prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="ca21e-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="ca21e-107">Poiché i contesti di dispositivo sono anche non thread-safe, i thread diversi devono passare contesti di dispositivo diversi al metodo ID3DX11EffectPass:: Apply.</span><span class="sxs-lookup"><span data-stu-id="ca21e-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="ca21e-108">È possibile clonare un effetto con la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="ca21e-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="ca21e-109">Nell'esempio precedente, la copia clonata incapsula lo stesso stato dell'effetto originale, indipendentemente dallo stato in cui si trova l'effetto originale.</span><span class="sxs-lookup"><span data-stu-id="ca21e-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="ca21e-110">In particolare:</span><span class="sxs-lookup"><span data-stu-id="ca21e-110">In particular:</span></span>

1.  <span data-ttu-id="ca21e-111">Se pEffect è ottimizzato, l'effetto pCloned è ottimizzato</span><span class="sxs-lookup"><span data-stu-id="ca21e-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="ca21e-112">Se pEffect dispone di alcune variabili gestite dall'utente, l'effetto pCloned avrà le stesse variabili gestite dall'utente (vedere la descrizione singola riportata di seguito)</span><span class="sxs-lookup"><span data-stu-id="ca21e-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="ca21e-113">Eventuali aggiornamenti di variabili in sospeso (fino a quando una chiamata Apply aggiorna lo stato del dispositivo) in pEffect sarà in sospeso in pClonedEffect</span><span class="sxs-lookup"><span data-stu-id="ca21e-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="ca21e-114">Gli oggetti dispositivo Direct3D 11 seguenti non sono modificabili o non vengono mai aggiornati dal framework degli effetti, quindi l'effetto clonato punterà sugli stessi oggetti dell'effetto originale:</span><span class="sxs-lookup"><span data-stu-id="ca21e-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="ca21e-115">Oggetti Block di stato (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span><span class="sxs-lookup"><span data-stu-id="ca21e-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="ca21e-116">Shader</span><span class="sxs-lookup"><span data-stu-id="ca21e-116">Shaders</span></span>
3.  <span data-ttu-id="ca21e-117">Istanze di classe</span><span class="sxs-lookup"><span data-stu-id="ca21e-117">Class instances</span></span>
4.  <span data-ttu-id="ca21e-118">Trame (esclusi i buffer di trama)</span><span class="sxs-lookup"><span data-stu-id="ca21e-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="ca21e-119">Viste di accesso non ordinate</span><span class="sxs-lookup"><span data-stu-id="ca21e-119">Unordered access views</span></span>

<span data-ttu-id="ca21e-120">Gli oggetti dispositivo Direct3D 11 seguenti sono sia non modificabili che modificati dal runtime degli effetti (a meno che non sia gestito dall'utente o singolo in un effetto clonato); le nuove copie di questi oggetti vengono create quando non sono singole:</span><span class="sxs-lookup"><span data-stu-id="ca21e-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="ca21e-121">Buffer costanti</span><span class="sxs-lookup"><span data-stu-id="ca21e-121">Constant buffers</span></span>
2.  <span data-ttu-id="ca21e-122">Buffer di trama</span><span class="sxs-lookup"><span data-stu-id="ca21e-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="ca21e-123">Buffer costanti singoli e buffer di trama</span><span class="sxs-lookup"><span data-stu-id="ca21e-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="ca21e-124">Si noti che questa discussione si applica sia ai buffer costanti che alle trame, ma si presuppone che i buffer costanti siano facilmente leggibili.</span><span class="sxs-lookup"><span data-stu-id="ca21e-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="ca21e-125">In alcuni casi è possibile che un buffer costante venga aggiornato da un solo thread, ma questi dati verranno utilizzati dallo stato del dispositivo impostato dagli effetti clonati.</span><span class="sxs-lookup"><span data-stu-id="ca21e-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="ca21e-126">Ad esempio, l'effetto principale può aggiornare le matrici World e View a cui viene fatto riferimento dagli shader negli effetti clonati che non modificano le matrici World e View.</span><span class="sxs-lookup"><span data-stu-id="ca21e-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="ca21e-127">In questi casi, è necessario che gli effetti clonati facciano riferimento al buffer costante corrente anziché ricrearne uno.</span><span class="sxs-lookup"><span data-stu-id="ca21e-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="ca21e-128">Esistono due modi per ottenere questo risultato desiderato:</span><span class="sxs-lookup"><span data-stu-id="ca21e-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="ca21e-129">Usare ID3DX11EffectConstantBuffer:: SetConstantBuffer per l'effetto clonato per renderlo gestito dall'utente</span><span class="sxs-lookup"><span data-stu-id="ca21e-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="ca21e-130">Contrassegnare il buffer costante come "singolo" nel codice HLSL, forzando il runtime di effetto a considerarlo come gestito dall'utente dopo la clonazione</span><span class="sxs-lookup"><span data-stu-id="ca21e-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="ca21e-131">Esistono due differenze tra i due metodi precedenti.</span><span class="sxs-lookup"><span data-stu-id="ca21e-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="ca21e-132">Per prima cosa, nel metodo 1, viene creato un nuovo ID3D11Buffer e l'utente prima della chiamata a SetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="ca21e-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="ca21e-133">Inoltre, dopo aver chiamato UndoSetConstantBuffer nell'effetto clonato, la variabile nel metodo 1will punta al buffer appena creato (gli effetti verranno aggiornati su Apply), mentre la variabile nel metodo 2 continuerà a puntare al buffer originale (senza aggiornarlo all'applicazione).</span><span class="sxs-lookup"><span data-stu-id="ca21e-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="ca21e-134">Vedere l'esempio seguente in HLSL:</span><span class="sxs-lookup"><span data-stu-id="ca21e-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="ca21e-135">Durante la clonazione, l'effetto clonato creerà un nuovo ID3D11Buffer per ObjectData e riempirà il relativo contenuto su Apply, ma fa riferimento al ID3D11Buffer originale per ViewData.</span><span class="sxs-lookup"><span data-stu-id="ca21e-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="ca21e-136">Il qualificatore singolo può essere ignorato nel processo di clonazione impostando il \_ flag D3DX11 Effect \_ Clone \_ Force \_ unsingle flag.</span><span class="sxs-lookup"><span data-stu-id="ca21e-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca21e-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca21e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca21e-138">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ca21e-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




