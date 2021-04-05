---
title: Messaggio LVM_GETGROUPINFO (COMmctrl. h)
description: Ottiene le informazioni sul gruppo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Controlli di Windows Message LVM_GETGROUPINFO
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048197"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="16ffb-104">\_Messaggio GETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="16ffb-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="16ffb-105">Ottiene le informazioni sul gruppo.</span><span class="sxs-lookup"><span data-stu-id="16ffb-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="16ffb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16ffb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16ffb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16ffb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="16ffb-108">ID che specifica il gruppo le cui informazioni vengono recuperate.</span><span class="sxs-lookup"><span data-stu-id="16ffb-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="16ffb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16ffb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="16ffb-110">Puntatore A una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> che riceve le informazioni recuperate.</span><span class="sxs-lookup"><span data-stu-id="16ffb-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="16ffb-111">Impostare il membro **cbSize** della struttura su sizeof (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="16ffb-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16ffb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16ffb-112">Return value</span></span>

<span data-ttu-id="16ffb-113">Restituisce l'ID del gruppo, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="16ffb-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="16ffb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="16ffb-114">Remarks</span></span>

<span data-ttu-id="16ffb-115">Prima di tentare di recuperare l'intestazione per un gruppo, verificare innanzitutto che il gruppo non abbia lo \_ stile NOheader LBGS.</span><span class="sxs-lookup"><span data-stu-id="16ffb-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="16ffb-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="16ffb-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="16ffb-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16ffb-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16ffb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16ffb-118">Requirements</span></span>



| <span data-ttu-id="16ffb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16ffb-119">Requirement</span></span> | <span data-ttu-id="16ffb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="16ffb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16ffb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16ffb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16ffb-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16ffb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16ffb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16ffb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16ffb-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16ffb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16ffb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16ffb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16ffb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16ffb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





