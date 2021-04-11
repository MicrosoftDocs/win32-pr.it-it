---
description: Specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Authentication (authEncryption)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226489"
---
# <a name="authentication-authencryption-element"></a>Authentication (authEncryption)-elemento

L'elemento Authentication (authEncryption) specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Commenti

Nella tabella seguente vengono descritti i valori di enumerazione.



| Valore   | Descrizione                            |
|---------|----------------------------------------|
| apre    | Aprire l'autenticazione 802,11.            |
| shared  | Autenticazione 802,11 condivisa.          |
| WPA     | Autenticazione WPA-Enterprise 802,11.  |
| WPAPSK  | Autenticazione WPA-Personal 802,11.    |
| WPA2    | Autenticazione WPA2-Enterprise 802,11. |
| WPA2PSK | Autenticazione WPA2-Personal 802,11.   |



 

Per ulteriori informazioni sui metodi di autenticazione 802,11, vedere le specifiche [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **Authentication** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**authEncryption (sicurezza)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




