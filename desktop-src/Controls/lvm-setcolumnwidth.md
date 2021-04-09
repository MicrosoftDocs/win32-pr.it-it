---
title: Messaggio LVM_SETCOLUMNWIDTH (COMmctrl. h)
description: Modifica la larghezza di una colonna in modalità di visualizzazione report o la larghezza di tutte le colonne in modalità visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetColumnWidth di ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Controlli di Windows Message LVM_SETCOLUMNWIDTH
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118998"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="ed958-105">\_Messaggio SETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="ed958-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="ed958-106">Modifica la larghezza di una colonna in modalità di visualizzazione report o la larghezza di tutte le colonne in modalità visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="ed958-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="ed958-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetColumnWidth di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="ed958-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed958-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed958-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed958-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed958-110">Indice in base zero di una colonna valida.</span><span class="sxs-lookup"><span data-stu-id="ed958-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="ed958-111">Per la modalità di visualizzazione elenco, questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="ed958-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ed958-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed958-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed958-113">Nuova larghezza della colonna in pixel.</span><span class="sxs-lookup"><span data-stu-id="ed958-113">New width of the column, in pixels.</span></span> <span data-ttu-id="ed958-114">Per la modalità di visualizzazione report, sono supportati i valori speciali seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed958-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="ed958-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ed958-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="ed958-116">Significato</span><span class="sxs-lookup"><span data-stu-id="ed958-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="ed958-117"><dt>**\_ridimensionamento automatico LVSCW**</dt></span><span class="sxs-lookup"><span data-stu-id="ed958-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="ed958-118">Ridimensiona automaticamente la colonna.</span><span class="sxs-lookup"><span data-stu-id="ed958-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="ed958-119"><dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt></span><span class="sxs-lookup"><span data-stu-id="ed958-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="ed958-120">Ridimensiona automaticamente la colonna per adattarla al testo dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="ed958-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="ed958-121">Se si usa questo valore con l'ultima colonna, la larghezza viene impostata in modo da riempire la larghezza rimanente del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="ed958-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed958-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed958-122">Return value</span></span>

<span data-ttu-id="ed958-123">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ed958-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed958-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed958-124">Remarks</span></span>

<span data-ttu-id="ed958-125">Si supponga di disporre di un controllo di visualizzazione elenco a 2 colonne con una larghezza di 500 pixel.</span><span class="sxs-lookup"><span data-stu-id="ed958-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="ed958-126">Se la larghezza della colonna zero è impostata su 200 pixel e si invia questo messaggio con *wParam* = 1 e *lParam* = LVSCW \_ AUTOSIZE \_ USEHEADER, la seconda colonna (e l'ultima) sarà 300 pixel di larghezza.</span><span class="sxs-lookup"><span data-stu-id="ed958-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed958-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed958-127">Requirements</span></span>



| <span data-ttu-id="ed958-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed958-128">Requirement</span></span> | <span data-ttu-id="ed958-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed958-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed958-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed958-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed958-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed958-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed958-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed958-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed958-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed958-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed958-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed958-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed958-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed958-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





