---
title: Messaggio LVM_GETFOOTERINFO (COMmctrl. h)
description: Ottiene informazioni sul piè di pagina di un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterInfo di ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Controlli di Windows Message LVM_GETFOOTERINFO
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963767"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="0b162-105">\_Messaggio GETFOOTERINFO LVM</span><span class="sxs-lookup"><span data-stu-id="0b162-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="0b162-106">Ottiene informazioni sul piè di pagina di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="0b162-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="0b162-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterInfo di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .</span><span class="sxs-lookup"><span data-stu-id="0b162-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b162-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b162-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b162-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b162-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b162-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="0b162-110">Not used.</span></span> <span data-ttu-id="0b162-111">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="0b162-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="0b162-112">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0b162-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b162-113">Puntatore a una struttura [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) per ricevere informazioni a seconda del valore del membro **mask** .</span><span class="sxs-lookup"><span data-stu-id="0b162-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="0b162-114">Il processo chiamante è responsabile dell'allocazione della struttura e dell'impostazione del membro **mask** .</span><span class="sxs-lookup"><span data-stu-id="0b162-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b162-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b162-115">Return value</span></span>

<span data-ttu-id="0b162-116">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="0b162-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b162-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b162-117">Requirements</span></span>



| <span data-ttu-id="0b162-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b162-118">Requirement</span></span> | <span data-ttu-id="0b162-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0b162-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b162-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b162-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0b162-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b162-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b162-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b162-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0b162-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b162-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b162-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b162-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b162-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b162-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





