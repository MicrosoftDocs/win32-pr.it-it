---
title: Messaggio TB_GETINSERTMARKCOLOR (COMmctrl. h)
description: Recupera il colore utilizzato per tracciare il segno di inserimento per la barra degli strumenti.
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- Controlli di Windows Message TB_GETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ceebd5f3989ed870cf70ccad819300d85c05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873837"
---
# <a name="tb_getinsertmarkcolor-message"></a><span data-ttu-id="f869b-104">TB \_ GETINSERTMARKCOLOR messaggio</span><span class="sxs-lookup"><span data-stu-id="f869b-104">TB\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="f869b-105">Recupera il colore utilizzato per tracciare il segno di inserimento per la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f869b-105">Retrieves the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f869b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f869b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f869b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f869b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f869b-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f869b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f869b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f869b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f869b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f869b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f869b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f869b-111">Return value</span></span>

<span data-ttu-id="f869b-112">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il colore del segno di inserimento corrente.</span><span class="sxs-lookup"><span data-stu-id="f869b-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="f869b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f869b-113">Requirements</span></span>



| <span data-ttu-id="f869b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f869b-114">Requirement</span></span> | <span data-ttu-id="f869b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f869b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f869b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f869b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f869b-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f869b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f869b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f869b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f869b-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f869b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f869b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f869b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f869b-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f869b-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f869b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f869b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f869b-123">**TB \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="f869b-123">**TB\_SETINSERTMARKCOLOR**</span></span>](tb-setinsertmarkcolor.md)
</dt> </dl>

 

