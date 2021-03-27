---
description: Imposta i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.
title: Messaggio NCM_SETALLOWTYPE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753055"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="6069a-103">\_Messaggio NCM SETALLOWTYPE</span><span class="sxs-lookup"><span data-stu-id="6069a-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="6069a-104">Imposta i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="6069a-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="6069a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="6069a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6069a-106">*addrMask* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6069a-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="6069a-107">Specifica i tipi di indirizzo di rete come una o più <a href="net-string.md">**costanti \_ stringa net**</a> .</span><span class="sxs-lookup"><span data-stu-id="6069a-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="6069a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6069a-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6069a-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6069a-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6069a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6069a-110">Return value</span></span>

<span data-ttu-id="6069a-111">Restituisce \_ OK se l'esito è positivo o un valore di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6069a-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6069a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6069a-112">Remarks</span></span>

<span data-ttu-id="6069a-113">Il set di maschere è il criterio utilizzato per convalidare un indirizzo di rete nel messaggio [**NCM \_ GetAddress**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="6069a-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="6069a-114">Utilizzare questo messaggio solo per un controllo degli indirizzi di rete.</span><span class="sxs-lookup"><span data-stu-id="6069a-114">Use this message for a network address control only.</span></span> <span data-ttu-id="6069a-115">Per creare un'istanza di, usare la classe **msctls \_ Netaddress** definita in Shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="6069a-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="6069a-116">Chiamare [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) in fase di esecuzione prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6069a-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="6069a-117">Viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.</span><span class="sxs-lookup"><span data-stu-id="6069a-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6069a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6069a-118">Requirements</span></span>



| <span data-ttu-id="6069a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6069a-119">Requirement</span></span> | <span data-ttu-id="6069a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6069a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6069a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6069a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6069a-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6069a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6069a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6069a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6069a-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6069a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6069a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6069a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6069a-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6069a-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6069a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6069a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6069a-128">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="6069a-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="6069a-129">**\_SetAllowType NetAddr**</span><span class="sxs-lookup"><span data-stu-id="6069a-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




