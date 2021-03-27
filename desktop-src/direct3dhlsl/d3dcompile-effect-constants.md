---
title: Costanti D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Queste costanti indirizzano il modo in cui il compilatore compila un file di effetti o il modo in cui il runtime elabora il file di effetti.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982121"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="f101a-103">\_Costanti effetto D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="f101a-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="f101a-104">Queste costanti indirizzano il modo in cui il compilatore compila un file di effetti o il modo in cui il runtime elabora il file di effetti.</span><span class="sxs-lookup"><span data-stu-id="f101a-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="f101a-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_Effetto D3DCOMPILE effetto \_ figlio \_**</span><span class="sxs-lookup"><span data-stu-id="f101a-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f101a-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="f101a-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="f101a-107">Compilare il file Effects (. FX) in un effetto figlio.</span><span class="sxs-lookup"><span data-stu-id="f101a-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="f101a-108">Gli effetti figlio non hanno inizializzatori per i valori condivisi, perché questi effetti figlio vengono inizializzati nell'effetto principale (il pool di effetti).</span><span class="sxs-lookup"><span data-stu-id="f101a-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="f101a-109">I pool di effetti sono supportati dagli effetti 10 (FX10) ma non dagli effetti 11 (FX11).</span><span class="sxs-lookup"><span data-stu-id="f101a-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="f101a-110">Per altre informazioni sulle differenze tra i pool di effetti in Direct3D 10 e sui gruppi di effetti in Direct3D 11, vedere [pool di effetti e gruppi](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span><span class="sxs-lookup"><span data-stu-id="f101a-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f101a-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ Effect \_ consente \_ \_ operazioni lente**</span><span class="sxs-lookup"><span data-stu-id="f101a-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f101a-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="f101a-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="f101a-113">Disabilita la modalità di prestazioni e consente oggetti di stato modificabili.</span><span class="sxs-lookup"><span data-stu-id="f101a-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="f101a-114">Per impostazione predefinita, è abilitata la modalità prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f101a-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="f101a-115">La modalità prestazioni non consente oggetti di stato modificabili impedendo la visualizzazione di espressioni non letterali nelle definizioni degli oggetti di stato.</span><span class="sxs-lookup"><span data-stu-id="f101a-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f101a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f101a-116">Requirements</span></span>



| <span data-ttu-id="f101a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f101a-117">Requirement</span></span> | <span data-ttu-id="f101a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f101a-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f101a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f101a-119">Header</span></span><br/> | <dl> <span data-ttu-id="f101a-120"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="f101a-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f101a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f101a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f101a-122">Costanti D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="f101a-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

