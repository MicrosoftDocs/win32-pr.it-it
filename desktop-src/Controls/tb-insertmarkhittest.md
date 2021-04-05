---
title: Messaggio TB_INSERTMARKHITTEST (COMmctrl. h)
description: Recupera le informazioni sul segno di inserimento per un punto in una barra degli strumenti.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Controlli di Windows Message TB_INSERTMARKHITTEST
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048188"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="87af8-104">TB \_ INSERTMARKHITTEST messaggio</span><span class="sxs-lookup"><span data-stu-id="87af8-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="87af8-105">Recupera le informazioni sul segno di inserimento per un punto in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="87af8-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="87af8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87af8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87af8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87af8-108">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che contiene le coordinate dell'hit test rispetto all'area client della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="87af8-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="87af8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87af8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87af8-110">Puntatore a una struttura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) che riceve le informazioni sul segno di inserimento.</span><span class="sxs-lookup"><span data-stu-id="87af8-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87af8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87af8-111">Return value</span></span>

<span data-ttu-id="87af8-112">Restituisce un valore diverso da zero se il punto è un segno di inserimento oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="87af8-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="87af8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87af8-113">Requirements</span></span>



| <span data-ttu-id="87af8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="87af8-114">Requirement</span></span> | <span data-ttu-id="87af8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="87af8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87af8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87af8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="87af8-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87af8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87af8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87af8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="87af8-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87af8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87af8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87af8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="87af8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87af8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

