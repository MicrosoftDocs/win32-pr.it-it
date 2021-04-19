---
description: Arresta la modalità di sink Miracast, disattiva l'individuabilità e Annulla la registrazione del callback.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Funzione WFDDisplaySinkStop (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309442"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="bda6c-103">WFDDisplaySinkStop (funzione)</span><span class="sxs-lookup"><span data-stu-id="bda6c-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="bda6c-104">Arresta la modalità di sink Miracast, disattiva l'individuabilità e Annulla la registrazione del callback.</span><span class="sxs-lookup"><span data-stu-id="bda6c-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="bda6c-105">L'app dovrebbe chiamarla una volta all'arresto.</span><span class="sxs-lookup"><span data-stu-id="bda6c-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda6c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bda6c-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="bda6c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bda6c-107">Parameters</span></span>

<span data-ttu-id="bda6c-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="bda6c-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bda6c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bda6c-109">Return value</span></span>

<span data-ttu-id="bda6c-110">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bda6c-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda6c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bda6c-111">Remarks</span></span>

<span data-ttu-id="bda6c-112">Si prevede che l'app abbia sbloccato tutti i callback in corso prima di chiamare **WFDStopDisplaySink**.</span><span class="sxs-lookup"><span data-stu-id="bda6c-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda6c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda6c-113">Requirements</span></span>



| <span data-ttu-id="bda6c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda6c-114">Requirement</span></span> | <span data-ttu-id="bda6c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bda6c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda6c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda6c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bda6c-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bda6c-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bda6c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda6c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bda6c-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bda6c-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bda6c-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bda6c-120">End of client support</span></span><br/>    | <span data-ttu-id="bda6c-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="bda6c-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="bda6c-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bda6c-122">End of server support</span></span><br/>    | <span data-ttu-id="bda6c-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bda6c-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="bda6c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bda6c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda6c-125"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="bda6c-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="bda6c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="bda6c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bda6c-127"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bda6c-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="bda6c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bda6c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bda6c-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda6c-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




