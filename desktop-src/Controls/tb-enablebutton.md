---
title: Messaggio TB_ENABLEBUTTON (COMmctrl. h)
description: Abilita o Disabilita il pulsante specificato in una barra degli strumenti.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Controlli di Windows Message TB_ENABLEBUTTON
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302784"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="62be0-104">TB \_ ENABLEBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="62be0-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="62be0-105">Abilita o Disabilita il pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="62be0-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="62be0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62be0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62be0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62be0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62be0-108">Identificatore di comando del pulsante da abilitare o disabilitare.</span><span class="sxs-lookup"><span data-stu-id="62be0-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="62be0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62be0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62be0-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **bool** che indica se abilitare o disabilitare il pulsante specificato.</span><span class="sxs-lookup"><span data-stu-id="62be0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="62be0-111">Se **true**, il pulsante è abilitato.</span><span class="sxs-lookup"><span data-stu-id="62be0-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="62be0-112">Se **false**, il pulsante è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="62be0-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62be0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62be0-113">Return value</span></span>

<span data-ttu-id="62be0-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="62be0-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="62be0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="62be0-115">Remarks</span></span>

<span data-ttu-id="62be0-116">Quando un pulsante è stato abilitato, è possibile premerlo e selezionarlo.</span><span class="sxs-lookup"><span data-stu-id="62be0-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="62be0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62be0-117">Requirements</span></span>



| <span data-ttu-id="62be0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62be0-118">Requirement</span></span> | <span data-ttu-id="62be0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="62be0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62be0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62be0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62be0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62be0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62be0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62be0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62be0-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62be0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62be0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62be0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62be0-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62be0-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

