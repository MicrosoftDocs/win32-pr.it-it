---
title: Messaggio LVM_GETGROUPINFOBYINDEX (COMmctrl. h)
description: Ottiene informazioni su un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetGroupInfoByIndex di ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- Controlli di Windows Message LVM_GETGROUPINFOBYINDEX
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120290"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="dc0ce-105">\_Messaggio GETGROUPINFOBYINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="dc0ce-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="dc0ce-106">Ottiene informazioni su un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="dc0ce-106">Gets information on a specified group.</span></span> <span data-ttu-id="dc0ce-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetGroupInfoByIndex di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .</span><span class="sxs-lookup"><span data-stu-id="dc0ce-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc0ce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc0ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0ce-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc0ce-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0ce-110">Indice del gruppo.</span><span class="sxs-lookup"><span data-stu-id="dc0ce-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="dc0ce-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="dc0ce-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0ce-112">Puntatore a una struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) per ricevere informazioni sul gruppo specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="dc0ce-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="dc0ce-113">Il processo chiamante è responsabile dell'allocazione della memoria per la struttura e di tutti i buffer nella struttura, ad esempio quella a cui fa riferimento il membro **pszHeader** .</span><span class="sxs-lookup"><span data-stu-id="dc0ce-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="dc0ce-114">Impostare qualsiasi membro contingente della struttura, ad esempio **cchHeader** , la dimensione del buffer a cui punta **pszHeader** in **WCHAR** , incluso il **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="dc0ce-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="dc0ce-115">Impostare **cbSize** su sizeof (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="dc0ce-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="dc0ce-116">Il ricevitore del messaggio è responsabile dell'impostazione dei membri della struttura con le informazioni per il gruppo specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="dc0ce-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0ce-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc0ce-117">Return value</span></span>

<span data-ttu-id="dc0ce-118">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dc0ce-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0ce-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc0ce-119">Requirements</span></span>



| <span data-ttu-id="dc0ce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc0ce-120">Requirement</span></span> | <span data-ttu-id="dc0ce-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dc0ce-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0ce-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc0ce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc0ce-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc0ce-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc0ce-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc0ce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc0ce-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc0ce-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc0ce-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc0ce-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc0ce-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0ce-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





