---
description: D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Supporto della funzione Math in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124476"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="6378a-104">Supporto della funzione Math in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6378a-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="6378a-105">D3DX è una libreria di utilità che fornisce servizi di supporto.</span><span class="sxs-lookup"><span data-stu-id="6378a-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="6378a-106">Si tratta di un livello sopra il componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6378a-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="6378a-107">Math</span><span class="sxs-lookup"><span data-stu-id="6378a-107">Math</span></span>

<span data-ttu-id="6378a-108">Il supporto matematico, contenuto in un set di funzioni, è disponibile per:</span><span class="sxs-lookup"><span data-stu-id="6378a-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="6378a-109">Calcoli colori</span><span class="sxs-lookup"><span data-stu-id="6378a-109">Color calculations</span></span>
-   <span data-ttu-id="6378a-110">Aerei</span><span class="sxs-lookup"><span data-stu-id="6378a-110">Planes</span></span>
-   <span data-ttu-id="6378a-111">Manipolazione della matrice</span><span class="sxs-lookup"><span data-stu-id="6378a-111">Matrix manipulation</span></span>
-   <span data-ttu-id="6378a-112">Quaternioni</span><span class="sxs-lookup"><span data-stu-id="6378a-112">Quaternions</span></span>
-   <span data-ttu-id="6378a-113">vettori 2D</span><span class="sxs-lookup"><span data-stu-id="6378a-113">2D vectors</span></span>
-   <span data-ttu-id="6378a-114">vettori 3D</span><span class="sxs-lookup"><span data-stu-id="6378a-114">3D vectors</span></span>
-   <span data-ttu-id="6378a-115">vettori 4D</span><span class="sxs-lookup"><span data-stu-id="6378a-115">4D vectors</span></span>

<span data-ttu-id="6378a-116">Si noti che, quando abbinato agli overload C++, il supporto per i tipi matematici 3D di base è esteso.</span><span class="sxs-lookup"><span data-stu-id="6378a-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="6378a-117">Per ulteriori informazioni su queste funzioni, vedere [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6378a-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="6378a-118">Per individuare la funzione di cui si ha bisogno, vengono suddivise in diverse cartelle.</span><span class="sxs-lookup"><span data-stu-id="6378a-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="6378a-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6378a-119">FLOAT16</span></span>

<span data-ttu-id="6378a-120">Quando si usa il tipo di dati FLOAT16, assicurarsi di limitare i valori a un massimo di D3DX \_ 16F \_ max.</span><span class="sxs-lookup"><span data-stu-id="6378a-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="6378a-121">Qualsiasi valore di FLOAT16 che supera questa operazione determinerà un comportamento indefinito nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="6378a-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="6378a-122">Vedere [altre costanti D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6378a-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6378a-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6378a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6378a-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="6378a-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



