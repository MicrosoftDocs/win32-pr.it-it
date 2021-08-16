---
description: Contiene il nome di un profilo LAN wireless.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Elemento name (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6a6d19c043f7cc2e42ca8221e98b05e4afe7628b143bd572465f00e1d3652275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984114"
---
# <a name="name-wlanprofile-element"></a>Elemento name (WLANProfile)

L'elemento name (WLANProfile) contiene il nome di un profilo LAN wireless.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

**L'elemento** name è definito dall'elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="remarks"></a>Commenti

Per i nomi viene fatto distinzione tra maiuscole e minuscole.

Per Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2), l'elemento name viene ignorato quando il profilo viene salvato nell'archivio profili. Il nome del profilo deriva dall'SSID della rete. Per i profili di rete dell'infrastruttura, il nome del profilo è l'SSID della rete. Per i profili di rete ad hoc, il nome del profilo è l'SSID della rete ad hoc seguito da `-adhoc` . I caratteri di escape XML, ad &, non vengono visualizzati. Evitare di usare caratteri di escape XML nei nomi SSID per i profili distribuiti in Windows XP con SP3 o nell'API LAN wireless per Windows XP con SP2.

Per qualsiasi profilo di rete destinato all'uso solo in Windows Vista o Windows Server 2008, il nome può essere qualsiasi stringa.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano **l'elemento name,** vedere [Wireless Profile Samples](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




