---
title: Codice di notifica TBN_ENDDRAG (COMmctrl. h)
description: Notifica alla finestra padre della barra degli strumenti che l'utente ha interrotto il trascinamento di un pulsante in una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- Controlli di Windows per il codice di notifica TBN_ENDDRAG
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120671"
---
# <a name="tbn_enddrag-notification-code"></a><span data-ttu-id="be007-105">\_Codice di notifica ENDDRAG di TBN</span><span class="sxs-lookup"><span data-stu-id="be007-105">TBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="be007-106">Notifica alla finestra padre della barra degli strumenti che l'utente ha interrotto il trascinamento di un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="be007-106">Notifies the toolbar's parent window that the user has stopped dragging a button in a toolbar.</span></span> <span data-ttu-id="be007-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="be007-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="be007-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be007-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be007-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be007-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be007-110">Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="be007-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="be007-111">Il membro **iItem** contiene l'identificatore di comando del pulsante trascinato.</span><span class="sxs-lookup"><span data-stu-id="be007-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be007-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be007-112">Return value</span></span>

<span data-ttu-id="be007-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="be007-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be007-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be007-114">Requirements</span></span>



| <span data-ttu-id="be007-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="be007-115">Requirement</span></span> | <span data-ttu-id="be007-116">Valore</span><span class="sxs-lookup"><span data-stu-id="be007-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be007-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be007-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be007-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be007-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be007-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be007-119">Minimum supported server</span></span><br/> | <span data-ttu-id="be007-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be007-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be007-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be007-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="be007-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be007-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





