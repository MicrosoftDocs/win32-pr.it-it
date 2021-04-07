---
title: Messaggio TVM_GETLINECOLOR (COMmctrl. h)
description: Il \_ messaggio GETLINECOLOR TVM ottiene il colore della riga corrente.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Controlli di Windows Message TVM_GETLINECOLOR
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048513"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="2216c-104">\_Messaggio GETLINECOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="2216c-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="2216c-105">Il **messaggio \_ GETLINECOLOR TVM** ottiene il colore della riga corrente.</span><span class="sxs-lookup"><span data-stu-id="2216c-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="2216c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2216c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2216c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2216c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2216c-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2216c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2216c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2216c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2216c-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2216c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2216c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2216c-111">Return value</span></span>

<span data-ttu-id="2216c-112">Restituisce il colore della riga corrente oppure il \_ valore predefinito CLR se non ne è stato specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="2216c-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="2216c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2216c-113">Remarks</span></span>

<span data-ttu-id="2216c-114">Questo messaggio recupera solo i colori linea.</span><span class="sxs-lookup"><span data-stu-id="2216c-114">This message only retrieves line colors.</span></span> <span data-ttu-id="2216c-115">Per recuperare i colori di "+" e "-" all'interno dei pulsanti, usare il messaggio [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="2216c-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2216c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2216c-116">Requirements</span></span>



| <span data-ttu-id="2216c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2216c-117">Requirement</span></span> | <span data-ttu-id="2216c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2216c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2216c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2216c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2216c-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2216c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2216c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2216c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2216c-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2216c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2216c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2216c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2216c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2216c-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2216c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2216c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2216c-126">**\_SETLINECOLOR TVM**</span><span class="sxs-lookup"><span data-stu-id="2216c-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





