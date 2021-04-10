---
title: Messaggio TTM_GETCURRENTTOOL (COMmctrl. h)
description: Recupera le informazioni per lo strumento corrente in un controllo ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Controlli di Windows Message TTM_GETCURRENTTOOL
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964242"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="d3b85-104">\_Messaggio TTM GETCURRENTTOOL</span><span class="sxs-lookup"><span data-stu-id="d3b85-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="d3b85-105">Recupera le informazioni per lo strumento corrente in un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="d3b85-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3b85-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3b85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3b85-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d3b85-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d3b85-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d3b85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3b85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b85-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento corrente.</span><span class="sxs-lookup"><span data-stu-id="d3b85-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="d3b85-111">Se questo valore è **null**, il valore restituito indica l'esistenza dello strumento corrente senza recuperare effettivamente le informazioni sullo strumento.</span><span class="sxs-lookup"><span data-stu-id="d3b85-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="d3b85-112">Se questo valore non è **null**, prima di inviare questo messaggio è necessario compilare il membro **cbSize** della struttura **TOOLINFO** .</span><span class="sxs-lookup"><span data-stu-id="d3b85-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b85-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3b85-113">Return value</span></span>

<span data-ttu-id="d3b85-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d3b85-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="d3b85-115">Se *lParam* è **null**, restituisce un valore diverso da zero se esiste uno strumento corrente oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d3b85-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b85-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3b85-116">Requirements</span></span>



| <span data-ttu-id="d3b85-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b85-117">Requirement</span></span> | <span data-ttu-id="d3b85-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d3b85-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b85-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3b85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b85-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3b85-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3b85-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3b85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b85-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3b85-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3b85-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3b85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b85-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3b85-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d3b85-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d3b85-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d3b85-126">**TTM \_ GETCURRENTTOOLW** (Unicode) e **TTM \_ GETCURRENTTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d3b85-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





