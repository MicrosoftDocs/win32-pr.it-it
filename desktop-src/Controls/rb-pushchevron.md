---
title: Messaggio RB_PUSHCHEVRON (COMmctrl. h)
description: Inviato a un controllo Rebar per eseguire il push a livello di codice di una freccia di espansione.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- Controlli di Windows Message RB_PUSHCHEVRON
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518274"
---
# <a name="rb_pushchevron-message"></a><span data-ttu-id="35b9f-104">\_Messaggio PUSHCHEVRON RB</span><span class="sxs-lookup"><span data-stu-id="35b9f-104">RB\_PUSHCHEVRON message</span></span>

<span data-ttu-id="35b9f-105">Inviato a un controllo Rebar per eseguire il push a livello di codice di una freccia di espansione.</span><span class="sxs-lookup"><span data-stu-id="35b9f-105">Sent to a rebar control to programmatically push a chevron.</span></span>

## <a name="parameters"></a><span data-ttu-id="35b9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35b9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b9f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35b9f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35b9f-108">Indice in base zero della banda di cui deve essere eseguito il push della freccia di espansione.</span><span class="sxs-lookup"><span data-stu-id="35b9f-108">Zero-based index of the band whose chevron is to be pushed.</span></span>

</dd> <dt>

<span data-ttu-id="35b9f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35b9f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35b9f-110">Valore a 32 bit definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35b9f-110">An application defined 32-bit value.</span></span> <span data-ttu-id="35b9f-111">Viene passato nuovamente all'applicazione come membro **lParamNM** della struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) che viene passata con la notifica [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) .</span><span class="sxs-lookup"><span data-stu-id="35b9f-111">It will be passed back to the application as the **lParamNM** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure that is passed with the [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b9f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35b9f-112">Return value</span></span>

<span data-ttu-id="35b9f-113">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="35b9f-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="35b9f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="35b9f-114">Remarks</span></span>

<span data-ttu-id="35b9f-115">Quando questo messaggio viene inviato, il controllo Rebar invierà all'applicazione un codice di notifica [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , in cui viene richiesto di visualizzare il menu della freccia di espansione.</span><span class="sxs-lookup"><span data-stu-id="35b9f-115">When this message is sent, the rebar control will send the application an [RBN\_CHEVRONPUSHED](rbn-chevronpushed.md) notification code, prompting it to display the chevron menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b9f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35b9f-116">Requirements</span></span>



| <span data-ttu-id="35b9f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="35b9f-117">Requirement</span></span> | <span data-ttu-id="35b9f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="35b9f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35b9f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35b9f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35b9f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35b9f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35b9f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35b9f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35b9f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35b9f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35b9f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35b9f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b9f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b9f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





