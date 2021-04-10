---
description: I parametri sono variabili di effetto.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parametri (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125583"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="13a7e-103">Parametri (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="13a7e-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="13a7e-104">I parametri sono variabili di effetto.</span><span class="sxs-lookup"><span data-stu-id="13a7e-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a7e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13a7e-105">Syntax</span></span>

<span data-ttu-id="13a7e-106">*ID tipo di utilizzo* \[ : espressione di  \] \[ < *annotazione* semantica > \] \[ =   \] .</span><span class="sxs-lookup"><span data-stu-id="13a7e-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="13a7e-107">I parametri possono essere letti e scritti dall'applicazione con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="13a7e-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="13a7e-108">È possibile fare riferimento ai parametri nelle funzioni e nelle tecniche, in particolare nel lato destro delle assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="13a7e-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="13a7e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="13a7e-109">Item</span></span>                                                                                 | <span data-ttu-id="13a7e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13a7e-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a7e-111"><span id="usage"></span><span id="USAGE"></span>*utilizzo*</span><span class="sxs-lookup"><span data-stu-id="13a7e-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="13a7e-112">Ambito del parametro.</span><span class="sxs-lookup"><span data-stu-id="13a7e-112">Scope of the parameter.</span></span> <span data-ttu-id="13a7e-113">Vedere [utilizzi e valori letterali (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="13a7e-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="13a7e-114"><span id="type"></span><span id="TYPE"></span>*tipo*</span><span class="sxs-lookup"><span data-stu-id="13a7e-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="13a7e-115">Qualsiasi [riferimento valido per](../direct3dhlsl/dx-graphics-hlsl-reference.md) il tipo HLSL.</span><span class="sxs-lookup"><span data-stu-id="13a7e-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="13a7e-116"><span id="ID"></span><span id="id"></span>*ID*</span><span class="sxs-lookup"><span data-stu-id="13a7e-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="13a7e-117">Un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="13a7e-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="13a7e-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantica*</span><span class="sxs-lookup"><span data-stu-id="13a7e-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="13a7e-119">Tag che segue le regole dell'identificatore che in genere indicano l'uso del parametro.</span><span class="sxs-lookup"><span data-stu-id="13a7e-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="13a7e-120">Deve essere un tipo particolare.</span><span class="sxs-lookup"><span data-stu-id="13a7e-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="13a7e-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotazioni*</span><span class="sxs-lookup"><span data-stu-id="13a7e-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="13a7e-122">Zero o più elementi di informazioni specifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="13a7e-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="13a7e-123">Può essere qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="13a7e-123">May be any type.</span></span> <span data-ttu-id="13a7e-124">Vedere [aggiungere informazioni ai parametri di effetto con le annotazioni](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="13a7e-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="13a7e-125"><span id="expression"></span><span id="EXPRESSION"></span>*espressione*</span><span class="sxs-lookup"><span data-stu-id="13a7e-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="13a7e-126">Inizializza il valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="13a7e-126">Initializes the parameter's value.</span></span> <span data-ttu-id="13a7e-127">Vedere [espressioni (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="13a7e-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="13a7e-128">I parametri possono essere inizializzati in qualsiasi [riferimento valido per](../direct3dhlsl/dx-graphics-hlsl-reference.md) l'espressione HLSL che si riduce a un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="13a7e-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="13a7e-129">I valori dei parametri non vengono modificati dall'esecuzione dell'assegnazione di stato o delle chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="13a7e-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13a7e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13a7e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13a7e-131">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="13a7e-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
