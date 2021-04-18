---
description: Rimuove un oggetto IContextNode da questa raccolta.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'Metodo IContextNodes:: RemoveContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307412"
---
# <a name="icontextnodesremovecontextnode-method"></a><span data-ttu-id="c8ea0-103">Metodo IContextNodes:: RemoveContextNode</span><span class="sxs-lookup"><span data-stu-id="c8ea0-103">IContextNodes::RemoveContextNode method</span></span>

<span data-ttu-id="c8ea0-104">Rimuove un oggetto [**IContextNode**](icontextnode.md) da questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="c8ea0-104">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ea0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8ea0-105">Syntax</span></span>


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="c8ea0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8ea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ea0-107">*pContextNode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8ea0-107">*pContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ea0-108">Oggetto [**IContextNode**](icontextnode.md) da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c8ea0-108">The [**IContextNode**](icontextnode.md) object to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ea0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8ea0-109">Return value</span></span>

<span data-ttu-id="c8ea0-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c8ea0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ea0-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8ea0-111">Requirements</span></span>



| <span data-ttu-id="c8ea0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8ea0-112">Requirement</span></span> | <span data-ttu-id="c8ea0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c8ea0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ea0-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8ea0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ea0-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c8ea0-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8ea0-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8ea0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ea0-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c8ea0-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c8ea0-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8ea0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ea0-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea0-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c8ea0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c8ea0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8ea0-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8ea0-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c8ea0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8ea0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ea0-123">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="c8ea0-123">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="c8ea0-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c8ea0-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




