---
title: Messaggio di EM_EXSETSEL (RichEdit. h)
description: Seleziona un intervallo di caratteri o oggetti Component Object Model (COM) in un controllo Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Controlli di Windows Message EM_EXSETSEL
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874049"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="9f62d-104">\_Messaggio EXSETSEL em</span><span class="sxs-lookup"><span data-stu-id="9f62d-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="9f62d-105">Seleziona un intervallo di caratteri o oggetti Component Object Model (COM) in un controllo Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9f62d-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f62d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f62d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f62d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f62d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f62d-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9f62d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9f62d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f62d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f62d-110">Struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che specifica l'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="9f62d-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f62d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f62d-111">Return value</span></span>

<span data-ttu-id="9f62d-112">Il valore restituito è la selezione effettivamente impostata.</span><span class="sxs-lookup"><span data-stu-id="9f62d-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f62d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f62d-113">Requirements</span></span>



| <span data-ttu-id="9f62d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f62d-114">Requirement</span></span> | <span data-ttu-id="9f62d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9f62d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f62d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f62d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f62d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f62d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f62d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f62d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f62d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f62d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f62d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f62d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f62d-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f62d-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





