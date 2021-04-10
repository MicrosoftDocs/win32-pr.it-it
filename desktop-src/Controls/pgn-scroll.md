---
title: Codice di notifica PGN_SCROLL (COMmctrl. h)
description: Notifica alla finestra padre di un controllo pager che sta per essere eseguito lo scorrimento della finestra contenuta. Questa notifica viene inviata sotto forma di \_ messaggio di notifica WM.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- Controlli di Windows per il codice di notifica PGN_SCROLL
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119578"
---
# <a name="pgn_scroll-notification-code"></a><span data-ttu-id="3a448-105">\_Codice di notifica di scorrimento PGN</span><span class="sxs-lookup"><span data-stu-id="3a448-105">PGN\_SCROLL notification code</span></span>

<span data-ttu-id="3a448-106">Notifica alla finestra padre di un controllo pager che sta per essere eseguito lo scorrimento della finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="3a448-106">Notifies a pager control's parent window that the contained window is about to be scrolled.</span></span> <span data-ttu-id="3a448-107">Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3a448-107">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3a448-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a448-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a448-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a448-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a448-110">Puntatore a una struttura [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) che contiene e riceve informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a448-110">Pointer to an [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="3a448-111">Il membro **Idir** della struttura indica la direzione dello scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3a448-111">The **iDir** member of this structure indicates the direction of the scroll.</span></span> <span data-ttu-id="3a448-112">I membri **iXpos** e **iYpos** contengono la posizione orizzontale e verticale della finestra contenuta prima dello scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3a448-112">The **iXpos** and **iYpos** members contain the horizontal and vertical position of the contained window prior to the scroll.</span></span> <span data-ttu-id="3a448-113">Il membro **iScroll** contiene l'importo Delta di scorrimento predefinito.</span><span class="sxs-lookup"><span data-stu-id="3a448-113">The **iScroll** member contains the default scroll delta amount.</span></span> <span data-ttu-id="3a448-114">Se lo si desidera, è possibile modificare questo membro in un altro valore di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3a448-114">You can modify this member to a different scroll amount if desired.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a448-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a448-115">Return value</span></span>

<span data-ttu-id="3a448-116">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a448-116">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a448-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a448-117">Requirements</span></span>



| <span data-ttu-id="3a448-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a448-118">Requirement</span></span> | <span data-ttu-id="3a448-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3a448-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a448-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a448-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a448-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a448-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a448-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a448-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a448-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a448-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a448-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a448-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a448-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a448-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





