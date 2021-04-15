---
title: Codice di notifica CBEN_GETDISPINFO (COMmctrl. h)
description: Inviato per recuperare le informazioni di visualizzazione relative a un elemento di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- Controlli di Windows per il codice di notifica CBEN_GETDISPINFO
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517385"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="96a0c-105">\_Codice di notifica GETDISPINFO di CBEN</span><span class="sxs-lookup"><span data-stu-id="96a0c-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="96a0c-106">Inviato per recuperare le informazioni di visualizzazione relative a un elemento di callback.</span><span class="sxs-lookup"><span data-stu-id="96a0c-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="96a0c-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="96a0c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="96a0c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96a0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96a0c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96a0c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96a0c-110">Puntatore a una struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="96a0c-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96a0c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96a0c-111">Return value</span></span>

<span data-ttu-id="96a0c-112">L'elaborazione dell'applicazione del codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="96a0c-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="96a0c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="96a0c-113">Remarks</span></span>

<span data-ttu-id="96a0c-114">La struttura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contiene una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="96a0c-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="96a0c-115">Il membro **mask** specifica le informazioni richieste dal controllo.</span><span class="sxs-lookup"><span data-stu-id="96a0c-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="96a0c-116">Compilare i membri appropriati della struttura per restituire al controllo le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="96a0c-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="96a0c-117">Se il gestore di messaggi imposta il membro **mask** della struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) su CBEIF \_ di un \_ elemento, il controllo archivia le informazioni e non le richiede di nuovo.</span><span class="sxs-lookup"><span data-stu-id="96a0c-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a0c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96a0c-118">Requirements</span></span>



| <span data-ttu-id="96a0c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a0c-119">Requirement</span></span> | <span data-ttu-id="96a0c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="96a0c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96a0c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a0c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96a0c-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96a0c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96a0c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a0c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96a0c-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96a0c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96a0c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96a0c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a0c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a0c-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="96a0c-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="96a0c-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="96a0c-128">**CBEN \_ GETDISPINFOW** (Unicode) e **CBEN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="96a0c-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





