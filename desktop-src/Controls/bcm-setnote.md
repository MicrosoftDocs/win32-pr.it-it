---
title: Messaggio BCM_SETNOTE (COMmctrl. h)
description: Imposta il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro di pulsanti \_ .
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Controlli di Windows Message BCM_SETNOTE
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964208"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="00506-105">\_Messaggio di nota BCM</span><span class="sxs-lookup"><span data-stu-id="00506-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="00506-106">Imposta il testo della nota associata a un pulsante di collegamento al comando.</span><span class="sxs-lookup"><span data-stu-id="00506-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="00506-107">È possibile inviare questo messaggio in modo esplicito o usare la macro di [**pulsanti \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .</span><span class="sxs-lookup"><span data-stu-id="00506-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="00506-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="00506-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00506-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00506-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00506-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="00506-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="00506-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00506-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00506-112">Puntatore a una stringa **WCHAR** con terminazione null che contiene la nota.</span><span class="sxs-lookup"><span data-stu-id="00506-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00506-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00506-113">Return value</span></span>

<span data-ttu-id="00506-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="00506-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00506-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="00506-115">Remarks</span></span>

<span data-ttu-id="00506-116">A partire dalla versione 6,01 di comctl32, i pulsanti di collegamento al comando possono avere una nota.</span><span class="sxs-lookup"><span data-stu-id="00506-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="00506-117">Il messaggio **BCM \_ Nota** funziona solo con gli stili dei pulsanti [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="00506-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="00506-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00506-118">Requirements</span></span>



| <span data-ttu-id="00506-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="00506-119">Requirement</span></span> | <span data-ttu-id="00506-120">Valore</span><span class="sxs-lookup"><span data-stu-id="00506-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00506-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00506-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00506-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00506-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00506-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00506-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00506-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00506-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00506-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00506-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00506-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00506-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00506-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00506-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="00506-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="00506-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="00506-129">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="00506-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="00506-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="00506-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00506-131">Tipi di pulsante</span><span class="sxs-lookup"><span data-stu-id="00506-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





