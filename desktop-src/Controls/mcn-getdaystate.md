---
title: Codice di notifica MCN_GETDAYSTATE (COMmctrl. h)
description: Inviato da un controllo di calendario mensile per richiedere informazioni sulla modalità di visualizzazione dei singoli giorni. Questo codice di notifica viene inviato solo da controlli calendario mensile che usano lo \_ stile DAYSTATE MCS e viene inviato sotto forma di messaggio di notifica WM \_ .
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- Controlli di Windows per il codice di notifica MCN_GETDAYSTATE
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741690"
---
# <a name="mcn_getdaystate-notification-code"></a><span data-ttu-id="c1d41-105">\_Codice di notifica GETDAYSTATE di MCN</span><span class="sxs-lookup"><span data-stu-id="c1d41-105">MCN\_GETDAYSTATE notification code</span></span>

<span data-ttu-id="c1d41-106">Inviato da un controllo di calendario mensile per richiedere informazioni sulla modalità di visualizzazione dei singoli giorni.</span><span class="sxs-lookup"><span data-stu-id="c1d41-106">Sent by a month calendar control to request information about how individual days should be displayed.</span></span> <span data-ttu-id="c1d41-107">Questo codice di notifica viene inviato solo da controlli calendario mensile che usano lo stile [**\_ DAYSTATE MCS**](month-calendar-control-styles.md) e viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d41-107">This notification code is sent only by month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style, and it is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c1d41-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1d41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1d41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d41-110">Puntatore a una struttura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) .</span><span class="sxs-lookup"><span data-stu-id="c1d41-110">Pointer to an [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure.</span></span> <span data-ttu-id="c1d41-111">La struttura contiene informazioni sull'intervallo di tempo per il quale il controllo necessita di informazioni e riceve l'indirizzo di una matrice che fornisce questi dati.</span><span class="sxs-lookup"><span data-stu-id="c1d41-111">The structure contains information about the time frame for which the control needs information, and it receives the address of an array that provides this data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d41-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1d41-112">Return value</span></span>

<span data-ttu-id="c1d41-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c1d41-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1d41-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1d41-114">Remarks</span></span>

<span data-ttu-id="c1d41-115">La gestione di questo codice di notifica consente all'applicazione di personalizzare la visualizzazione specificando che determinati giorni devono essere visualizzati in grassetto.</span><span class="sxs-lookup"><span data-stu-id="c1d41-115">Handling this notification code allows your application to customize its display by specifying that certain days be displayed in bold.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d41-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1d41-116">Requirements</span></span>



| <span data-ttu-id="c1d41-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d41-117">Requirement</span></span> | <span data-ttu-id="c1d41-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c1d41-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d41-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d41-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1d41-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1d41-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1d41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d41-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1d41-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1d41-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1d41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d41-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d41-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





