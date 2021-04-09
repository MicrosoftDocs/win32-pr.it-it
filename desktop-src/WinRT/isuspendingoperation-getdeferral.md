---
description: Richiede che l'operazione di sospensione dell'app venga posticipata.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Metodo ISuspendingOperation:: getrinvio (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879254"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="1a063-103">Metodo ISuspendingOperation:: getrinvio</span><span class="sxs-lookup"><span data-stu-id="1a063-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="1a063-104">Richiede che l'operazione di sospensione dell'app venga posticipata.</span><span class="sxs-lookup"><span data-stu-id="1a063-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a063-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a063-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="1a063-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a063-107">*rinvio* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1a063-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1a063-108">Sospensione di rinvio.</span><span class="sxs-lookup"><span data-stu-id="1a063-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a063-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a063-109">Return value</span></span>

<span data-ttu-id="1a063-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a063-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a063-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a063-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a063-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a063-112">Requirements</span></span>



| <span data-ttu-id="1a063-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a063-113">Requirement</span></span> | <span data-ttu-id="1a063-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1a063-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a063-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a063-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1a063-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1a063-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1a063-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a063-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1a063-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a063-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1a063-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a063-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a063-120"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a063-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a063-121">IDL</span><span class="sxs-lookup"><span data-stu-id="1a063-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a063-122"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a063-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a063-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a063-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a063-124">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="1a063-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




