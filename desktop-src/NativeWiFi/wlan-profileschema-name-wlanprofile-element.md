---
description: Contiene il nome di un profilo LAN wireless.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Elemento Name (WLANProfile)
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
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527787"
---
# <a name="name-wlanprofile-element"></a>Elemento Name (WLANProfile)

L'elemento Name (WLANProfile) contiene il nome di un profilo LAN wireless.

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

L'elemento **Name** viene definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Commenti

I nomi fanno distinzione tra maiuscole e minuscole.

Per Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2), l'elemento Name viene ignorato quando il profilo viene salvato nell'archivio profili. Il nome del profilo deriva dall'SSID della rete. Per i profili di rete dell'infrastruttura, il nome del profilo è il SSID della rete. Per i profili di rete ad hoc, il nome del profilo è il SSID della rete ad hoc seguita da `-adhoc` . I caratteri di escape XML, ad esempio &, non vengono visualizzati. Evitare di utilizzare caratteri di escape XML nei nomi SSID per i profili distribuiti in Windows XP con SP3 o l'API LAN wireless per Windows XP con SP2.

Per qualsiasi profilo di rete destinato a essere utilizzato solo in Windows Vista o Windows Server 2008, il nome può essere qualsiasi stringa.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **Name** , vedere esempi di profili [wireless](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




