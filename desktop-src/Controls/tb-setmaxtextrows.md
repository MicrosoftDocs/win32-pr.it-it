---
title: Messaggio TB_SETMAXTEXTROWS (COMmctrl. h)
description: Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Controlli di Windows Message TB_SETMAXTEXTROWS
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963938"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="4112b-104">TB \_ SETMAXTEXTROWS messaggio</span><span class="sxs-lookup"><span data-stu-id="4112b-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="4112b-105">Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="4112b-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="4112b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4112b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4112b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4112b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4112b-108">Numero massimo di righe di testo che è possibile visualizzare.</span><span class="sxs-lookup"><span data-stu-id="4112b-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="4112b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4112b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4112b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4112b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4112b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4112b-111">Return value</span></span>

<span data-ttu-id="4112b-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4112b-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4112b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4112b-113">Remarks</span></span>

<span data-ttu-id="4112b-114">Per fare in modo che il testo venga incapsulato, è necessario impostare la larghezza massima del pulsante inviando un messaggio [**\_ SETBUTTONWIDTH TB**](tb-setbuttonwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="4112b-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="4112b-115">Il testo viene incapsulato in corrispondenza di una parola break; le interruzioni di riga (" \\ n") nel testo vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="4112b-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="4112b-116">Il testo nelle \_ barre degli strumenti dell'elenco TBSTYLE viene sempre visualizzato su una sola riga.</span><span class="sxs-lookup"><span data-stu-id="4112b-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="4112b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4112b-117">Requirements</span></span>



| <span data-ttu-id="4112b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4112b-118">Requirement</span></span> | <span data-ttu-id="4112b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4112b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4112b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4112b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4112b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4112b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4112b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4112b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4112b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4112b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4112b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4112b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4112b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4112b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





