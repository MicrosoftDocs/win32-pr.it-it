---
description: Il \_ messaggio di eliminazione del Tablet WM \_ viene pubblicato quando un dispositivo tablet viene rimosso da Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Messaggio WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306700"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="085c0-103">Messaggio di eliminazione del \_ Tablet WM \_</span><span class="sxs-lookup"><span data-stu-id="085c0-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="085c0-104">Il messaggio di **\_ \_ eliminazione del Tablet WM** viene pubblicato quando un dispositivo tablet viene rimosso da Windows.</span><span class="sxs-lookup"><span data-stu-id="085c0-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="085c0-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="085c0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085c0-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="085c0-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="085c0-107">Indice del dispositivo tablet da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="085c0-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="085c0-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="085c0-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="085c0-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="085c0-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="085c0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="085c0-110">Remarks</span></span>

<span data-ttu-id="085c0-111">Questo messaggio viene inviato a tutte le finestre di primo livello del sistema, incluse le finestre senza proprietà disabilitate o invisibili, le finestre sovrapposte e le finestre popup; ma il messaggio non viene inviato alle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="085c0-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="085c0-112">Gli indici passati in *wParam* sono correlati all'indice usato dal metodo [**ITabletManager:: gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="085c0-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="085c0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="085c0-113">Requirements</span></span>



| <span data-ttu-id="085c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="085c0-114">Requirement</span></span> | <span data-ttu-id="085c0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="085c0-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="085c0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="085c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="085c0-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="085c0-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="085c0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="085c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="085c0-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="085c0-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="085c0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="085c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="085c0-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="085c0-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
