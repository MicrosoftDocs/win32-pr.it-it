---
description: Rilascia le risorse usate dalla funzione SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049143"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="4ec57-103">SdbReleaseMatchingExe (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ec57-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="4ec57-104">Rilascia le risorse usate dalla funzione [**SdbGetMatchingExe**](sdbgetmatchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec57-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec57-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ec57-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="4ec57-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ec57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec57-107">*hSDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ec57-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec57-108">Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec57-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4ec57-109">*trExe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ec57-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec57-110">[**TAGREF**](tagref.md) restituito da [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span><span class="sxs-lookup"><span data-stu-id="4ec57-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec57-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ec57-111">Return value</span></span>

<span data-ttu-id="4ec57-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4ec57-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec57-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ec57-113">Requirements</span></span>



| <span data-ttu-id="4ec57-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec57-114">Requirement</span></span> | <span data-ttu-id="4ec57-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4ec57-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec57-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec57-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec57-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ec57-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4ec57-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec57-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec57-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ec57-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4ec57-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4ec57-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ec57-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec57-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec57-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ec57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec57-123">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="4ec57-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="4ec57-124">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="4ec57-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




