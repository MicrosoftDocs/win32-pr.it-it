---
description: Queste costanti si applicano alle variabili di effetto.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Costanti D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304718"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="5552a-103">Costanti della variabile di \_ effetto D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="5552a-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="5552a-104">Queste costanti si applicano alle variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="5552a-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="5552a-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="5552a-105">\#define</span></span>                                       | <span data-ttu-id="5552a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5552a-106">Description</span></span>  | <span data-ttu-id="5552a-107">Valore</span><span class="sxs-lookup"><span data-stu-id="5552a-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5552a-108">\_ \_ Annotazione variabile effetto D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="5552a-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="5552a-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="5552a-109">1 << 0</span></span> | <span data-ttu-id="5552a-110">Indica che si tratta di un'annotazione o una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="5552a-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="5552a-111">\_Variabile effetto d3d10 in \_ \_ pool</span><span class="sxs-lookup"><span data-stu-id="5552a-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="5552a-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="5552a-112">1 << 1</span></span> | <span data-ttu-id="5552a-113">Indica che la variabile o il buffer costante si trova in un pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="5552a-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="5552a-114">Se questo flag non è impostato, la variabile si trova in un effetto autonomo o un effetto figlio (gli effetti autonomi restituiscono false da [**ID3D10Effect:: il pool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span><span class="sxs-lookup"><span data-stu-id="5552a-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="5552a-115">\_Punto di \_ \_ Binding esplicito variabile \_ effetto D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="5552a-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="5552a-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="5552a-116">1 << 2</span></span> | <span data-ttu-id="5552a-117">Indica che la variabile è stata associata in modo esplicito tramite la parola chiave register.</span><span class="sxs-lookup"><span data-stu-id="5552a-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="5552a-118">Questi flag sono definiti come macro in d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="5552a-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5552a-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5552a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5552a-120">Costanti effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5552a-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



