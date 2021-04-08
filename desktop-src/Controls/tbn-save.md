---
title: Codice di notifica TBN_SAVE (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 31622f5e-2e33-4a42-8c49-cc3028a6fa62
keywords:
- Controlli di Windows per il codice di notifica TBN_SAVE
topic_type:
- apiref
api_name:
- TBN_SAVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cd28cb9d5fa1804caa3fe0ca89823305725ddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743802"
---
# <a name="tbn_save-notification-code"></a><span data-ttu-id="8775d-105">TBN \_ salvare il codice di notifica</span><span class="sxs-lookup"><span data-stu-id="8775d-105">TBN\_SAVE notification code</span></span>

<span data-ttu-id="8775d-106">Notifica alla finestra padre di una barra degli strumenti che è in corso il salvataggio di una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="8775d-106">Notifies a toolbar's parent window that a toolbar is in the process of being saved.</span></span> <span data-ttu-id="8775d-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8775d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_SAVE 

    lpnmtb = (LPNMTBSAVE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8775d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8775d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8775d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8775d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8775d-110">Puntatore a una struttura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) .</span><span class="sxs-lookup"><span data-stu-id="8775d-110">Pointer to an [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8775d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8775d-111">Return value</span></span>

<span data-ttu-id="8775d-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8775d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8775d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8775d-113">Remarks</span></span>

<span data-ttu-id="8775d-114">L'applicazione riceverà il codice di notifica una volta all'inizio del processo di salvataggio e una volta per ogni pulsante.</span><span class="sxs-lookup"><span data-stu-id="8775d-114">The application will receive this notification code once at the start of the save process and once for each button.</span></span> <span data-ttu-id="8775d-115">Questo codice di notifica consente di aggiungere le proprie informazioni a salvate dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="8775d-115">This notification code gives you an opportunity to add your own information to that saved by the Shell.</span></span> <span data-ttu-id="8775d-116">Se non si desidera aggiungere informazioni, ignorare il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="8775d-116">If you do not wish to add information, ignore the notification code.</span></span> <span data-ttu-id="8775d-117">Per una descrizione più dettagliata di come gestire TBN Salva, vedere [personalizzazione della barra degli strumenti](toolbar-controls-overview.md) \_ .</span><span class="sxs-lookup"><span data-stu-id="8775d-117">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle TBN\_SAVE.</span></span>

## <a name="requirements"></a><span data-ttu-id="8775d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8775d-118">Requirements</span></span>



| <span data-ttu-id="8775d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8775d-119">Requirement</span></span> | <span data-ttu-id="8775d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8775d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8775d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8775d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8775d-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8775d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8775d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8775d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8775d-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8775d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8775d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8775d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8775d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8775d-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8775d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8775d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8775d-128">\_ripristino TBN</span><span class="sxs-lookup"><span data-stu-id="8775d-128">TBN\_RESTORE</span></span>](tbn-restore.md)
</dt> </dl>

 

 





