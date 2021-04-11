---
description: Recupera il tipo di relazione rappresentata da questo IContextLink.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'Metodo IContextLink:: GetContextLinkDirection (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226167"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="40d5b-103">Metodo IContextLink:: GetContextLinkDirection</span><span class="sxs-lookup"><span data-stu-id="40d5b-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="40d5b-104">Recupera il tipo di relazione rappresentata da questo [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="40d5b-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d5b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40d5b-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="40d5b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40d5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d5b-107">*pContextLinkDirection* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="40d5b-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40d5b-108">Direzione rappresentata da questo [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="40d5b-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d5b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40d5b-109">Return value</span></span>

<span data-ttu-id="40d5b-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="40d5b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40d5b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40d5b-111">Requirements</span></span>



| <span data-ttu-id="40d5b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d5b-112">Requirement</span></span> | <span data-ttu-id="40d5b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="40d5b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40d5b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d5b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="40d5b-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="40d5b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="40d5b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d5b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="40d5b-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="40d5b-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="40d5b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40d5b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d5b-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="40d5b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="40d5b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d5b-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="40d5b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40d5b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d5b-123">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="40d5b-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="40d5b-124">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="40d5b-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="40d5b-125">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="40d5b-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




