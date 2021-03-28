---
title: Come inizializzare la fase mosaico
description: In questo argomento viene illustrato come inizializzare la fase mosaico.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992741"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="222ba-103">Procedura: inizializzare la fase mosaico</span><span class="sxs-lookup"><span data-stu-id="222ba-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="222ba-104">In generale, la suddivisione a mosaico espande il modello compatto, definito dall'utente, di una patch in geometria che contiene una quantità programmabile di dettagli.</span><span class="sxs-lookup"><span data-stu-id="222ba-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="222ba-105">La geometria è in genere un set di triangoli che rappresenta la geometria della superficie dettagliata.</span><span class="sxs-lookup"><span data-stu-id="222ba-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="222ba-106">In questo argomento viene illustrato come inizializzare la fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="222ba-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="222ba-107">La fase mosaico è la seconda delle tre fasi che interagiscono con conteggiarla suddividerla o affiancano una superficie.</span><span class="sxs-lookup"><span data-stu-id="222ba-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="222ba-108">La prima fase è la fase Hull shader; funziona una volta per patch e configura il comportamento della fase successiva (funzione fissa mosaico).</span><span class="sxs-lookup"><span data-stu-id="222ba-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="222ba-109">Uno scafo shader genera anche output definiti dall'utente, ad esempio punti di controllo di output e costanti di patch, che vengono inviati oltre il mosaico direttamente alla terza fase, ovvero la fase di shader del dominio.</span><span class="sxs-lookup"><span data-stu-id="222ba-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="222ba-110">Un Domain shader viene richiamato una volta per ogni punto di mosaico e valuta le posizioni della superficie.</span><span class="sxs-lookup"><span data-stu-id="222ba-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="222ba-111">La fase mosaico è una fase di funzione fissa, non sono presenti shader da generare e nessun stato da impostare.</span><span class="sxs-lookup"><span data-stu-id="222ba-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="222ba-112">Riceve tutto lo stato di installazione dalla fase dello scafo dello shader. una volta inizializzata la fase Hull shader, la fase mosaico viene inizializzata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="222ba-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="222ba-113">**Per inizializzare la fase mosaico**</span><span class="sxs-lookup"><span data-stu-id="222ba-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="222ba-114">Inizializzare la fase Hull shader con [**sul ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="222ba-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="222ba-115">*ppClassInstances* è un puntatore a una matrice di interfacce dello shader, rappresentata da puntatori [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) e dal numero di interfacce, rappresentate da *NumClassInstances*.</span><span class="sxs-lookup"><span data-stu-id="222ba-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="222ba-116">Se non viene usato, questi parametri possono essere impostati rispettivamente su **null** e 0.</span><span class="sxs-lookup"><span data-stu-id="222ba-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="222ba-117">Dopo l'inizializzazione della fase Hull shader, è necessario inizializzare anche la fase Domain-shader.</span><span class="sxs-lookup"><span data-stu-id="222ba-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="222ba-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="222ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222ba-119">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="222ba-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="222ba-120">Panoramica dello schema a mosaico</span><span class="sxs-lookup"><span data-stu-id="222ba-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




