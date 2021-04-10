---
description: L' \_ evento DBT USERDEFINED Device identifica un evento definito dall'utente.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Evento DBT_USERDEFINED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049187"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="a871c-103">\_Evento USERDEFINED DBT</span><span class="sxs-lookup"><span data-stu-id="a871c-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="a871c-104">L' \_ evento DBT USERDEFINED Device identifica un evento definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a871c-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="a871c-105">Per trasmettere questo evento del dispositivo, chiamare la funzione [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) con il messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="a871c-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="a871c-106">Impostare *wParam* su DBT \_ USERDEFINED e impostare *lParam* come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="a871c-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="a871c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a871c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a871c-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a871c-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a871c-109">Handle di una finestra.</span><span class="sxs-lookup"><span data-stu-id="a871c-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="a871c-110">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="a871c-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="a871c-111">Identificatore del messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="a871c-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a871c-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a871c-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a871c-113">Impostare su DBT \_ USERDEFINED.</span><span class="sxs-lookup"><span data-stu-id="a871c-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="a871c-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a871c-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a871c-115">Puntatore a una struttura [**\_ \_ \_ USERDEFINED di sviluppo broadcast**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) che descrive la trasmissione definita dall'utente in corso.</span><span class="sxs-lookup"><span data-stu-id="a871c-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="a871c-116">Il membro **dbud \_ szName** contiene il nome del messaggio definito dall'utente, seguito da tutti i dati definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a871c-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a871c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a871c-117">Return value</span></span>

<span data-ttu-id="a871c-118">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="a871c-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a871c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a871c-119">Requirements</span></span>



| <span data-ttu-id="a871c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a871c-120">Requirement</span></span> | <span data-ttu-id="a871c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a871c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a871c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a871c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a871c-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a871c-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="a871c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a871c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a871c-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a871c-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="a871c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a871c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a871c-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a871c-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a871c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a871c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a871c-129">Eventi dispositivo</span><span class="sxs-lookup"><span data-stu-id="a871c-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="a871c-130">Eventi di gestione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="a871c-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="a871c-131">**\_\_USERDEFINED broadcast \_ dev**</span><span class="sxs-lookup"><span data-stu-id="a871c-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="a871c-132">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="a871c-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="a871c-133">**BroadcastSystemMessage**</span><span class="sxs-lookup"><span data-stu-id="a871c-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

