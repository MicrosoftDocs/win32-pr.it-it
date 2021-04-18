---
description: Indica se una chiave condivisa è crittografata.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Elemento Protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306484"
---
# <a name="protected-sharedkey-element"></a>Elemento Protected (sharedKey)

L'elemento Protected (sharedKey) indica se una chiave condivisa è crittografata.

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

L'elemento è definito dall'elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Commenti

Per Windows Vista e Windows Server 2008, **protected** always ha il valore true se il profilo è stato recuperato dall'archivio profili, ad esempio chiamando [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

Per i profili destinati all'uso in Windows XP con Service Pack 3 (SP3) o l'API LAN wireless per Windows XP con Service Pack 2 (SP2), il valore **protetto** deve essere false.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **protetto** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sharedKey (sicurezza)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




