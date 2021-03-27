---
description: Recupera i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.
title: Messaggio NCM_GETALLOWTYPE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049601"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="f1d7a-103">\_Messaggio NCM GETALLOWTYPE</span><span class="sxs-lookup"><span data-stu-id="f1d7a-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="f1d7a-104">Recupera i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="f1d7a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1d7a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1d7a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1d7a-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f1d7a-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f1d7a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1d7a-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f1d7a-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1d7a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1d7a-110">Return value</span></span>

<span data-ttu-id="f1d7a-111">Restituisce i tipi di indirizzi di rete consentiti come una o più costanti [**\_ stringa di rete**](net-string.md) .</span><span class="sxs-lookup"><span data-stu-id="f1d7a-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1d7a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1d7a-112">Remarks</span></span>

<span data-ttu-id="f1d7a-113">La maschera restituita è il criterio usato per convalidare un indirizzo di rete nel messaggio [**NCM \_ GetAddress**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="f1d7a-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="f1d7a-114">Utilizzare questo messaggio solo per un controllo degli indirizzi di rete.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-114">Use this message for a network address control only.</span></span> <span data-ttu-id="f1d7a-115">Per creare un'istanza di, usare la classe **msctls \_ Netaddress** definita in Shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="f1d7a-116">Chiamare [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) in fase di esecuzione prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="f1d7a-117">Viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.</span><span class="sxs-lookup"><span data-stu-id="f1d7a-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d7a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1d7a-118">Requirements</span></span>



| <span data-ttu-id="f1d7a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1d7a-119">Requirement</span></span> | <span data-ttu-id="f1d7a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f1d7a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d7a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1d7a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d7a-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1d7a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1d7a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1d7a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d7a-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1d7a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1d7a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1d7a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1d7a-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1d7a-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d7a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1d7a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d7a-128">**NCM \_ SETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="f1d7a-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="f1d7a-129">**\_GetAllowType NetAddr**</span><span class="sxs-lookup"><span data-stu-id="f1d7a-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




