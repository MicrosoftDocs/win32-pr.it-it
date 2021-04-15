---
title: Codice di notifica RBN_SPLITTERDRAG (COMmctrl. h)
description: Inviato da un controllo Rebar quando l'utente trascina una barra di divisione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- Controlli di Windows per il codice di notifica RBN_SPLITTERDRAG
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518268"
---
# <a name="rbn_splitterdrag-notification-code"></a><span data-ttu-id="7a188-105">\_Codice di notifica SPLITTERDRAG di RBN</span><span class="sxs-lookup"><span data-stu-id="7a188-105">RBN\_SPLITTERDRAG notification code</span></span>

<span data-ttu-id="7a188-106">Inviato da un controllo Rebar quando l'utente trascina una barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="7a188-106">Sent by a rebar control when the user drags a splitter.</span></span> <span data-ttu-id="7a188-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7a188-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7a188-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a188-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a188-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a188-110">Puntatore a una struttura [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="7a188-110">Pointer to an [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a188-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a188-111">Return value</span></span>

<span data-ttu-id="7a188-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7a188-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a188-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a188-113">Requirements</span></span>



| <span data-ttu-id="7a188-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a188-114">Requirement</span></span> | <span data-ttu-id="7a188-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7a188-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a188-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a188-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7a188-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a188-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a188-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a188-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7a188-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a188-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a188-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a188-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a188-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a188-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





