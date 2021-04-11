---
title: Codice di notifica NM_TVSTATEIMAGECHANGING (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero alla finestra padre che l'immagine di stato sta cambiando. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- Controlli di Windows per il codice di notifica NM_TVSTATEIMAGECHANGING
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119450"
---
# <a name="nm_tvstateimagechanging-notification-code"></a><span data-ttu-id="07142-105">\_Codice di notifica TVSTATEIMAGECHANGING Nm</span><span class="sxs-lookup"><span data-stu-id="07142-105">NM\_TVSTATEIMAGECHANGING notification code</span></span>

<span data-ttu-id="07142-106">Inviato da un controllo di visualizzazione albero alla finestra padre che l'immagine di stato sta cambiando.</span><span class="sxs-lookup"><span data-stu-id="07142-106">Sent by a tree-view control to its parent window that the state image is changing.</span></span> <span data-ttu-id="07142-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="07142-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a><span data-ttu-id="07142-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07142-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07142-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07142-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07142-110">Puntatore a una struttura [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="07142-110">A pointer to an [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07142-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07142-111">Return value</span></span>

<span data-ttu-id="07142-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="07142-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="07142-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07142-113">Requirements</span></span>



| <span data-ttu-id="07142-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="07142-114">Requirement</span></span> | <span data-ttu-id="07142-115">Valore</span><span class="sxs-lookup"><span data-stu-id="07142-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07142-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07142-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07142-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07142-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07142-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07142-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07142-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07142-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07142-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07142-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07142-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07142-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





