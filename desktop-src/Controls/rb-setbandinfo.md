---
title: Messaggio RB_SETBANDINFO (COMmctrl. h)
description: Imposta le caratteristiche di una banda esistente in un controllo Rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Controlli di Windows Message RB_SETBANDINFO
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477866"
---
# <a name="rb_setbandinfo-message"></a><span data-ttu-id="b8541-104">\_Messaggio SETBANDINFO RB</span><span class="sxs-lookup"><span data-stu-id="b8541-104">RB\_SETBANDINFO message</span></span>

<span data-ttu-id="b8541-105">Imposta le caratteristiche di una banda esistente in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="b8541-105">Sets characteristics of an existing band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8541-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8541-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8541-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8541-108">Indice in base zero della banda per ricevere le nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b8541-108">Zero-based index of the band to receive the new settings.</span></span>

</dd> <dt>

<span data-ttu-id="b8541-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8541-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8541-110">Puntatore a una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che definisce la banda da modificare e le nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b8541-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be modified and the new settings.</span></span> <span data-ttu-id="b8541-111">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura sulla struttura **sizeof**(REBARBANDINFO).</span><span class="sxs-lookup"><span data-stu-id="b8541-111">Before sending this message, you must set the **cbSize** member of this structure to the **sizeof**(REBARBANDINFO) structure.</span></span> <span data-ttu-id="b8541-112">Inoltre, è necessario impostare il **membro** REBARBANDINFO della struttura  sulla dimensione del buffer **lpText** quando \_ viene specificato il testo RBBIM.</span><span class="sxs-lookup"><span data-stu-id="b8541-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8541-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8541-113">Return value</span></span>

<span data-ttu-id="b8541-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b8541-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8541-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8541-115">Requirements</span></span>



| <span data-ttu-id="b8541-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8541-116">Requirement</span></span> | <span data-ttu-id="b8541-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b8541-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8541-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8541-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8541-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8541-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8541-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8541-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8541-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8541-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8541-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8541-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8541-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8541-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b8541-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b8541-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8541-125">**RB \_ SETBANDINFOW** (Unicode) e **RB \_ SETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8541-125">**RB\_SETBANDINFOW** (Unicode) and **RB\_SETBANDINFOA** (ANSI)</span></span><br/>             |



 

 





