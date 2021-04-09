---
title: Codice di notifica di NM_RDBLCLK (visualizzazione albero) (COMmctrl. h)
description: Notifica all'elemento padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo. Questa notifica viene inviata sotto forma di \_ messaggio di notifica WM.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK (visualizzazione albero) controlli di Windows per il codice di notifica
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120839"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a><span data-ttu-id="4379d-105">\_Codice di notifica di RDBLCLK Nm (visualizzazione albero)</span><span class="sxs-lookup"><span data-stu-id="4379d-105">NM\_RDBLCLK (tree view) notification code</span></span>

<span data-ttu-id="4379d-106">Notifica all'elemento padre di un controllo di visualizzazione albero che l'utente ha fatto doppio clic con il pulsante destro del mouse all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="4379d-106">Notifies the parent of a tree-view control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="4379d-107">Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4379d-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4379d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4379d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4379d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4379d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4379d-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="4379d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4379d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4379d-111">Return value</span></span>

<span data-ttu-id="4379d-112">Restituisce un valore diverso da zero per impedire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4379d-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="4379d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4379d-113">Requirements</span></span>



| <span data-ttu-id="4379d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4379d-114">Requirement</span></span> | <span data-ttu-id="4379d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4379d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4379d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4379d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4379d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4379d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4379d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4379d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4379d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4379d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4379d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4379d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4379d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4379d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





