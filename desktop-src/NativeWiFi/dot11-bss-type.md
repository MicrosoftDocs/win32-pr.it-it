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
# <a name="dot11_bss_type-enumeration"></a>\_Enumerazione del \_ tipo BSS DOT11

Il tipo enumerato di **\_ \_ tipo BSS DOT11** definisce un tipo di rete del set di servizi di base (BSS).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infrastruttura di \_ tipi \_ BSS dot11**
</dt> <dd>

Specifica una rete BSS dell'infrastruttura.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11 \_ di \_ tipo BSS \_ indipendente**
</dt> <dd>

Specifica una rete BSS (IBSS) indipendente.

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11 \_ di \_ tipo BSS \_ any**
</dt> <dd>

Specifica l'infrastruttura o la rete IBSS.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_voce BSS \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**\_parametri di connessione WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




