---
title: Enumerazione CB_ADDRESS_TYPE (Cbclient. h)
description: Specifica il tipo di indirizzo.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- Enumerazione CB_ADDRESS_TYPE Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740586"
---
# <a name="cb_address_type-enumeration"></a><span data-ttu-id="f1671-104">Enumerazione del tipo di \_ Indirizzo CB \_</span><span class="sxs-lookup"><span data-stu-id="f1671-104">CB\_ADDRESS\_TYPE enumeration</span></span>

<span data-ttu-id="f1671-105">Specifica il tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f1671-105">Specifies the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1671-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1671-106">Syntax</span></span>


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f1671-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="f1671-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f1671-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**Indirizzo CB non \_ \_ definito**</span><span class="sxs-lookup"><span data-stu-id="f1671-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB\_ADDR\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="f1671-109">Il tipo di indirizzo non è definito.</span><span class="sxs-lookup"><span data-stu-id="f1671-109">The address type is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="f1671-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**\_IPv4 indirizzi \_ CB**</span><span class="sxs-lookup"><span data-stu-id="f1671-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB\_ADDR\_IPv4**</span></span>
</dt> <dd>

<span data-ttu-id="f1671-111">L'indirizzo è un indirizzo IPv4.</span><span class="sxs-lookup"><span data-stu-id="f1671-111">The address is an IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="f1671-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**\_IPv6 indirizzo \_ CB**</span><span class="sxs-lookup"><span data-stu-id="f1671-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB\_ADDR\_IPv6**</span></span>
</dt> <dd>

<span data-ttu-id="f1671-113">L'indirizzo è un indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="f1671-113">The address is an IPv6 address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1671-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1671-114">Requirements</span></span>



| <span data-ttu-id="f1671-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1671-115">Requirement</span></span> | <span data-ttu-id="f1671-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f1671-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1671-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1671-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1671-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f1671-118">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="f1671-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1671-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1671-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1671-120">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="f1671-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1671-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1671-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1671-122"><dt>Cbclient.h</dt></span></span> </dl> |



 

 





