---
description: Questa sezione contiene informazioni sull'organizzazione interna dei formati di trama compressi.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formati di trama compressi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748799"
---
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="a7db4-103">Formati di trama compressi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a7db4-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="a7db4-104">Questa sezione contiene informazioni sull'organizzazione interna dei formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="a7db4-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="a7db4-105">Questi dettagli non sono necessari per usare le trame compresse, perché è possibile usare le funzioni D3DX per la conversione da e verso formati compressi.</span><span class="sxs-lookup"><span data-stu-id="a7db4-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="a7db4-106">Tuttavia, queste informazioni sono utili se si desidera operare direttamente sui dati della superficie compressa.</span><span class="sxs-lookup"><span data-stu-id="a7db4-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="a7db4-107">Direct3D usa un formato di compressione che divide le mappe di trama in blocchi di Texel 4x4.</span><span class="sxs-lookup"><span data-stu-id="a7db4-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="a7db4-108">Se la trama non contiene trasparenza, è opaca o se la trasparenza è specificata da un alfa a 1 bit, un blocco a 8 byte rappresenta il blocco mappa di trama.</span><span class="sxs-lookup"><span data-stu-id="a7db4-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="a7db4-109">Se la mappa di trama contiene Texel trasparenti, usando un canale alfa, un blocco a 16 byte lo rappresenta.</span><span class="sxs-lookup"><span data-stu-id="a7db4-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="a7db4-110">Trame alfa opache e a 1 bit (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a7db4-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="a7db4-111">Trame con canali alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a7db4-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="a7db4-112">Ogni singola trama deve specificare che i dati vengono archiviati come 64 o 128 bit per gruppo di 16 Texel.</span><span class="sxs-lookup"><span data-stu-id="a7db4-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="a7db4-113">Se i blocchi a 64 bit, ovvero Format DXT1, vengono usati per la trama, è possibile combinare i formati alfa opachi e a 1 bit in base ai singoli blocchi all'interno della stessa trama.</span><span class="sxs-lookup"><span data-stu-id="a7db4-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="a7db4-114">In altre parole, il confronto tra il Unsigned Integer Magnitude del colore \_ 0 e il colore \_ 1 viene eseguito in modo univoco per ogni blocco di 16 Texel.</span><span class="sxs-lookup"><span data-stu-id="a7db4-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="a7db4-115">Quando si utilizzano blocchi a 128 bit, il canale alfa deve essere specificato in modo esplicito (format DXT2 o DXT3) o in modalità interpolata (format DXT4 o DXT5) per l'intera trama.</span><span class="sxs-lookup"><span data-stu-id="a7db4-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="a7db4-116">Come con il colore, quando si seleziona la modalità interpolata, è possibile usare otto Alpha interpolati o sei modalità alfa interpolate in base a blocchi.</span><span class="sxs-lookup"><span data-stu-id="a7db4-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="a7db4-117">Anche in questo caso, il confronto di magnitude tra Alpha \_ 0 e Alpha \_ 1 viene eseguito in modo univoco in base a blocchi.</span><span class="sxs-lookup"><span data-stu-id="a7db4-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="a7db4-118">Il pitch per i formati DXTn è diverso da quello restituito in DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="a7db4-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="a7db4-119">Il pitch è ora misurato in byte (non in blocchi).</span><span class="sxs-lookup"><span data-stu-id="a7db4-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="a7db4-120">Se, ad esempio, si dispone di una larghezza di 16, sarà presente un passo di quattro blocchi (4 \* 8 per DXT1, 4 \* 16 per DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="a7db4-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7db4-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7db4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7db4-122">Risorse di trama compresse</span><span class="sxs-lookup"><span data-stu-id="a7db4-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



