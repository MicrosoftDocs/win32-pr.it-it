---
title: Messaggio SB_GETICON (COMmctrl. h)
description: Recupera l'icona per una parte in una barra di stato.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Controlli di Windows Message SB_GETICON
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874230"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="de188-104">\_Messaggio SB GETicon</span><span class="sxs-lookup"><span data-stu-id="de188-104">SB\_GETICON message</span></span>

<span data-ttu-id="de188-105">Recupera l'icona per una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="de188-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="de188-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de188-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de188-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de188-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de188-108">Indice in base zero della parte che contiene l'icona da recuperare.</span><span class="sxs-lookup"><span data-stu-id="de188-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="de188-109">Se questo parametro è-1, si presuppone che la barra di stato sia una barra di stato in [modalità semplice](status-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="de188-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="de188-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de188-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="de188-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="de188-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de188-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de188-112">Return value</span></span>

<span data-ttu-id="de188-113">Restituisce l'handle per l'icona in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="de188-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de188-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de188-114">Requirements</span></span>



| <span data-ttu-id="de188-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="de188-115">Requirement</span></span> | <span data-ttu-id="de188-116">Valore</span><span class="sxs-lookup"><span data-stu-id="de188-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de188-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de188-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de188-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de188-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de188-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de188-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de188-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="de188-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de188-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de188-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de188-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de188-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





