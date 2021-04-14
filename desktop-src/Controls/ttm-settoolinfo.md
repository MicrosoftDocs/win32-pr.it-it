---
title: Messaggio TTM_SETTOOLINFO (COMmctrl. h)
description: Imposta le informazioni che un controllo ToolTip gestisce per uno strumento.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Controlli di Windows Message TTM_SETTOOLINFO
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478952"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="c4358-104">\_Messaggio TTM SETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="c4358-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="c4358-105">Imposta le informazioni che un controllo ToolTip gestisce per uno strumento.</span><span class="sxs-lookup"><span data-stu-id="c4358-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4358-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4358-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4358-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4358-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c4358-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c4358-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c4358-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4358-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4358-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che specifica le informazioni da impostare.</span><span class="sxs-lookup"><span data-stu-id="c4358-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="c4358-111">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura.</span><span class="sxs-lookup"><span data-stu-id="c4358-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4358-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4358-112">Return value</span></span>

<span data-ttu-id="c4358-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c4358-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4358-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4358-114">Remarks</span></span>

<span data-ttu-id="c4358-115">Alcune proprietà interne di uno strumento vengono stabilite quando lo strumento viene creato e non vengono ricalcolate quando viene inviato un messaggio **TTM \_ SETTOOLINFO** .</span><span class="sxs-lookup"><span data-stu-id="c4358-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="c4358-116">Se si assegnano semplicemente valori a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) e lo si passa al controllo ToolTip con un messaggio **\_ SETTOOLINFO di TTM** , queste proprietà potrebbero andare perse.</span><span class="sxs-lookup"><span data-stu-id="c4358-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="c4358-117">Al contrario, l'applicazione deve prima richiedere la struttura **TOOLINFO** corrente dello strumento inviando la descrizione comando di un messaggio [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c4358-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="c4358-118">Modificare quindi i membri di questa struttura in base alle esigenze e passarli di nuovo al controllo ToolTip con **TTM \_ SETTOOLINFO**.</span><span class="sxs-lookup"><span data-stu-id="c4358-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="c4358-119">Quando si chiama **TTM \_ SETTOOLINFO**, la stringa a cui punta il membro **lpszText** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) non deve superare 80 **TCHARs** di lunghezza, incluso il **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c4358-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4358-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4358-120">Requirements</span></span>



| <span data-ttu-id="c4358-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4358-121">Requirement</span></span> | <span data-ttu-id="c4358-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c4358-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4358-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4358-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4358-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4358-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4358-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4358-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4358-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4358-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4358-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4358-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4358-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4358-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c4358-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c4358-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4358-130">**TTM \_ SETTOOLINFOW** (Unicode) e **TTM \_ SETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c4358-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





