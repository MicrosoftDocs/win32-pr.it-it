---
title: Messaggio TBM_GETBUDDY (COMmctrl. h)
description: Recupera l'handle a una finestra buddy del controllo TrackBar in una posizione specificata. La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- Controlli di Windows message TBM_GETBUDDY
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964997"
---
# <a name="tbm_getbuddy-message"></a><span data-ttu-id="f0b81-105">\_Messaggio TBM GETbuddy</span><span class="sxs-lookup"><span data-stu-id="f0b81-105">TBM\_GETBUDDY message</span></span>

<span data-ttu-id="f0b81-106">Recupera l'handle a una finestra buddy del controllo TrackBar in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f0b81-106">Retrieves the handle to a trackbar control buddy window at a given location.</span></span> <span data-ttu-id="f0b81-107">La posizione specificata è relativa all'orientamento del controllo (orizzontale o verticale).</span><span class="sxs-lookup"><span data-stu-id="f0b81-107">The specified location is relative to the control's orientation (horizontal or vertical).</span></span>

## <a name="parameters"></a><span data-ttu-id="f0b81-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0b81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b81-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0b81-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b81-110">Valore che indica quale handle della finestra buddy verrà recuperato in base alla posizione relativa.</span><span class="sxs-lookup"><span data-stu-id="f0b81-110">Value indicating which buddy window handle will be retrieved, by relative location.</span></span> <span data-ttu-id="f0b81-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0b81-111">This value can be one of the following:</span></span>



| <span data-ttu-id="f0b81-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f0b81-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="f0b81-113">Significato</span><span class="sxs-lookup"><span data-stu-id="f0b81-113">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f0b81-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f0b81-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="f0b81-115">Recupera l'handle per l'oggetto Buddy a sinistra del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f0b81-115">Retrieves the handle to the buddy to the left of the trackbar.</span></span> <span data-ttu-id="f0b81-116">Se il controllo TrackBar utilizza lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , il messaggio recupererà l'oggetto Buddy sopra il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f0b81-116">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy above the trackbar.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f0b81-117"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f0b81-117"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="f0b81-118">Recupera l'handle per l'oggetto Buddy a destra del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f0b81-118">Retrieves the handle to the buddy to the right of the trackbar.</span></span> <span data-ttu-id="f0b81-119">Se il controllo TrackBar utilizza lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , il messaggio recupererà l'oggetto Buddy al di sotto di TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f0b81-119">If the trackbar control uses the [**TBS\_VERT**](trackbar-control-styles.md) style, the message will retrieve the buddy below the trackbar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f0b81-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0b81-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f0b81-121">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f0b81-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b81-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0b81-122">Return value</span></span>

<span data-ttu-id="f0b81-123">Restituisce l'handle per la finestra di Buddy nella posizione specificata da *wParam* oppure **null** se non esiste alcuna finestra di Buddy in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="f0b81-123">Returns the handle to the buddy window at the location specified by *wParam*, or **NULL** if no buddy window exists at that location.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b81-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0b81-124">Requirements</span></span>



| <span data-ttu-id="f0b81-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0b81-125">Requirement</span></span> | <span data-ttu-id="f0b81-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f0b81-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b81-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0b81-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b81-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0b81-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0b81-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0b81-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b81-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0b81-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0b81-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0b81-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b81-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b81-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





