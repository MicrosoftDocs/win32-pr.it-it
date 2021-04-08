---
title: Codice di notifica PGN_CALCSIZE (COMmctrl. h)
description: Inviato da un controllo cercapersone per ottenere le dimensioni di scorrimento della finestra contenuta.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- Controlli di Windows per il codice di notifica PGN_CALCSIZE
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741218"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="0fd85-104">\_Codice di notifica CALCSIZE di PGN</span><span class="sxs-lookup"><span data-stu-id="0fd85-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="0fd85-105">Inviato da un controllo cercapersone per ottenere le dimensioni di scorrimento della finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="0fd85-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="0fd85-106">Queste dimensioni vengono utilizzate dal controllo pager per determinare la dimensione scorrevole della finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="0fd85-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="0fd85-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd85-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0fd85-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fd85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fd85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fd85-110">Puntatore a una struttura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) che contiene e riceve informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="0fd85-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="0fd85-111">Il membro **dwFlag** della struttura indica la dimensione da calcolare.</span><span class="sxs-lookup"><span data-stu-id="0fd85-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="0fd85-112">A seconda del valore di **dwFlag**, è necessario inserire la dimensione desiderata nel membro **larghezza** o **altezza** della struttura.</span><span class="sxs-lookup"><span data-stu-id="0fd85-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd85-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fd85-113">Return value</span></span>

<span data-ttu-id="0fd85-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0fd85-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd85-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fd85-115">Requirements</span></span>



| <span data-ttu-id="0fd85-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd85-116">Requirement</span></span> | <span data-ttu-id="0fd85-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0fd85-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd85-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fd85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd85-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fd85-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fd85-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fd85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd85-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0fd85-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fd85-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fd85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd85-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd85-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





