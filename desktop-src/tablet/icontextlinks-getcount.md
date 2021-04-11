---
description: Ottiene il numero di oggetti IContextLink nell'insieme.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'Metodo IContextLinks:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226165"
---
# <a name="icontextlinksgetcount-method"></a><span data-ttu-id="908f6-103">Metodo IContextLinks:: GetCount</span><span class="sxs-lookup"><span data-stu-id="908f6-103">IContextLinks::GetCount method</span></span>

<span data-ttu-id="908f6-104">Ottiene il numero di oggetti [**IContextLink**](icontextlink.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="908f6-104">Gets the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="908f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="908f6-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="908f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="908f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908f6-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="908f6-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="908f6-108">Numero di oggetti [**IContextLink**](icontextlink.md) contenuti in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="908f6-108">The number of [**IContextLink**](icontextlink.md) objects that are contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="908f6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="908f6-109">Return value</span></span>

<span data-ttu-id="908f6-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="908f6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="908f6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="908f6-111">Requirements</span></span>



| <span data-ttu-id="908f6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="908f6-112">Requirement</span></span> | <span data-ttu-id="908f6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="908f6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="908f6-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="908f6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="908f6-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="908f6-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="908f6-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="908f6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="908f6-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="908f6-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="908f6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="908f6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="908f6-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="908f6-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="908f6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="908f6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="908f6-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="908f6-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="908f6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="908f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908f6-123">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="908f6-123">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="908f6-124">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="908f6-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




