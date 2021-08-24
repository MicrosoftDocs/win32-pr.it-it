---
description: Definisce un tipo di rete BSS (Basic Service Set).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: DOT11_BSS_TYPE enumerazione (Wlantypes.h)
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
ms.openlocfilehash: 2d1c83ced842dbb876fea89271a160df2ca07fb9f02f415b13f8f1a46bc8dc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780321"
---
# <a name="dot11_bss_type-enumeration"></a>Enumerazione DOT11 \_ BSS \_ TYPE

Il **tipo enumerato DOT11 \_ BSS \_ TYPE** definisce un tipo di rete BSS (Basic Service Set).

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

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**Infrastruttura di tipo \_ BSS dot11 \_ \_**
</dt> <dd>

Specifica una rete BSS dell'infrastruttura.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**Indipendente dal tipo \_ BSS dot11 \_ \_**
</dt> <dd>

Specifica una rete BSS (IBSS) indipendente.

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11 \_ BSS \_ type \_ any**
</dt> <dd>

Specifica l'infrastruttura o la rete IBSS.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes.h (includere Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VOCE \_ WLAN BSS \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**PARAMETRI DI CONNESSIONE \_ \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




