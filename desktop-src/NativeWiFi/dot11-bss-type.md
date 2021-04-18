---
description: Definisce un tipo di rete del set di servizi di base (BSS).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Enumerazione DOT11_BSS_TYPE (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313766"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="6c344-103">\_Enumerazione del \_ tipo BSS DOT11</span><span class="sxs-lookup"><span data-stu-id="6c344-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="6c344-104">Il tipo enumerato di **\_ \_ tipo BSS DOT11** definisce un tipo di rete del set di servizi di base (BSS).</span><span class="sxs-lookup"><span data-stu-id="6c344-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c344-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c344-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6c344-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="6c344-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6c344-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infrastruttura di \_ tipi \_ BSS dot11**</span><span class="sxs-lookup"><span data-stu-id="6c344-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="6c344-108">Specifica una rete BSS dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="6c344-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="6c344-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11 \_ di \_ tipo BSS \_ indipendente**</span><span class="sxs-lookup"><span data-stu-id="6c344-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="6c344-110">Specifica una rete BSS (IBSS) indipendente.</span><span class="sxs-lookup"><span data-stu-id="6c344-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="6c344-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11 \_ di \_ tipo BSS \_ any**</span><span class="sxs-lookup"><span data-stu-id="6c344-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="6c344-112">Specifica l'infrastruttura o la rete IBSS.</span><span class="sxs-lookup"><span data-stu-id="6c344-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c344-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c344-113">Requirements</span></span>



| <span data-ttu-id="6c344-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c344-114">Requirement</span></span> | <span data-ttu-id="6c344-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6c344-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c344-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c344-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c344-117">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="6c344-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6c344-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c344-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c344-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c344-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="6c344-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6c344-120">Redistributable</span></span><br/>          | <span data-ttu-id="6c344-121">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="6c344-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="6c344-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c344-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c344-123"><dt>Wlantypes. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c344-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c344-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c344-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c344-125">**\_voce BSS \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="6c344-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="6c344-126">**\_parametri di connessione WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6c344-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="6c344-127">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="6c344-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




