---
title: Messaggio RB_SETBARINFO (COMmctrl. h)
description: Imposta le caratteristiche di un controllo Rebar.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- Controlli di Windows Message RB_SETBARINFO
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047918"
---
# <a name="rb_setbarinfo-message"></a><span data-ttu-id="f9edc-104">\_Messaggio SETBARINFO RB</span><span class="sxs-lookup"><span data-stu-id="f9edc-104">RB\_SETBARINFO message</span></span>

<span data-ttu-id="f9edc-105">Imposta le caratteristiche di un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="f9edc-105">Sets the characteristics of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9edc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9edc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9edc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9edc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f9edc-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f9edc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f9edc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9edc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9edc-110">Puntatore a una struttura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) che contiene le informazioni da impostare.</span><span class="sxs-lookup"><span data-stu-id="f9edc-110">Pointer to a [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) structure that contains the information to be set.</span></span> <span data-ttu-id="f9edc-111">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(REBARINFO).</span><span class="sxs-lookup"><span data-stu-id="f9edc-111">You must set the **cbSize** member of this structure to **sizeof**(REBARINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9edc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9edc-112">Return value</span></span>

<span data-ttu-id="f9edc-113">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f9edc-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9edc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9edc-114">Requirements</span></span>



| <span data-ttu-id="f9edc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9edc-115">Requirement</span></span> | <span data-ttu-id="f9edc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f9edc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9edc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9edc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f9edc-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9edc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9edc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9edc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f9edc-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9edc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9edc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9edc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9edc-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9edc-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





