---
description: Recupera un valore che descrive lo stato di imposizione dei criteri di Device Guard per il codice dinamico .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Funzione WldpIsDynamicCodePolicyEnabled (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125853"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="c8f02-103">WldpIsDynamicCodePolicyEnabled (funzione)</span><span class="sxs-lookup"><span data-stu-id="c8f02-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="c8f02-104">Recupera un valore che descrive lo stato di imposizione dei criteri di Device Guard per il codice dinamico .NET.</span><span class="sxs-lookup"><span data-stu-id="c8f02-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8f02-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="c8f02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8f02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f02-107">*IsEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8f02-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f02-108">In caso di esito positivo, restituisce **true** se i criteri di Device Guard applicano criteri di codice dinamici .NET; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c8f02-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f02-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8f02-109">Return value</span></span>

<span data-ttu-id="c8f02-110">Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="c8f02-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f02-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8f02-111">Remarks</span></span>

<span data-ttu-id="c8f02-112">Il codice dinamico si riferisce al codice generato in modo dinamico CRL .NET.</span><span class="sxs-lookup"><span data-stu-id="c8f02-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f02-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8f02-113">Requirements</span></span>



| <span data-ttu-id="c8f02-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f02-114">Requirement</span></span> | <span data-ttu-id="c8f02-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c8f02-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f02-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8f02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f02-117">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8f02-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c8f02-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8f02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f02-119">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c8f02-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c8f02-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8f02-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f02-121"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8f02-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8f02-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c8f02-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8f02-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8f02-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




