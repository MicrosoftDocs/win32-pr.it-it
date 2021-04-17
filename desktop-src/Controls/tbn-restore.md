---
title: Codice di notifica TBN_RESTORE (COMmctrl. h)
description: Notifica alla finestra padre di una barra degli strumenti che è in corso il ripristino di una barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- Controlli di Windows per il codice di notifica TBN_RESTORE
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478083"
---
# <a name="tbn_restore-notification-code"></a><span data-ttu-id="763a7-105">\_Codice di notifica del ripristino TBN</span><span class="sxs-lookup"><span data-stu-id="763a7-105">TBN\_RESTORE notification code</span></span>

<span data-ttu-id="763a7-106">Notifica alla finestra padre di una barra degli strumenti che è in corso il ripristino di una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="763a7-106">Notifies a toolbar's parent window that a toolbar is in the process of being restored.</span></span> <span data-ttu-id="763a7-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="763a7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="763a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="763a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763a7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="763a7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="763a7-110">Puntatore a una struttura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .</span><span class="sxs-lookup"><span data-stu-id="763a7-110">Pointer to an [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="763a7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="763a7-111">Return value</span></span>

<span data-ttu-id="763a7-112">L'applicazione deve restituire zero in risposta al primo codice di notifica del **\_ ripristino di TBN** ricevuto all'inizio del processo di ripristino per continuare a ripristinare le informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="763a7-112">The application should return zero in response to the first **TBN\_RESTORE** notification code received at the start of the restore process to continue restoring the button information.</span></span> <span data-ttu-id="763a7-113">Se l'applicazione restituisce un valore diverso da zero, il processo di ripristino viene annullato.</span><span class="sxs-lookup"><span data-stu-id="763a7-113">If the application returns a nonzero value, the restore process is canceled.</span></span>

## <a name="remarks"></a><span data-ttu-id="763a7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="763a7-114">Remarks</span></span>

<span data-ttu-id="763a7-115">L'applicazione riceverà il codice di notifica una volta all'inizio del processo di ripristino e una volta per ogni pulsante.</span><span class="sxs-lookup"><span data-stu-id="763a7-115">The application will receive this notification code once at the start of the restore process and once for each button.</span></span> <span data-ttu-id="763a7-116">Questo codice di notifica consente di estrarre le informazioni dal flusso di dati salvato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="763a7-116">This notification code gives you an opportunity to extract the information from the data stream that you saved previously.</span></span> <span data-ttu-id="763a7-117">Se non sono state salvate informazioni, ignorare il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="763a7-117">If you haven't saved any information, ignore the notification code.</span></span> <span data-ttu-id="763a7-118">Per una descrizione più dettagliata di come gestire il **\_ ripristino di TBN**, vedere [personalizzazione della barra degli strumenti](toolbar-controls-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="763a7-118">See [Toolbar Customization](toolbar-controls-overview.md) for a more detailed discussion of how to handle **TBN\_RESTORE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="763a7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="763a7-119">Requirements</span></span>



| <span data-ttu-id="763a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="763a7-120">Requirement</span></span> | <span data-ttu-id="763a7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="763a7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="763a7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="763a7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="763a7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="763a7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="763a7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="763a7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="763a7-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="763a7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="763a7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="763a7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="763a7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="763a7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





