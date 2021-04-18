---
description: Le prime immagini 3D generate dal computer, sebbene in genere avanzate per il loro tempo, tendono a avere un aspetto lucido in plastica.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Concetti di base sulla trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305112"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="841c5-103">Concetti di base sulla trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="841c5-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="841c5-104">Le prime immagini 3D generate dal computer, sebbene in genere avanzate per il loro tempo, tendono a avere un aspetto lucido in plastica.</span><span class="sxs-lookup"><span data-stu-id="841c5-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="841c5-105">Hanno mancato i tipi di contrassegno, ad esempio graffi, crepe, impronte digitali e sbavature, che offrono agli oggetti 3D complessità visiva realistica.</span><span class="sxs-lookup"><span data-stu-id="841c5-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="841c5-106">Negli ultimi anni, le trame hanno acquisito popolarità tra gli sviluppatori come uno strumento per migliorare il realismo delle immagini 3D generate dal computer.</span><span class="sxs-lookup"><span data-stu-id="841c5-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="841c5-107">Nell'uso quotidiano, la trama della parola si riferisce alla fluidità o alla rugosità di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="841c5-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="841c5-108">In grafica computer, tuttavia, una trama è una bitmap di colori pixel che assegna a un oggetto l'aspetto della trama.</span><span class="sxs-lookup"><span data-stu-id="841c5-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="841c5-109">Poiché le trame Direct3D sono bitmap, qualsiasi bitmap può essere applicata a una primitiva Direct3D.</span><span class="sxs-lookup"><span data-stu-id="841c5-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="841c5-110">Ad esempio, le applicazioni possono creare e modificare gli oggetti che sembrano avere un modello di grana a legna.</span><span class="sxs-lookup"><span data-stu-id="841c5-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="841c5-111">È possibile applicare erba, sporcizia e rocce a un set di primitive 3D che formano una collina.</span><span class="sxs-lookup"><span data-stu-id="841c5-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="841c5-112">Il risultato è un Hillside di aspetto realistico.</span><span class="sxs-lookup"><span data-stu-id="841c5-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="841c5-113">È anche possibile usare il texturing per creare effetti quali i segni lungo una strada, gli strati rocciosi in una scogliera o l'aspetto del marmo in un piano.</span><span class="sxs-lookup"><span data-stu-id="841c5-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="841c5-114">Inoltre, Direct3D supporta tecniche di texturing più avanzate, ad esempio la combinazione di trame, con o senza la trasparenza e il mapping chiaro.</span><span class="sxs-lookup"><span data-stu-id="841c5-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="841c5-115">Per altre informazioni, vedere [blending di trame (Direct3D 9)](texture-blending.md) e [mapping chiaro con trame (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="841c5-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="841c5-116">Se l'applicazione crea un dispositivo HAL (Hardware Abstraction Layer) o un dispositivo software, può usare trame 8, 16, 24, 32, 64 o 128 bit.</span><span class="sxs-lookup"><span data-stu-id="841c5-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="841c5-117">Informazioni aggiuntive sono contenute negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="841c5-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="841c5-118">Modalità di indirizzamento delle trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="841c5-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="841c5-119">Aree dirty texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="841c5-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="841c5-120">Tavolozze delle trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="841c5-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="841c5-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="841c5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="841c5-122">Trame Direct3D</span><span class="sxs-lookup"><span data-stu-id="841c5-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



