---
description: Aggiunge un oggetto IContextNode alla raccolta.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: 'Metodo IContextNodes:: AddContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.AddContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 18a7438c09fb2a850637bbae549ada61c37fb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129486"
---
# <a name="icontextnodesaddcontextnode-method"></a><span data-ttu-id="b146e-103">Metodo IContextNodes:: AddContextNode</span><span class="sxs-lookup"><span data-stu-id="b146e-103">IContextNodes::AddContextNode method</span></span>

<span data-ttu-id="b146e-104">Aggiunge un oggetto [**IContextNode**](icontextnode.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="b146e-104">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b146e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b146e-105">Syntax</span></span>


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="b146e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b146e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b146e-107">*pContextNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b146e-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b146e-108">Oggetto [**IContextNode**](icontextnode.md) da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b146e-108">The [**IContextNode**](icontextnode.md) object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b146e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b146e-109">Return value</span></span>

<span data-ttu-id="b146e-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b146e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b146e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b146e-111">Requirements</span></span>



| <span data-ttu-id="b146e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b146e-112">Requirement</span></span> | <span data-ttu-id="b146e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b146e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b146e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b146e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b146e-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b146e-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b146e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b146e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b146e-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b146e-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b146e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b146e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b146e-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b146e-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b146e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b146e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b146e-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b146e-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b146e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b146e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b146e-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="b146e-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="b146e-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b146e-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




