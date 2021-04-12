---
title: Messaggio TB_SETINSERTMARKCOLOR (COMmctrl. h)
description: Imposta il colore utilizzato per creare il segno di inserimento per la barra degli strumenti.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- Controlli di Windows Message TB_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118971"
---
# <a name="tb_setinsertmarkcolor-message"></a><span data-ttu-id="e9482-104">TB \_ SETINSERTMARKCOLOR messaggio</span><span class="sxs-lookup"><span data-stu-id="e9482-104">TB\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="e9482-105">Imposta il colore utilizzato per creare il segno di inserimento per la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e9482-105">Sets the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9482-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9482-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9482-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9482-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e9482-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e9482-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e9482-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9482-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9482-110">Valore di **COLORREF** che contiene il nuovo colore del segno di inserimento.</span><span class="sxs-lookup"><span data-stu-id="e9482-110">**COLORREF** value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9482-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9482-111">Return value</span></span>

<span data-ttu-id="e9482-112">Restituisce un valore **COLORREF** che contiene il colore del segno di inserimento precedente.</span><span class="sxs-lookup"><span data-stu-id="e9482-112">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9482-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9482-113">Requirements</span></span>



| <span data-ttu-id="e9482-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9482-114">Requirement</span></span> | <span data-ttu-id="e9482-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e9482-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9482-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9482-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9482-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9482-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9482-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9482-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9482-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9482-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9482-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9482-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9482-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9482-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9482-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9482-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9482-123">**TB \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="e9482-123">**TB\_GETINSERTMARKCOLOR**</span></span>](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





