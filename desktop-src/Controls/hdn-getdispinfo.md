---
title: Codice di notifica HDN_GETDISPINFO (COMmctrl. h)
description: Inviato al proprietario di un controllo intestazione quando il controllo necessita di informazioni su un elemento dell'intestazione di callback. Questo codice di notifica viene inviato come un \_ messaggio di notifica WM.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- Controlli di Windows per il codice di notifica HDN_GETDISPINFO
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047937"
---
# <a name="hdn_getdispinfo-notification-code"></a><span data-ttu-id="6a9ed-105">\_Codice di notifica GETDISPINFO di HDN</span><span class="sxs-lookup"><span data-stu-id="6a9ed-105">HDN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="6a9ed-106">Inviato al proprietario di un controllo intestazione quando il controllo necessita di informazioni su un elemento dell'intestazione di callback.</span><span class="sxs-lookup"><span data-stu-id="6a9ed-106">Sent to the owner of a header control when the control needs information about a callback header item.</span></span> <span data-ttu-id="6a9ed-107">Questo codice di notifica viene inviato come un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6a9ed-107">This notification code is sent as a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6a9ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a9ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a9ed-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a9ed-110">Puntatore a una struttura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="6a9ed-110">A pointer to an [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure.</span></span> <span data-ttu-id="6a9ed-111">In input i campi della struttura specificano le informazioni necessarie e l'elemento di interesse.</span><span class="sxs-lookup"><span data-stu-id="6a9ed-111">On input, the fields of the structure specify what information is required and the item of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a9ed-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a9ed-112">Return value</span></span>

<span data-ttu-id="6a9ed-113">Restituisce un LRESULT.</span><span class="sxs-lookup"><span data-stu-id="6a9ed-113">Returns an LRESULT.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a9ed-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a9ed-114">Remarks</span></span>

<span data-ttu-id="6a9ed-115">Compilare i membri appropriati della struttura per restituire le informazioni richieste al controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="6a9ed-115">Fill the appropriate members of the structure to return the requested information to the header control.</span></span> <span data-ttu-id="6a9ed-116">Se il gestore di messaggi imposta il membro **mask** della struttura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) su HDI \_ di \_ SetItem, il controllo intestazione archivia le informazioni e non le richiede di nuovo.</span><span class="sxs-lookup"><span data-stu-id="6a9ed-116">If your message handler sets the **mask** member of the [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) structure to HDI\_DI\_SETITEM, the header control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9ed-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a9ed-117">Requirements</span></span>



| <span data-ttu-id="6a9ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a9ed-118">Requirement</span></span> | <span data-ttu-id="6a9ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6a9ed-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9ed-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a9ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9ed-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a9ed-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a9ed-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a9ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9ed-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a9ed-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a9ed-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a9ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a9ed-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a9ed-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6a9ed-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6a9ed-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6a9ed-127">**HDN \_ GETDISPINFOW** (Unicode) e **HDN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6a9ed-127">**HDN\_GETDISPINFOW** (Unicode) and **HDN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



 

 





