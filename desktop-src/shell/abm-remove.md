---
description: Annulla la registrazione di un AppBar rimuovendo l'oggetto dall'elenco interno del sistema. Il sistema non invia più messaggi di notifica a AppBar o impedisce ad altre applicazioni di utilizzare l'area dello schermo utilizzata dal AppBar.
title: Messaggio ABM_REMOVE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878782"
---
# <a name="abm_remove-message"></a><span data-ttu-id="e5fd7-104">\_Rimuovi messaggio da ABM</span><span class="sxs-lookup"><span data-stu-id="e5fd7-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="e5fd7-105">Annulla la registrazione di un AppBar rimuovendo l'oggetto dall'elenco interno del sistema.</span><span class="sxs-lookup"><span data-stu-id="e5fd7-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="e5fd7-106">Il sistema non invia più messaggi di notifica a AppBar o impedisce ad altre applicazioni di utilizzare l'area dello schermo utilizzata dal AppBar.</span><span class="sxs-lookup"><span data-stu-id="e5fd7-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="e5fd7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5fd7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5fd7-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="e5fd7-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="e5fd7-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) contenente l'handle per il AppBar di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="e5fd7-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="e5fd7-110">Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **HWND** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="e5fd7-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5fd7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5fd7-111">Return value</span></span>

<span data-ttu-id="e5fd7-112">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="e5fd7-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5fd7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5fd7-113">Remarks</span></span>

<span data-ttu-id="e5fd7-114">Questo messaggio consente al sistema di inviare il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) a tutti i AppBar.</span><span class="sxs-lookup"><span data-stu-id="e5fd7-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5fd7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5fd7-115">Requirements</span></span>



| <span data-ttu-id="e5fd7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5fd7-116">Requirement</span></span> | <span data-ttu-id="e5fd7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e5fd7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5fd7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5fd7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5fd7-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e5fd7-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5fd7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5fd7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5fd7-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e5fd7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5fd7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5fd7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5fd7-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5fd7-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




