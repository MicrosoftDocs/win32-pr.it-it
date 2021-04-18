---
description: Notifica al sistema che l'app ha salvato i dati ed è pronta per essere sospesa.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'Metodo ISuspendingDeferral:: complete (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307072"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="e584a-103">Metodo ISuspendingDeferral:: complete</span><span class="sxs-lookup"><span data-stu-id="e584a-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="e584a-104">Notifica al sistema che l'app ha salvato i dati ed è pronta per essere sospesa.</span><span class="sxs-lookup"><span data-stu-id="e584a-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="e584a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e584a-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="e584a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e584a-106">Parameters</span></span>

<span data-ttu-id="e584a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e584a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e584a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e584a-108">Return value</span></span>

<span data-ttu-id="e584a-109">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e584a-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e584a-110">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e584a-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e584a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e584a-111">Requirements</span></span>



| <span data-ttu-id="e584a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e584a-112">Requirement</span></span> | <span data-ttu-id="e584a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e584a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e584a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e584a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e584a-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e584a-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e584a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e584a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e584a-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e584a-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e584a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e584a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e584a-119"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="e584a-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="e584a-120">IDL</span><span class="sxs-lookup"><span data-stu-id="e584a-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e584a-121"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e584a-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e584a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e584a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e584a-123">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="e584a-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




