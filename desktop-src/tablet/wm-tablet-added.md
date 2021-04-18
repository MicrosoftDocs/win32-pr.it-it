---
description: Il \_ \_ messaggio di aggiunta del Tablet WM viene pubblicato quando un dispositivo tablet viene aggiunto a Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Messaggio WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306701"
---
# <a name="wm_tablet_added-message"></a><span data-ttu-id="8d14d-103">\_Messaggio di \_ aggiunta Tablet WM</span><span class="sxs-lookup"><span data-stu-id="8d14d-103">WM\_TABLET\_ADDED message</span></span>

<span data-ttu-id="8d14d-104">Il messaggio di **\_ \_ aggiunta del Tablet WM** viene pubblicato quando un dispositivo tablet viene aggiunto a Windows.</span><span class="sxs-lookup"><span data-stu-id="8d14d-104">The **WM\_TABLET\_ADDED** message is posted when a tablet device is added to Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a><span data-ttu-id="8d14d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d14d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d14d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d14d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d14d-107">Indice di un dispositivo Tablet aggiunto</span><span class="sxs-lookup"><span data-stu-id="8d14d-107">Index of tablet device being added</span></span>

</dd> <dt>

<span data-ttu-id="8d14d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d14d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d14d-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8d14d-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d14d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d14d-110">Remarks</span></span>

<span data-ttu-id="8d14d-111">Questo messaggio viene inviato a tutte le finestre di primo livello del sistema, incluse le finestre senza proprietà disabilitate o invisibili, le finestre sovrapposte e le finestre popup; ma il messaggio non viene inviato alle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="8d14d-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="8d14d-112">Gli indici passati in *wParam* sono correlati all'indice usato dal metodo [**ITabletManager:: gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d14d-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d14d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d14d-113">Requirements</span></span>



| <span data-ttu-id="8d14d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d14d-114">Requirement</span></span> | <span data-ttu-id="8d14d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8d14d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d14d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d14d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8d14d-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d14d-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8d14d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d14d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8d14d-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8d14d-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="8d14d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d14d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d14d-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d14d-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
