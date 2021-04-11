---
description: Il metodo MCSVC chiama il metodo OnStatus per notificare al monitoraggio che si è verificata l'esistenza di un evento di stato NPP. Questo metodo deve essere implementato dal monitoraggio.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Metodo IMonitor:: onStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130262"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="09513-104">Metodo IMonitor:: OnStatus</span><span class="sxs-lookup"><span data-stu-id="09513-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="09513-105">Il metodo MCSVC chiama il metodo **OnStatus** per notificare al monitoraggio che si è verificata l'esistenza di un evento di stato NPP.</span><span class="sxs-lookup"><span data-stu-id="09513-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="09513-106">Questo metodo deve essere implementato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="09513-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="09513-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09513-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="09513-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09513-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09513-109">*Evento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09513-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09513-110">Struttura [di \_ eventi di aggiornamento](update-event.md) .</span><span class="sxs-lookup"><span data-stu-id="09513-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09513-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09513-111">Return value</span></span>

<span data-ttu-id="09513-112">Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR) e MCSVC passa il valore restituito all'oggetto NPP per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="09513-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="09513-113">Se il metodo ha esito negativo, restituire un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="09513-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="09513-114">In errore, MCSVC passa il valore restituito all'oggetto NPP per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="09513-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="09513-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09513-115">Requirements</span></span>



| <span data-ttu-id="09513-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09513-116">Requirement</span></span> | <span data-ttu-id="09513-117">Valore</span><span class="sxs-lookup"><span data-stu-id="09513-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09513-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09513-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09513-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09513-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09513-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09513-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09513-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09513-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09513-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09513-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09513-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="09513-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




