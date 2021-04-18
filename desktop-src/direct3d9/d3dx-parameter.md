---
description: Questi flag forniscono informazioni aggiuntive sui parametri di effetto.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322893"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="76453-103">\_Parametro D3DX</span><span class="sxs-lookup"><span data-stu-id="76453-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="76453-104">Questi flag forniscono informazioni aggiuntive sui parametri di effetto.</span><span class="sxs-lookup"><span data-stu-id="76453-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="76453-105">Le costanti del parametro Effect vengono usate da [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="76453-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="76453-106">Costante</span><span class="sxs-lookup"><span data-stu-id="76453-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="76453-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76453-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="76453-108"><dt>**\_Annotazione del parametro D3DX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76453-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="76453-109">Questo parametro è contrassegnato come annotazione.</span><span class="sxs-lookup"><span data-stu-id="76453-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="76453-110">Vedere [aggiungere informazioni ai parametri di effetto con le annotazioni](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="76453-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="76453-111"><dt>**\_ \_ Valore letterale parametro D3DX**</dt></span><span class="sxs-lookup"><span data-stu-id="76453-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="76453-112">Questo parametro è contrassegnato come valore letterale.</span><span class="sxs-lookup"><span data-stu-id="76453-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="76453-113">I parametri letterali non possono essere modificati dopo la compilazione, consentendo al compilatore di ottimizzare l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="76453-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="76453-114">I parametri condivisi non possono essere contrassegnati come valori letterali.</span><span class="sxs-lookup"><span data-stu-id="76453-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="76453-115">Vedere [utilizzi e valori letterali (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="76453-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="76453-116"><dt>**\_Parametro D3DX \_ condiviso**</dt></span><span class="sxs-lookup"><span data-stu-id="76453-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="76453-117">Il valore di un parametro verrà condiviso da tutti gli effetti nello stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="76453-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="76453-118">Se si modifica il valore in un effetto, questo verrà modificato in tutti gli effetti condivisi.</span><span class="sxs-lookup"><span data-stu-id="76453-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="76453-119">Vedere [condivisione di parametri](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="76453-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="76453-120">**D3DX \_ Impossibile combinare il parametro \_ Shared** con l' **\_ \_ annotazione** del parametro D3DX o D3DX. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="76453-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="76453-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76453-121">Requirements</span></span>



| <span data-ttu-id="76453-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76453-122">Requirement</span></span> | <span data-ttu-id="76453-123">Valore</span><span class="sxs-lookup"><span data-stu-id="76453-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76453-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76453-124">Header</span></span><br/> | <dl> <span data-ttu-id="76453-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="76453-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76453-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76453-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76453-127">Costanti effetto</span><span class="sxs-lookup"><span data-stu-id="76453-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




