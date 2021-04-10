---
description: Scarica la cache per la compatibilità delle applicazioni.
ms.assetid: 03f47813-87f6-4b71-b453-77a2facab019
title: BaseFlushAppcompatCache (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BaseFlushAppcompatCache
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-appcompat-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-appcompat-l1-1-1.dll
ms.openlocfilehash: 6118c78784bb96b9f25e008cd2221112eeb646f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126213"
---
# <a name="baseflushappcompatcache-function"></a><span data-ttu-id="6869b-103">BaseFlushAppcompatCache (funzione)</span><span class="sxs-lookup"><span data-stu-id="6869b-103">BaseFlushAppcompatCache function</span></span>

<span data-ttu-id="6869b-104">Scarica la cache per la compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6869b-104">Flushes the application compatibility cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="6869b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6869b-105">Syntax</span></span>


```C++
BOOL WINAPI BaseFlushAppcompatCache(void);
```



## <a name="parameters"></a><span data-ttu-id="6869b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6869b-106">Parameters</span></span>

<span data-ttu-id="6869b-107">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6869b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6869b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6869b-108">Return value</span></span>

<span data-ttu-id="6869b-109">La funzione restituisce **true** se ha esito positivo e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6869b-109">The function returns **TRUE** if it succeeds and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6869b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6869b-110">Remarks</span></span>

<span data-ttu-id="6869b-111">Il chiamante deve essere un amministratore.</span><span class="sxs-lookup"><span data-stu-id="6869b-111">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6869b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6869b-112">Requirements</span></span>



| <span data-ttu-id="6869b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6869b-113">Requirement</span></span> | <span data-ttu-id="6869b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6869b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6869b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6869b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6869b-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6869b-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6869b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6869b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6869b-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6869b-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6869b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6869b-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6869b-120"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6869b-120"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6869b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6869b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6869b-122">**ShimFlushCache**</span><span class="sxs-lookup"><span data-stu-id="6869b-122">**ShimFlushCache**</span></span>](shimflushcache.md)
</dt> </dl>

 

 




