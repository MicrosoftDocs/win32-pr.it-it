---
title: Messaggio TTM_GETTEXT (COMmctrl. h)
description: Recupera le informazioni gestite da un controllo ToolTip su uno strumento.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Controlli di Windows Message TTM_GETTEXT
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301653"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="267fd-104">TTM \_ messaggio GETtext</span><span class="sxs-lookup"><span data-stu-id="267fd-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="267fd-105">Recupera le informazioni gestite da un controllo ToolTip su uno strumento.</span><span class="sxs-lookup"><span data-stu-id="267fd-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="267fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="267fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="267fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="267fd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="267fd-108">Il numero di **TCHARs**, incluso il **null** di terminazione, da copiare nel buffer a cui punta **lpszText**.</span><span class="sxs-lookup"><span data-stu-id="267fd-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="267fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="267fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="267fd-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="267fd-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="267fd-111">Impostare il membro **cbSize** della struttura su `sizeof(TOOLINFO)` prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="267fd-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="267fd-112">Impostare i membri **HWND** e **UID** per identificare lo strumento per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="267fd-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="267fd-113">Allocare un buffer di dimensioni specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="267fd-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="267fd-114">Impostare il membro **lpszText** in modo che punti al buffer per ricevere il testo dello strumento.</span><span class="sxs-lookup"><span data-stu-id="267fd-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="267fd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="267fd-115">Return value</span></span>

<span data-ttu-id="267fd-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="267fd-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="267fd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="267fd-117">Requirements</span></span>



| <span data-ttu-id="267fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="267fd-118">Requirement</span></span> | <span data-ttu-id="267fd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="267fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="267fd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="267fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="267fd-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="267fd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="267fd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="267fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="267fd-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="267fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="267fd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="267fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="267fd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="267fd-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="267fd-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="267fd-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="267fd-127">**TTM \_ GETTEXTW** (Unicode) e **TTM \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="267fd-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





