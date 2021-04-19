---
description: Indica se connettersi a una rete nascosta.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Elemento nonbroadcast (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308882"
---
# <a name="nonbroadcast-ssidconfig-element"></a>Elemento nonbroadcast (SSIDConfig)

L'elemento nonbroadcast (SSIDConfig) indica se connettersi a una rete nascosta. Se una rete non trasmette il proprio SSID, è nota come rete nascosta. Se all'interno del profilo sono impostati più SSID, è necessario che tutti abbiano lo stesso valore non broadcast.

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su **ESS**, questo valore può essere "true" o "false". Se questo elemento non è presente, il valore predefinito è "false".

Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su **IBSS**, questo valore deve essere "false". Se questo elemento non è presente, il valore predefinito è "false".

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

L'elemento è definito dall'elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="examples"></a>Esempio

Per visualizzare un profilo di esempio che usa l'elemento non **broadcast** , vedere [esempio di profilo non broadcast](non-broadcast-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




