---
description: Contiene l'SSID di un'interfaccia.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Struttura DOT11_SSID (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882677"
---
# <a name="dot11_ssid-structure"></a>\_Struttura SSID DOT11

Una **struttura \_ SSID DOT11** contiene il valore SSID di un'interfaccia.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>Members

<dl> <dt>

**uSSIDLength**
</dt> <dd>

Lunghezza, in byte, della matrice **ucSSID** .

</dd> <dt>

**ucSSID**
</dt> <dd>

SSID. \_ \_ La lunghezza massima SSID DOT11 \_ è impostata su 32.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'SSID specificato dal membro **ucSSID** non è una stringa ASCII con terminazione null. La lunghezza del SSID è determinata dal membro **uSSIDLength** .

Un SSID con caratteri jolly è un SSID il cui membro **uSSIDLength** è impostato su zero. Quando l'SSID desiderato è impostato sull'SSID con caratteri jolly, la stazione 802,11 può connettersi a qualsiasi rete di Service Set (BSS) di base.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_parametri di connessione WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




