---
description: Le applicazioni Direct3D possono ottenere numerosi effetti speciali applicando varie trame a una primitiva nel corso di più passaggi di rendering.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Combinazione di trame multipass (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124473"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="593ce-103">Combinazione di trame multipass (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="593ce-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="593ce-104">Le applicazioni Direct3D possono ottenere numerosi effetti speciali applicando varie trame a una primitiva nel corso di più passaggi di rendering.</span><span class="sxs-lookup"><span data-stu-id="593ce-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="593ce-105">Il termine comune per questa operazione è la combinazione di trame MultiPASS.</span><span class="sxs-lookup"><span data-stu-id="593ce-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="593ce-106">Un uso tipico della combinazione di trame MultiPASS consiste nell'emulare gli effetti dei modelli di illuminazione e ombreggiatura complessi applicando più colori da diverse trame diverse.</span><span class="sxs-lookup"><span data-stu-id="593ce-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="593ce-107">Una di queste applicazioni è denominata Light Mapping.</span><span class="sxs-lookup"><span data-stu-id="593ce-107">One such application is called light mapping.</span></span> <span data-ttu-id="593ce-108">Per altre informazioni, vedere [mapping chiaro con trame (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="593ce-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="593ce-109">Alcuni dispositivi sono in grado di applicare più trame alle primitive in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="593ce-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="593ce-110">Per informazioni dettagliate, vedere [blending di trame (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="593ce-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="593ce-111">Se l'hardware dell'utente non supporta la combinazione di più trame, l'applicazione può usare la combinazione di trame MultiPASS per ottenere gli stessi effetti visivi.</span><span class="sxs-lookup"><span data-stu-id="593ce-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="593ce-112">Tuttavia, l'applicazione non può sostenere le frequenze dei fotogrammi possibili quando si usa la combinazione di più trame.</span><span class="sxs-lookup"><span data-stu-id="593ce-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="593ce-113">Per eseguire la fusione di trame MultiPASS in un'applicazione C/C++.</span><span class="sxs-lookup"><span data-stu-id="593ce-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="593ce-114">Impostare una trama nella fase di trama 0 chiamando il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="593ce-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="593ce-115">Selezionare le operazioni e gli argomenti del colore e della fusione alfa desiderati con il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="593ce-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="593ce-116">Le impostazioni predefinite sono particolarmente adatte per la fusione di trame MultiPASS.</span><span class="sxs-lookup"><span data-stu-id="593ce-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="593ce-117">Esegue il rendering degli oggetti appropriati nella scena.</span><span class="sxs-lookup"><span data-stu-id="593ce-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="593ce-118">Impostare la trama successiva nella fase della trama 0.</span><span class="sxs-lookup"><span data-stu-id="593ce-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="593ce-119">Impostare gli \_ Stati di rendering D3DRS SRCBLEND e D3DRS \_ DESTBLEND per modificare i fattori di fusione di origine e di destinazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="593ce-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="593ce-120">Il sistema combina le nuove trame con i pixel esistenti nella superficie di destinazione di rendering in base a questi parametri.</span><span class="sxs-lookup"><span data-stu-id="593ce-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="593ce-121">Ripetere i passaggi 3, 4 e 5 con il numero di trame necessario.</span><span class="sxs-lookup"><span data-stu-id="593ce-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="593ce-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="593ce-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="593ce-123">Combinazione di trame</span><span class="sxs-lookup"><span data-stu-id="593ce-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
