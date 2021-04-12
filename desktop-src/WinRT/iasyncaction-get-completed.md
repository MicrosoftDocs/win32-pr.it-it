---
description: Ottiene il metodo chiamato al completamento dell'azione asincrona.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Metodo IAsyncAction:: get_Completed'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129239"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="94e9e-103">Metodo IAsyncAction:: Get \_ Completed</span><span class="sxs-lookup"><span data-stu-id="94e9e-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="94e9e-104">Ottiene il metodo chiamato al completamento dell'azione asincrona.</span><span class="sxs-lookup"><span data-stu-id="94e9e-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94e9e-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="94e9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94e9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94e9e-107">*gestore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="94e9e-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94e9e-108">Tipo: **[ **asyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="94e9e-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="94e9e-109">Metodo che gestisce la notifica di completamento.</span><span class="sxs-lookup"><span data-stu-id="94e9e-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94e9e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94e9e-110">Return value</span></span>

<span data-ttu-id="94e9e-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="94e9e-111">Type: **HRESULT**</span></span>

<span data-ttu-id="94e9e-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="94e9e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="94e9e-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94e9e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e9e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94e9e-114">Requirements</span></span>



| <span data-ttu-id="94e9e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e9e-115">Requirement</span></span> | <span data-ttu-id="94e9e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="94e9e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e9e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94e9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="94e9e-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="94e9e-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="94e9e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94e9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="94e9e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="94e9e-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="94e9e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94e9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="94e9e-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94e9e-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e9e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94e9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e9e-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="94e9e-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
