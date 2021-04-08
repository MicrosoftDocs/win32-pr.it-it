---
title: Messaggio TB_GETIDEALSIZE (COMmctrl. h)
description: Ottiene la dimensione ideale della barra degli strumenti.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Controlli di Windows Message TB_GETIDEALSIZE
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047990"
---
# <a name="tb_getidealsize-message"></a><span data-ttu-id="7c422-104">TB \_ GETIDEALSIZE messaggio</span><span class="sxs-lookup"><span data-stu-id="7c422-104">TB\_GETIDEALSIZE message</span></span>

<span data-ttu-id="7c422-105">Ottiene la dimensione ideale della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7c422-105">Gets the ideal size of the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c422-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c422-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c422-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c422-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7c422-108">Valore **booleano** che indica se recuperare l'altezza o la larghezza ideale della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7c422-108">A **BOOL** that indicates whether to retrieve the ideal height or width of the toolbar.</span></span> <span data-ttu-id="7c422-109">Utilizzare **true** per recuperare l'altezza ideale, **false** per recuperare la larghezza ideale.</span><span class="sxs-lookup"><span data-stu-id="7c422-109">Use **TRUE** to retrieve the ideal height, **FALSE** to retrieve the ideal width.</span></span></dd> <dt>

<span data-ttu-id="7c422-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c422-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c422-111">Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che riceve l'altezza o la larghezza in corrispondenza della quale verranno visualizzati tutti i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="7c422-111">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the height or width at which all buttons would be displayed.</span></span> <span data-ttu-id="7c422-112">Se *wParam* è **true**, solo il membro **CY** (Height) è valido.</span><span class="sxs-lookup"><span data-stu-id="7c422-112">If *wParam* is **TRUE**, only the **cy** member (height) is valid.</span></span> <span data-ttu-id="7c422-113">Se *wParam* è **false**, solo il membro **CX** (width) è valido.</span><span class="sxs-lookup"><span data-stu-id="7c422-113">If *wParam* is **FALSE**, only the **cx** member (width) is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c422-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c422-114">Return value</span></span>

<span data-ttu-id="7c422-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7c422-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c422-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c422-116">Requirements</span></span>



| <span data-ttu-id="7c422-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c422-117">Requirement</span></span> | <span data-ttu-id="7c422-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7c422-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c422-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c422-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c422-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c422-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c422-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c422-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c422-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c422-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c422-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c422-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c422-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c422-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

