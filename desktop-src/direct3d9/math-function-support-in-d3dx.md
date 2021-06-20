---
description: Informazioni sul supporto delle funzioni matematiche in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Supporto delle funzioni matematiche in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407524"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="67b1e-105">Supporto delle funzioni matematiche in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="67b1e-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="67b1e-106">D3DX è una libreria di utilità che fornisce servizi helper.</span><span class="sxs-lookup"><span data-stu-id="67b1e-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="67b1e-107">Si tratta di un livello sopra il componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="67b1e-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="67b1e-108">Math</span><span class="sxs-lookup"><span data-stu-id="67b1e-108">Math</span></span>

<span data-ttu-id="67b1e-109">Il supporto matematico, contenuto in un set di funzioni, viene fornito per:</span><span class="sxs-lookup"><span data-stu-id="67b1e-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="67b1e-110">Calcoli dei colori</span><span class="sxs-lookup"><span data-stu-id="67b1e-110">Color calculations</span></span>
-   <span data-ttu-id="67b1e-111">Aerei</span><span class="sxs-lookup"><span data-stu-id="67b1e-111">Planes</span></span>
-   <span data-ttu-id="67b1e-112">Manipolazione della matrice</span><span class="sxs-lookup"><span data-stu-id="67b1e-112">Matrix manipulation</span></span>
-   <span data-ttu-id="67b1e-113">Quaternioni</span><span class="sxs-lookup"><span data-stu-id="67b1e-113">Quaternions</span></span>
-   <span data-ttu-id="67b1e-114">Vettori 2D</span><span class="sxs-lookup"><span data-stu-id="67b1e-114">2D vectors</span></span>
-   <span data-ttu-id="67b1e-115">Vettori 3D</span><span class="sxs-lookup"><span data-stu-id="67b1e-115">3D vectors</span></span>
-   <span data-ttu-id="67b1e-116">Vettori 4D</span><span class="sxs-lookup"><span data-stu-id="67b1e-116">4D vectors</span></span>

<span data-ttu-id="67b1e-117">Si noti che, se associato con gli overload di C++, il supporto per i tipi matematici 3D di base è ampio.</span><span class="sxs-lookup"><span data-stu-id="67b1e-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="67b1e-118">Per altre informazioni su queste funzioni, vedere [Funzioni D3DX.](dx9-graphics-reference-d3dx-functions.md)</span><span class="sxs-lookup"><span data-stu-id="67b1e-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="67b1e-119">Per facilitare l'individuazione della funzione necessaria, queste vengono suddivise in diverse cartelle.</span><span class="sxs-lookup"><span data-stu-id="67b1e-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="67b1e-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="67b1e-120">FLOAT16</span></span>

<span data-ttu-id="67b1e-121">Quando si usa il tipo di dati FLOAT16, assicurarsi di limitare i valori a un massimo di D3DX \_ 16F \_ MAX.</span><span class="sxs-lookup"><span data-stu-id="67b1e-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="67b1e-122">Qualsiasi valore FLOAT16 che supera questo valore comporta un comportamento non definito nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="67b1e-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="67b1e-123">Vedere [Altre costanti D3DX.](other-d3dx-constants.md)</span><span class="sxs-lookup"><span data-stu-id="67b1e-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67b1e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67b1e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b1e-125">D3DX</span><span class="sxs-lookup"><span data-stu-id="67b1e-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



