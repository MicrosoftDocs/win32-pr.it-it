---
title: Codice di notifica TBN_QUERYINSERT (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti se un pulsante può essere inserito a sinistra del pulsante specificato mentre l'utente sta personalizzando una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- Controlli di Windows per il codice di notifica TBN_QUERYINSERT
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964853"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="4650f-105">\_Codice di notifica QUERYINSERT di TBN</span><span class="sxs-lookup"><span data-stu-id="4650f-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="4650f-106">Notifica alla finestra padre della barra degli strumenti se un pulsante può essere inserito a sinistra del pulsante specificato mentre l'utente sta personalizzando una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="4650f-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="4650f-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4650f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4650f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4650f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4650f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4650f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4650f-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="4650f-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="4650f-111">Il membro **iItem** contiene l'indice in base zero del pulsante da inserire.</span><span class="sxs-lookup"><span data-stu-id="4650f-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4650f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4650f-112">Return value</span></span>

<span data-ttu-id="4650f-113">Restituisce **true** per consentire l'inserimento di un pulsante davanti al pulsante specificato o **false** per impedire l'inserimento del pulsante.</span><span class="sxs-lookup"><span data-stu-id="4650f-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="4650f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4650f-114">Requirements</span></span>



| <span data-ttu-id="4650f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4650f-115">Requirement</span></span> | <span data-ttu-id="4650f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4650f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4650f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4650f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4650f-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4650f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4650f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4650f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4650f-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4650f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4650f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4650f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4650f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4650f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





