---
title: Messaggio UDM_SETBASE (COMmctrl. h)
description: Imposta la base radice per un controllo di scorrimento. Il valore di base determina se la finestra Buddy Visualizza numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono firmati.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- Controlli di Windows Message UDM_SETBASE
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964544"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="4dc43-106">UDM- \_ messaggio di base</span><span class="sxs-lookup"><span data-stu-id="4dc43-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="4dc43-107">Imposta la base radice per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4dc43-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="4dc43-108">Il valore di base determina se la finestra Buddy Visualizza numeri in cifre decimali o esadecimali.</span><span class="sxs-lookup"><span data-stu-id="4dc43-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="4dc43-109">I numeri esadecimali sono sempre senza segno e i numeri decimali sono firmati.</span><span class="sxs-lookup"><span data-stu-id="4dc43-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dc43-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4dc43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc43-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dc43-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc43-112">Nuovo valore di base per il controllo.</span><span class="sxs-lookup"><span data-stu-id="4dc43-112">New base value for the control.</span></span> <span data-ttu-id="4dc43-113">Questo parametro può essere 10 per Decimal o 16 per l'esadecimale.</span><span class="sxs-lookup"><span data-stu-id="4dc43-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="4dc43-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dc43-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4dc43-115">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4dc43-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dc43-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4dc43-116">Return value</span></span>

<span data-ttu-id="4dc43-117">Il valore restituito è il valore di base precedente.</span><span class="sxs-lookup"><span data-stu-id="4dc43-117">The return value is the previous base value.</span></span> <span data-ttu-id="4dc43-118">Se viene specificata una base non valida, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="4dc43-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc43-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dc43-119">Requirements</span></span>



| <span data-ttu-id="4dc43-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc43-120">Requirement</span></span> | <span data-ttu-id="4dc43-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4dc43-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc43-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dc43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc43-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4dc43-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4dc43-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dc43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc43-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4dc43-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4dc43-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4dc43-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc43-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc43-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





