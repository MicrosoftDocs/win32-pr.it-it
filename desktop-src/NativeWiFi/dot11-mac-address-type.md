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
# <a name="dot11_mac_address"></a>\_Indirizzo Mac \_ DOT11

I tipi di **\_ \_ indirizzi Mac DOT11** vengono usati per definire un indirizzo IEEE Media Access Control (Mac).


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**\_Indirizzo Mac \_ DOT11 \[ 6\]**
</dt> <dd>

Indirizzo MAC in formato unicast, multicast o broadcast.

</dd> <dt>

**\_Indirizzo Mac \_ PDOT11**
</dt> <dd>

Puntatore a un indirizzo MAC in formato unicast, multicast o broadcast.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                       |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Windot11. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Elenco BSSID \_ DOT11**](dot11-bssid-list.md)
</dt> <dt>

[**\_attributi di associazione WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_voce BSS \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




