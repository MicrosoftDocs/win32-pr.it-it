---
title: Messaggio di WM_RASDIALEVENT (RAS. h)
description: Il sistema operativo invia un \_ messaggio WM RASDIALEVENT a una routine della finestra quando si verifica una modifica dell'evento di stato durante un processo di connessione RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- RAS del messaggio WM_RASDIALEVENT
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301002"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="b341d-104">\_Messaggio RASDIALEVENT WM</span><span class="sxs-lookup"><span data-stu-id="b341d-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="b341d-105">Il sistema operativo invia un messaggio **WM \_ RASDIALEVENT** a una routine della finestra quando si verifica una modifica dell'evento di stato durante un processo di connessione RAS.</span><span class="sxs-lookup"><span data-stu-id="b341d-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="b341d-106">Questo errore si verifica quando viene specificata una finestra per gestire le notifiche di tali eventi utilizzando il parametro *Notifier* di [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span><span class="sxs-lookup"><span data-stu-id="b341d-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="b341d-107">I due parametri del messaggio sono equivalenti ai parametri degli stessi nomi utilizzati con le funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="b341d-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="b341d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b341d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b341d-109">*rasconnstate*</span><span class="sxs-lookup"><span data-stu-id="b341d-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="b341d-110">Valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="b341d-110">Value of *wParam*.</span></span> <span data-ttu-id="b341d-111">Equivale al parametro *rasconnstate* delle funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="b341d-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="b341d-112">Specifica un valore di enumeratore [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) che indica lo stato in cui il processo di connessione di accesso remoto RasDial sta per essere inserito.</span><span class="sxs-lookup"><span data-stu-id="b341d-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="b341d-113">*dwError*</span><span class="sxs-lookup"><span data-stu-id="b341d-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="b341d-114">Valore di *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b341d-114">Value of *lParam*.</span></span> <span data-ttu-id="b341d-115">Equivale al parametro *dwError* delle funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="b341d-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="b341d-116">Un valore diverso da zero indica l'errore che si è verificato o zero se non si è verificato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="b341d-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="b341d-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) Invia questo messaggio con *dwError* impostato su zero alla voce per ogni stato della connessione.</span><span class="sxs-lookup"><span data-stu-id="b341d-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="b341d-118">Se si verifica un errore all'interno di uno stato, il messaggio viene inviato di nuovo per lo stato, questa volta con un valore *dwError* diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b341d-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b341d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b341d-119">Return value</span></span>

<span data-ttu-id="b341d-120">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="b341d-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b341d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b341d-121">Requirements</span></span>



| <span data-ttu-id="b341d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b341d-122">Requirement</span></span> | <span data-ttu-id="b341d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b341d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b341d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b341d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b341d-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b341d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b341d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b341d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b341d-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b341d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b341d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b341d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b341d-129"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="b341d-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b341d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b341d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b341d-131">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="b341d-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b341d-132">Messaggi del servizio di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="b341d-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="b341d-133">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="b341d-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="b341d-134">**RasDialFunc**</span><span class="sxs-lookup"><span data-stu-id="b341d-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="b341d-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="b341d-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="b341d-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b341d-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 

