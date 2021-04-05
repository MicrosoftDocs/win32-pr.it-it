---
description: Il metodo onframes deve essere implementato dal monitoraggio. MCSVC chiama questo metodo quando il buffer di acquisizione è pieno o il tempo di aggiornamento è scaduto.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Metodo IMonitor:: onframes (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751087"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="f3b0f-104">Metodo IMonitor:: onframes</span><span class="sxs-lookup"><span data-stu-id="f3b0f-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="f3b0f-105">Il metodo **Onframes** deve essere implementato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="f3b0f-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="f3b0f-106">MCSVC chiama questo metodo quando il buffer di acquisizione è pieno o il tempo di aggiornamento è scaduto.</span><span class="sxs-lookup"><span data-stu-id="f3b0f-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b0f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3b0f-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="f3b0f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3b0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b0f-109">*Evento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3b0f-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3b0f-110">[Aggiornamento \_ di ](update-event.md) Struttura dell'evento che include le informazioni sul frame utilizzate per aggiornare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="f3b0f-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b0f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3b0f-111">Return value</span></span>

<span data-ttu-id="f3b0f-112">Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).</span><span class="sxs-lookup"><span data-stu-id="f3b0f-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="f3b0f-113">MCSVC passa di nuovo il valore restituito all'oggetto NPP per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f3b0f-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="f3b0f-114">Se il metodo ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f3b0f-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="f3b0f-115">MCSVC passa di nuovo il valore restituito all'oggetto NPP per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f3b0f-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b0f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3b0f-116">Requirements</span></span>



| <span data-ttu-id="f3b0f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b0f-117">Requirement</span></span> | <span data-ttu-id="f3b0f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f3b0f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b0f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3b0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b0f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3b0f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f3b0f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3b0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b0f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f3b0f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f3b0f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3b0f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b0f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b0f-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




