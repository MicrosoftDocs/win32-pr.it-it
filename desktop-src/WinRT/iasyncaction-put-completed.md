---
description: Imposta il metodo che viene chiamato quando l'azione asincrona viene completata.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction::p ut_Completed metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966689"
---
# <a name="iasyncactionput_completed-method"></a><span data-ttu-id="830b5-103">IAsyncAction: metodo:p UT \_ completato</span><span class="sxs-lookup"><span data-stu-id="830b5-103">IAsyncAction::put\_Completed method</span></span>

<span data-ttu-id="830b5-104">Imposta il metodo che viene chiamato quando l'azione asincrona viene completata.</span><span class="sxs-lookup"><span data-stu-id="830b5-104">Sets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="830b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="830b5-105">Syntax</span></span>


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a><span data-ttu-id="830b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="830b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="830b5-107">*gestore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="830b5-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="830b5-108">Tipo: \**[**asyncActionCompletedHandler**](asyncactioncompletedhandler.md) \** _</span><span class="sxs-lookup"><span data-stu-id="830b5-108">Type: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\** _</span></span>

<span data-ttu-id="830b5-109">Metodo che gestisce la notifica di completamento.</span><span class="sxs-lookup"><span data-stu-id="830b5-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="830b5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="830b5-110">Return value</span></span>

<span data-ttu-id="830b5-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="830b5-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="830b5-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="830b5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="830b5-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="830b5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="830b5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="830b5-114">Requirements</span></span>



| <span data-ttu-id="830b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="830b5-115">Requirement</span></span> | <span data-ttu-id="830b5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="830b5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="830b5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="830b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="830b5-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="830b5-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="830b5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="830b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="830b5-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="830b5-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="830b5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="830b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="830b5-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="830b5-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="830b5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="830b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="830b5-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="830b5-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
