---
title: Messaggio IPM_GETADDRESS (COMmctrl. h)
description: Ottiene i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Controlli di Windows Message IPM_GETADDRESS
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964476"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="26a6a-104">\_Messaggio IPM GETaddress</span><span class="sxs-lookup"><span data-stu-id="26a6a-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="26a6a-105">Ottiene i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="26a6a-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="26a6a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26a6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26a6a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26a6a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="26a6a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="26a6a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="26a6a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26a6a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26a6a-110">Puntatore a un valore **DWORD** che riceve l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="26a6a-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="26a6a-111">Il valore del campo 3 sarà contenuto nei bit da 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="26a6a-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="26a6a-112">Il valore del campo 2 sarà contenuto in bit da 8 a 15.</span><span class="sxs-lookup"><span data-stu-id="26a6a-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="26a6a-113">Il valore del campo 1 sarà contenuto nei bit da 16 a 23.</span><span class="sxs-lookup"><span data-stu-id="26a6a-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="26a6a-114">Il valore del campo 0 sarà contenuto nei bit da 24 a 31.</span><span class="sxs-lookup"><span data-stu-id="26a6a-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="26a6a-115">Per estrarre le informazioni sull'indirizzo, è inoltre possibile utilizzare le [**prime \_**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)macro IPAddress, [**Second \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**Third \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)e [**Fourth \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) .</span><span class="sxs-lookup"><span data-stu-id="26a6a-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="26a6a-116">Zero verrà restituito come indirizzo per tutti i campi vuoti.</span><span class="sxs-lookup"><span data-stu-id="26a6a-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26a6a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26a6a-117">Return value</span></span>

<span data-ttu-id="26a6a-118">Restituisce il numero di campi non vuoti.</span><span class="sxs-lookup"><span data-stu-id="26a6a-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a6a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26a6a-119">Requirements</span></span>



| <span data-ttu-id="26a6a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a6a-120">Requirement</span></span> | <span data-ttu-id="26a6a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="26a6a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26a6a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26a6a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26a6a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26a6a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26a6a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26a6a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26a6a-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26a6a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26a6a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26a6a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a6a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26a6a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





