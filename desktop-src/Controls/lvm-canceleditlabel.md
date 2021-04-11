---
title: Messaggio LVM_CANCELEDITLABEL (COMmctrl. h)
description: Annulla l'operazione di modifica del testo di un elemento.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- Controlli di Windows Message LVM_CANCELEDITLABEL
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119014"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="6d963-104">\_Messaggio CANCELEDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="6d963-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="6d963-105">Annulla l'operazione di modifica del testo di un elemento.</span><span class="sxs-lookup"><span data-stu-id="6d963-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d963-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d963-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d963-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d963-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6d963-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6d963-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6d963-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d963-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6d963-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6d963-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d963-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d963-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d963-112">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="6d963-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6d963-113">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6d963-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="6d963-114">Questo messaggio causa l'invio di una notifica [ \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="6d963-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d963-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d963-115">Requirements</span></span>



| <span data-ttu-id="6d963-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d963-116">Requirement</span></span> | <span data-ttu-id="6d963-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6d963-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d963-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d963-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6d963-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d963-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d963-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d963-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6d963-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d963-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d963-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d963-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d963-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d963-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





