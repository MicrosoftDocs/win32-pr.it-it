---
title: Messaggio LVM_SETGROUPINFO (COMmctrl. h)
description: Imposta le informazioni sul gruppo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- Controlli di Windows Message LVM_SETGROUPINFO
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047854"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="7374c-104">\_Messaggio SETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="7374c-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="7374c-105">Imposta le informazioni sul gruppo.</span><span class="sxs-lookup"><span data-stu-id="7374c-105">Sets group information.</span></span> <span data-ttu-id="7374c-106">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetGroupInfo di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .</span><span class="sxs-lookup"><span data-stu-id="7374c-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7374c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7374c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7374c-108">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7374c-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="7374c-109">ID che specifica il gruppo di cui è necessario impostare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7374c-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="7374c-110">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7374c-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="7374c-111">Puntatore a una struttura [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) che contiene le informazioni da impostare.</span><span class="sxs-lookup"><span data-stu-id="7374c-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7374c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7374c-112">Return value</span></span>

<span data-ttu-id="7374c-113">Restituisce l'ID del gruppo, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7374c-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7374c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7374c-114">Remarks</span></span>

<span data-ttu-id="7374c-115">Per modificare l'ID di un gruppo esistente, aggiungere <b>LVGF_GROUPID</b> a <b>LVGROUP. mask</b> e impostare <b>LVGROUP. iGroupId</b> sul nuovo ID.</span><span class="sxs-lookup"><span data-stu-id="7374c-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="7374c-116">La chiamata avrà esito negativo se <b>LVGROUP. iGroupId</b> contiene l'ID di un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="7374c-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="7374c-117">Per aggiornare altre proprietà di un gruppo esistente (ad esempio, aggiornare un allineamento del testo dell'intestazione o del piè di pagina per il gruppo, <b>uAlign</b>) <b>LVGROUP. mask</b> non deve contenere <b>LVGF_GROUPID</b>. in caso contrario, l'aggiornamento avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7374c-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="7374c-118">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="7374c-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7374c-119">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7374c-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7374c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7374c-120">Requirements</span></span>



| <span data-ttu-id="7374c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7374c-121">Requirement</span></span> | <span data-ttu-id="7374c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7374c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7374c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7374c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7374c-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7374c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7374c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7374c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7374c-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7374c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7374c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7374c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7374c-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7374c-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





