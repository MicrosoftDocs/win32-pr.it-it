---
title: Funzione FreeUiInfo (Ndattributils. h)
description: Consente di deallocare la memoria allocata internamente a una struttura UiInfo.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- FreeUiInfo funzione NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119391"
---
# <a name="freeuiinfo-function"></a><span data-ttu-id="09fec-104">FreeUiInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="09fec-104">FreeUiInfo function</span></span>

<span data-ttu-id="09fec-105">La funzione **FreeUiInfo** consente di deallocare la memoria allocata internamente a una struttura [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) .</span><span class="sxs-lookup"><span data-stu-id="09fec-105">The **FreeUiInfo** function deallocates the memory allocated internally to a [**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) structure.</span></span> <span data-ttu-id="09fec-106">Questa funzione chiama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) per deallocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="09fec-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09fec-107">Syntax</span></span>


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="09fec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09fec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fec-109">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09fec-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fec-110">Tipo: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="09fec-110">Type: \**[**UiInfo**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\** _</span></span>

<span data-ttu-id="09fec-111">Struttura.</span><span class="sxs-lookup"><span data-stu-id="09fec-111">The structure.</span></span> <span data-ttu-id="09fec-112">La memoria allocata a cui fa riferimento questa struttura verrà liberata.</span><span class="sxs-lookup"><span data-stu-id="09fec-112">The allocated memory pointed to by this structure will be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fec-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09fec-113">Return value</span></span>

<span data-ttu-id="09fec-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="09fec-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fec-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09fec-115">Requirements</span></span>



| <span data-ttu-id="09fec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fec-116">Requirement</span></span> | <span data-ttu-id="09fec-117">Valore</span><span class="sxs-lookup"><span data-stu-id="09fec-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="09fec-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09fec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09fec-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09fec-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="09fec-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09fec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09fec-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09fec-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="09fec-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09fec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fec-123"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fec-123"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09fec-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09fec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fec-125">_ *UiInfo*\*</span><span class="sxs-lookup"><span data-stu-id="09fec-125">_ *UiInfo*\*</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[<span data-ttu-id="09fec-126">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="09fec-126">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

