---
description: L'API Direct3D definisce diversi elementi API per semplificare la creazione e la gestione del sistema di effetti.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Guida di riferimento agli effetti (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966102"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="1e31f-103">Guida di riferimento agli effetti (grafica Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1e31f-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="1e31f-104">L'API Direct3D definisce diversi elementi API per semplificare la creazione e la gestione del sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="1e31f-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="1e31f-105">Interfacce</span><span class="sxs-lookup"><span data-stu-id="1e31f-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="1e31f-106">Funzioni</span><span class="sxs-lookup"><span data-stu-id="1e31f-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="1e31f-107">Strutture</span><span class="sxs-lookup"><span data-stu-id="1e31f-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="1e31f-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="1e31f-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="1e31f-109">Il sistema di effetti incapsula le assegnazioni di stato in un effetto.</span><span class="sxs-lookup"><span data-stu-id="1e31f-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="1e31f-110">Ogni effetto è una raccolta dello stato della pipeline che può essere suddivisa in assegnazioni di stato usando blocchi di stato, risorse e shader.</span><span class="sxs-lookup"><span data-stu-id="1e31f-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="1e31f-111">A seconda delle dimensioni di un effetto, è possibile scegliere di implementarne una in una stringa di testo ASCII o un file di effetti (. FX).</span><span class="sxs-lookup"><span data-stu-id="1e31f-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="1e31f-112">Per organizzare le informazioni in un effetto, vedere il [formato dell'effetto](d3d10-effect-format.md).</span><span class="sxs-lookup"><span data-stu-id="1e31f-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="1e31f-113">Avendo progettato un effetto, usare l'API Effect per impostare lo stato nel dispositivo durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="1e31f-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="1e31f-114">Inoltre, il sistema degli effetti supporta una serie di API di reflection per ottenere e impostare i dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="1e31f-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="1e31f-115">Per altre informazioni, vedere [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="1e31f-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e31f-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e31f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e31f-117">Riferimento a Direct3D</span><span class="sxs-lookup"><span data-stu-id="1e31f-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



