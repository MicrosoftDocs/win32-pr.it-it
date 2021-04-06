---
title: Metodo OnWarning IMsTscAxEvents
description: Chiamato quando il controllo client rileva una condizione di errore non irreversibile.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Metodo OnWarning Servizi Desktop remoto
- Metodo OnWarning Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, Metodo OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742082"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="bf0ea-106">Metodo IMsTscAxEvents:: OnWarning</span><span class="sxs-lookup"><span data-stu-id="bf0ea-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="bf0ea-107">Chiamato quando il controllo client rileva una condizione di errore non irreversibile.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0ea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf0ea-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="bf0ea-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf0ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0ea-110">*WarningCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf0ea-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf0ea-111">Codice di errore.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="bf0ea-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="bf0ea-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="bf0ea-113">Cache bitmap danneggiata.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0ea-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf0ea-114">Return value</span></span>

<span data-ttu-id="bf0ea-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bf0ea-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0ea-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf0ea-116">Remarks</span></span>

<span data-ttu-id="bf0ea-117">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf0ea-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0ea-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf0ea-118">Requirements</span></span>



| <span data-ttu-id="bf0ea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf0ea-119">Requirement</span></span> | <span data-ttu-id="bf0ea-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bf0ea-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0ea-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf0ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0ea-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf0ea-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bf0ea-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf0ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0ea-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf0ea-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bf0ea-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bf0ea-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf0ea-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0ea-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf0ea-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0ea-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf0ea-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0ea-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf0ea-129">IID</span><span class="sxs-lookup"><span data-stu-id="bf0ea-129">IID</span></span><br/>                      | <span data-ttu-id="bf0ea-130">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="bf0ea-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bf0ea-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf0ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf0ea-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="bf0ea-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





