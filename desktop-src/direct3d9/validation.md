---
description: La convalida viene eseguita durante la compilazione dell'effetto. Per convalidare la tecnica corrente, specificare NULL come handle della tecnica da convalidare.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Convalida (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303916"
---
# <a name="validation-direct3d-9"></a><span data-ttu-id="75e05-104">Convalida (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="75e05-104">Validation (Direct3D 9)</span></span>

<span data-ttu-id="75e05-105">La convalida viene eseguita durante la compilazione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="75e05-105">Validation is performed during the effect compile.</span></span> <span data-ttu-id="75e05-106">Per convalidare la tecnica corrente, specificare **null** come handle della tecnica da convalidare.</span><span class="sxs-lookup"><span data-stu-id="75e05-106">To validate the current technique, specify **NULL** as the technique handle to be validated.</span></span>

<span data-ttu-id="75e05-107">La convalida avrà esito negativo per uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="75e05-107">Validation will fail for any of the following:</span></span>

-   <span data-ttu-id="75e05-108">Se l'handle di tecnica specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="75e05-108">If the specified technique handle does not exist.</span></span>
-   <span data-ttu-id="75e05-109">Se l'applicazione di qualsiasi stato in qualsiasi passaggio della tecnica ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="75e05-109">If the application of any state in any pass of the technique fails.</span></span>
-   <span data-ttu-id="75e05-110">Se la convalida del dispositivo ha esito negativo dopo l'applicazione di tutti gli stati in qualsiasi passaggio della tecnica.</span><span class="sxs-lookup"><span data-stu-id="75e05-110">If device validation fails after the application of all the states in any pass of the technique.</span></span>
-   <span data-ttu-id="75e05-111">Se agli Stati dell'effetto PIXELSHADER o VERTEXSHADER vengono assegnati shader non validi in qualsiasi passaggio della tecnica.</span><span class="sxs-lookup"><span data-stu-id="75e05-111">If the PIXELSHADER or VERTEXSHADER effect states are assigned invalid shaders in any pass of the technique.</span></span>
-   <span data-ttu-id="75e05-112">Se i tappi dei dispositivi non supportano il mapping dei cubi e a uno stato di effetto trama viene assegnato un valore di tipo textureCUBE in qualsiasi passaggio della tecnica.</span><span class="sxs-lookup"><span data-stu-id="75e05-112">If the device caps do not support cube mapping, and a TEXTURE effect state is assigned a value of type textureCUBE in any pass of the technique.</span></span>
-   <span data-ttu-id="75e05-113">Se i tappi dei dispositivi non supportano il mapping del volume e a uno stato di effetto trama viene assegnato un valore di tipo texture3D in qualsiasi passaggio della tecnica.</span><span class="sxs-lookup"><span data-stu-id="75e05-113">If the device caps do not support volume mapping and a TEXTURE effect state is assigned a value of type texture3D in any pass of the technique.</span></span>

<span data-ttu-id="75e05-114">Per altre informazioni, vedere [Stati degli effetti (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="75e05-114">For more information, see [Effect States (Direct3D 9)](effect-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75e05-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75e05-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75e05-116">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="75e05-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



