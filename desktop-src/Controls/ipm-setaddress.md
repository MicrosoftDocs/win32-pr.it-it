---
title: Messaggio IPM_SETADDRESS (COMmctrl. h)
description: Imposta i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Controlli di Windows Message IPM_SETADDRESS
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120294"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="7477a-104">\_Messaggio di indirizzo IPM</span><span class="sxs-lookup"><span data-stu-id="7477a-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="7477a-105">Imposta i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="7477a-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7477a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7477a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7477a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7477a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7477a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7477a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7477a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7477a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7477a-110">Valore **DWORD** che contiene il nuovo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7477a-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="7477a-111">Il valore del campo 3 è contenuto nei bit da 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="7477a-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="7477a-112">Il valore del campo 2 è contenuto in bit da 8 a 15.</span><span class="sxs-lookup"><span data-stu-id="7477a-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="7477a-113">Il valore del campo 1 è contenuto nei bit da 16 a 23.</span><span class="sxs-lookup"><span data-stu-id="7477a-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="7477a-114">Il valore del campo 0 è contenuto nei bit da 24 a 31.</span><span class="sxs-lookup"><span data-stu-id="7477a-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="7477a-115">La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) può essere usata anche per creare le informazioni sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7477a-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7477a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7477a-116">Return value</span></span>

<span data-ttu-id="7477a-117">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7477a-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7477a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7477a-118">Remarks</span></span>

<span data-ttu-id="7477a-119">Questo messaggio non genera una notifica [**IPN \_ FIELDCHANGED**](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7477a-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="7477a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7477a-120">Requirements</span></span>



| <span data-ttu-id="7477a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7477a-121">Requirement</span></span> | <span data-ttu-id="7477a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7477a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7477a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7477a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7477a-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7477a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7477a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7477a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7477a-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7477a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7477a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7477a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7477a-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7477a-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





