---
title: Messaggio TVM_SETLINECOLOR (COMmctrl. h)
description: Il \_ messaggio SETLINECOLOR TVM imposta il colore della riga corrente.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Controlli di Windows Message TVM_SETLINECOLOR
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048475"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="7d657-104">\_Messaggio SETLINECOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="7d657-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="7d657-105">Il **messaggio \_ SETLINECOLOR TVM** imposta il colore della riga corrente.</span><span class="sxs-lookup"><span data-stu-id="7d657-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d657-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d657-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d657-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d657-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7d657-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7d657-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7d657-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d657-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d657-110">Nuovo colore della linea.</span><span class="sxs-lookup"><span data-stu-id="7d657-110">New line color.</span></span> <span data-ttu-id="7d657-111">Usare il \_ valore CLR predefinito per ripristinare i colori predefiniti del sistema.</span><span class="sxs-lookup"><span data-stu-id="7d657-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d657-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d657-112">Return value</span></span>

<span data-ttu-id="7d657-113">Restituisce il colore della riga precedente.</span><span class="sxs-lookup"><span data-stu-id="7d657-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d657-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d657-114">Remarks</span></span>

<span data-ttu-id="7d657-115">Questo messaggio modifica solo i colori linea.</span><span class="sxs-lookup"><span data-stu-id="7d657-115">This message only changes line colors.</span></span> <span data-ttu-id="7d657-116">Per modificare i colori di "+" e "-" all'interno dei pulsanti, usare il messaggio [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="7d657-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d657-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d657-117">Requirements</span></span>



| <span data-ttu-id="7d657-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d657-118">Requirement</span></span> | <span data-ttu-id="7d657-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7d657-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d657-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d657-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d657-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d657-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d657-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d657-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d657-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d657-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d657-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d657-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d657-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d657-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d657-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d657-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d657-127">**\_GETLINECOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="7d657-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





