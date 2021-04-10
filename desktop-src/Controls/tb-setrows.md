---
title: Messaggio TB_SETROWS (COMmctrl. h)
description: Imposta il numero di righe di pulsanti in una barra degli strumenti.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- Controlli di Windows Message TB_SETROWS
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048768"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="957c7-104">\_Messaggio di righe TB</span><span class="sxs-lookup"><span data-stu-id="957c7-104">TB\_SETROWS message</span></span>

<span data-ttu-id="957c7-105">Imposta il numero di righe di pulsanti in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="957c7-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="957c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="957c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="957c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="957c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="957c7-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il numero di righe richieste.</span><span class="sxs-lookup"><span data-stu-id="957c7-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="957c7-109">Il numero minimo di righe è uno e il numero massimo di righe è uguale al numero di pulsanti nella barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="957c7-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="957c7-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un **bool** che indica se creare più righe rispetto a quelle richieste quando il sistema non è in grado di creare il numero di righe specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="957c7-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="957c7-111">Se **true**, il sistema crea più righe.</span><span class="sxs-lookup"><span data-stu-id="957c7-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="957c7-112">Se **false**, il sistema crea un minor numero di righe.</span><span class="sxs-lookup"><span data-stu-id="957c7-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="957c7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="957c7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="957c7-114">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo delimitatore della barra degli strumenti dopo l'impostazione delle righe.</span><span class="sxs-lookup"><span data-stu-id="957c7-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="957c7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="957c7-115">Return value</span></span>

<span data-ttu-id="957c7-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="957c7-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="957c7-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="957c7-117">Remarks</span></span>

<span data-ttu-id="957c7-118">Poiché il sistema non suddivide i gruppi di pulsanti quando si imposta il numero di righe, il numero di righe risultante potrebbe essere diverso da quello richiesto.</span><span class="sxs-lookup"><span data-stu-id="957c7-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="957c7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="957c7-119">Requirements</span></span>



| <span data-ttu-id="957c7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="957c7-120">Requirement</span></span> | <span data-ttu-id="957c7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="957c7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="957c7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="957c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="957c7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="957c7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="957c7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="957c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="957c7-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="957c7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="957c7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="957c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="957c7-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="957c7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

