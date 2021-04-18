---
title: Codice di notifica PSN_HELP (Prsht. h)
description: Notifica a una pagina che l'utente ha fatto clic sul pulsante della guida. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- Controlli di Windows per il codice di notifica PSN_HELP
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301936"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="95c99-105">Codice di notifica della Guida di PSN \_</span><span class="sxs-lookup"><span data-stu-id="95c99-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="95c99-106">Notifica a una pagina che l'utente ha fatto clic sul pulsante della guida.</span><span class="sxs-lookup"><span data-stu-id="95c99-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="95c99-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="95c99-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="95c99-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="95c99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c99-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95c99-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95c99-110">Puntatore a una struttura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="95c99-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="95c99-111">Questa struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) come primo membro, **HDR**. Il membro **hwndFrom** della struttura **NMHDR** contiene l'handle per la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="95c99-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="95c99-112">Il membro **lParam** della struttura **PSHNOTIFY** non contiene informazioni.</span><span class="sxs-lookup"><span data-stu-id="95c99-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c99-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95c99-113">Return value</span></span>

<span data-ttu-id="95c99-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="95c99-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95c99-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="95c99-115">Remarks</span></span>

<span data-ttu-id="95c99-116">Un'applicazione deve visualizzare le informazioni della Guida per la pagina.</span><span class="sxs-lookup"><span data-stu-id="95c99-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="95c99-117">Questo codice di notifica non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="95c99-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95c99-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95c99-118">Requirements</span></span>



| <span data-ttu-id="95c99-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c99-119">Requirement</span></span> | <span data-ttu-id="95c99-120">Valore</span><span class="sxs-lookup"><span data-stu-id="95c99-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95c99-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95c99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95c99-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95c99-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95c99-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95c99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95c99-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95c99-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95c99-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95c99-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c99-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c99-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





