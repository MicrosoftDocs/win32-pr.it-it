---
description: Ottiene il risultato di un'azione asincrona.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'Metodo IAsyncAction:: GetResults'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226101"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="1151e-103">Metodo IAsyncAction:: GetResults</span><span class="sxs-lookup"><span data-stu-id="1151e-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="1151e-104">Ottiene il risultato di un'azione asincrona.</span><span class="sxs-lookup"><span data-stu-id="1151e-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="1151e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1151e-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="1151e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1151e-106">Parameters</span></span>

<span data-ttu-id="1151e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1151e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1151e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1151e-108">Return value</span></span>

<span data-ttu-id="1151e-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1151e-109">Type: **HRESULT**</span></span>

<span data-ttu-id="1151e-110">Questo metodo restituisce sempre **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1151e-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1151e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1151e-111">Remarks</span></span>

<span data-ttu-id="1151e-112">La chiamata al metodo **GetResults** non produce alcun effetto se l'implementazione corrente ha un tipo dinamico di [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span><span class="sxs-lookup"><span data-stu-id="1151e-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="1151e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1151e-113">Requirements</span></span>



| <span data-ttu-id="1151e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1151e-114">Requirement</span></span> | <span data-ttu-id="1151e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1151e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1151e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1151e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1151e-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1151e-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="1151e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1151e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1151e-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1151e-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="1151e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1151e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1151e-121"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1151e-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1151e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1151e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1151e-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="1151e-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
