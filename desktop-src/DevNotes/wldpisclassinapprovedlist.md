---
description: Chiama la libreria per verificare se un particolare CLSID è sicuro da chiamare.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Funzione WldpIsClassInApprovedList (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125856"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="fb1f3-103">WldpIsClassInApprovedList (funzione)</span><span class="sxs-lookup"><span data-stu-id="fb1f3-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="fb1f3-104">Chiama la libreria per verificare se un particolare **CLSID** è sicuro da chiamare.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="fb1f3-105">Alla funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-105">The function has no associated import library.</span></span> <span data-ttu-id="fb1f3-106">È necessario utilizzare le funzioni LoadLibrary e GetProcAddress per collegare dinamicamente a wldp.dll.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1f3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb1f3-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fb1f3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb1f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1f3-109">*classID*</span><span class="sxs-lookup"><span data-stu-id="fb1f3-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1f3-110">ID della classe COM di cui verificare l'approvazione.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="fb1f3-111">*hostInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb1f3-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1f3-112">Struttura [**di \_ \_ informazioni sull'host WLDP**](wldp-host-information.md) che identifica l'host da valutare.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="fb1f3-113">*approvato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb1f3-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1f3-114">Al termine, contiene **true** se l'ID di classe è approvato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fb1f3-115">*optionalFlags*</span><span class="sxs-lookup"><span data-stu-id="fb1f3-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1f3-116">Questo parametro è riservato e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1f3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb1f3-117">Return value</span></span>

<span data-ttu-id="fb1f3-118">Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="fb1f3-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1f3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb1f3-119">Requirements</span></span>



| <span data-ttu-id="fb1f3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1f3-120">Requirement</span></span> | <span data-ttu-id="fb1f3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fb1f3-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1f3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb1f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1f3-123">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fb1f3-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fb1f3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb1f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1f3-125">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="fb1f3-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fb1f3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb1f3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb1f3-127"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb1f3-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb1f3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fb1f3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb1f3-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb1f3-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




