---
description: Consentono di definire un indirizzo IEEE Media Access Control (MAC).
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882685"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="a102f-103">\_Indirizzo Mac \_ DOT11</span><span class="sxs-lookup"><span data-stu-id="a102f-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="a102f-104">I tipi di **\_ \_ indirizzi Mac DOT11** vengono usati per definire un indirizzo IEEE Media Access Control (Mac).</span><span class="sxs-lookup"><span data-stu-id="a102f-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="a102f-105">**\_Indirizzo Mac \_ DOT11 \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="a102f-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="a102f-106">Indirizzo MAC in formato unicast, multicast o broadcast.</span><span class="sxs-lookup"><span data-stu-id="a102f-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="a102f-107">**\_Indirizzo Mac \_ PDOT11**</span><span class="sxs-lookup"><span data-stu-id="a102f-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="a102f-108">Puntatore a un indirizzo MAC in formato unicast, multicast o broadcast.</span><span class="sxs-lookup"><span data-stu-id="a102f-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a102f-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a102f-109">Requirements</span></span>



| <span data-ttu-id="a102f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a102f-110">Requirement</span></span> | <span data-ttu-id="a102f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="a102f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a102f-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a102f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a102f-113">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a102f-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a102f-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a102f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a102f-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a102f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a102f-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a102f-116">Redistributable</span></span><br/>          | <span data-ttu-id="a102f-117">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="a102f-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="a102f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a102f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a102f-119"><dt>Windot11. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a102f-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a102f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a102f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a102f-121">**\_Elenco BSSID \_ DOT11**</span><span class="sxs-lookup"><span data-stu-id="a102f-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="a102f-122">**\_attributi di associazione WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="a102f-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="a102f-123">**\_voce BSS \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="a102f-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




