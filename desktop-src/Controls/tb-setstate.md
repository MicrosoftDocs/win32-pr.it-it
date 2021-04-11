---
title: Messaggio TB_SETSTATE (COMmctrl. h)
description: Imposta lo stato del pulsante specificato in una barra degli strumenti.
ms.assetid: 68633b58-8d21-4931-b01f-32a66bda37b1
keywords:
- Controlli di Windows Message TB_SETSTATE
topic_type:
- apiref
api_name:
- TB_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aa46dc68d9af5559e580e697bf6893b15051cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121710"
---
# <a name="tb_setstate-message"></a><span data-ttu-id="a978c-104">TB- \_ messaggio di stato</span><span class="sxs-lookup"><span data-stu-id="a978c-104">TB\_SETSTATE message</span></span>

<span data-ttu-id="a978c-105">Imposta lo stato del pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="a978c-105">Sets the state for the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a978c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a978c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a978c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a978c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a978c-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="a978c-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="a978c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a978c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a978c-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è una combinazione di valori elencati negli [stati dei pulsanti della barra degli strumenti](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="a978c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a combination of values listed in [Toolbar Button States](toolbar-button-states.md).</span></span> <span data-ttu-id="a978c-111">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a978c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a978c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a978c-112">Return value</span></span>

<span data-ttu-id="a978c-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a978c-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a978c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a978c-114">Requirements</span></span>



| <span data-ttu-id="a978c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a978c-115">Requirement</span></span> | <span data-ttu-id="a978c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a978c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a978c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a978c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a978c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a978c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a978c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a978c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a978c-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a978c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a978c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a978c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a978c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a978c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

