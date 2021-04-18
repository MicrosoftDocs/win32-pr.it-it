---
title: Metodo IMsTscAxEvents OnUserNameAcquired
description: Chiamato quando il nome utente è stato acquisito dal controllo.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnUserNameAcquired
- Metodo OnUserNameAcquired Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnUserNameAcquired
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301876"
---
# <a name="imstscaxeventsonusernameacquired-method"></a><span data-ttu-id="113b5-106">Metodo IMsTscAxEvents:: OnUserNameAcquired</span><span class="sxs-lookup"><span data-stu-id="113b5-106">IMsTscAxEvents::OnUserNameAcquired method</span></span>

<span data-ttu-id="113b5-107">Chiamato quando il nome utente è stato acquisito dal controllo.</span><span class="sxs-lookup"><span data-stu-id="113b5-107">Called when the user name has been acquired by the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="113b5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="113b5-108">Syntax</span></span>


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a><span data-ttu-id="113b5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="113b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="113b5-110">*bstrUserName*</span><span class="sxs-lookup"><span data-stu-id="113b5-110">*bstrUserName*</span></span> 
</dt> <dd>

<span data-ttu-id="113b5-111">Nome utente.</span><span class="sxs-lookup"><span data-stu-id="113b5-111">The user name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="113b5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="113b5-112">Return value</span></span>

<span data-ttu-id="113b5-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="113b5-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="113b5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113b5-114">Requirements</span></span>



| <span data-ttu-id="113b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="113b5-115">Requirement</span></span> | <span data-ttu-id="113b5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="113b5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="113b5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="113b5-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="113b5-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="113b5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="113b5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="113b5-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="113b5-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="113b5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="113b5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="113b5-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="113b5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="113b5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="113b5-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="113b5-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="113b5-125">IID</span><span class="sxs-lookup"><span data-stu-id="113b5-125">IID</span></span><br/>                      | <span data-ttu-id="113b5-126">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="113b5-126">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="113b5-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113b5-128">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="113b5-128">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





