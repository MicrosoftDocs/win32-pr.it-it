---
title: Messaggio HDN_ITEMSTATEICONCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto clic sull'icona di stato di un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- Controlli di Windows Message HDN_ITEMSTATEICONCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479162"
---
# <a name="hdn_itemstateiconclick-message"></a><span data-ttu-id="f6653-105">\_Messaggio HDN ITEMSTATEICONCLICK</span><span class="sxs-lookup"><span data-stu-id="f6653-105">HDN\_ITEMSTATEICONCLICK message</span></span>

<span data-ttu-id="f6653-106">Notifica alla finestra padre di un controllo di intestazione che l'utente ha fatto clic sull'icona di stato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="f6653-106">Notifies a header control's parent window that the user clicked an item's state icon.</span></span> <span data-ttu-id="f6653-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f6653-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f6653-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6653-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6653-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6653-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6653-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) che contiene informazioni aggiuntive sull'icona di stato su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="f6653-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the state icon that was clicked on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6653-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6653-111">Return value</span></span>

<span data-ttu-id="f6653-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f6653-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6653-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6653-113">Requirements</span></span>



| <span data-ttu-id="f6653-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6653-114">Requirement</span></span> | <span data-ttu-id="f6653-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f6653-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6653-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6653-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6653-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6653-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6653-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6653-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6653-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6653-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6653-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6653-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6653-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6653-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





