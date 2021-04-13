---
title: Funzione WsSetAutoFail (WebServicesDebug. h)
description: Imposta il punto successivo in cui inserire un errore. Si tratta di una funzione di solo DEBUG.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Servizi Web per la funzione WsSetAutoFail per Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518538"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="371bd-105">WsSetAutoFail (funzione)</span><span class="sxs-lookup"><span data-stu-id="371bd-105">WsSetAutoFail function</span></span>

<span data-ttu-id="371bd-106">Imposta il punto successivo in cui inserire un errore.</span><span class="sxs-lookup"><span data-stu-id="371bd-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="371bd-107">Si tratta di una funzione di solo DEBUG.</span><span class="sxs-lookup"><span data-stu-id="371bd-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="371bd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="371bd-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="371bd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="371bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="371bd-110">*numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="371bd-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="371bd-111">Specifica il numero di operazioni prima che inizino a verificarsi degli errori.</span><span class="sxs-lookup"><span data-stu-id="371bd-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="371bd-112">*errore* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="371bd-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="371bd-113">Puntatore a un oggetto [WS \_ Error](ws-error.md) in cui è necessario archiviare informazioni aggiuntive sull'errore se la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="371bd-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="371bd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="371bd-114">Return value</span></span>

<span data-ttu-id="371bd-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="371bd-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="371bd-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="371bd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="371bd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="371bd-117">Requirements</span></span>



| <span data-ttu-id="371bd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="371bd-118">Requirement</span></span> | <span data-ttu-id="371bd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="371bd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="371bd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="371bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="371bd-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="371bd-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="371bd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="371bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="371bd-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="371bd-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="371bd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="371bd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="371bd-125"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="371bd-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





