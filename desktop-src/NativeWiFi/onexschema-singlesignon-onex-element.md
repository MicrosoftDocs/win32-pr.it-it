---
description: Specifica le informazioni di configurazione di rete single sign-on (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Elemento singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5d0e002133366527624a0954df9054272cc08d894ba8dc3121b8a86b807caab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798032"
---
# <a name="singlesignon-onex-element"></a>Elemento singleSignOn (OneX)

L'elemento singleSignOn (OneX) specifica le informazioni di configurazione di rete single sign-on (SSO).

Questo elemento è facoltativo. Non usare l'elemento singleSignOn in un profilo se la rete non lo richiede.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**L'elemento singleSignOn** è definito dall'elemento [**OneX.**](onexschema-onex-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo    | Descrizione                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-On non riesca.<br/>                                                                                                                      |
| [**digitare**](onexschema-type-singlesignon-element.md)                               |         | Specifica quando viene eseguito l'accesso Single Sign-On. Se impostato su `preLogon` , l'accesso Single Sign-On viene eseguito prima dell'accesso dell'utente. Se impostato su `postLogon` , l'accesso Single Sign-On viene eseguito immediatamente dopo l'accesso dell'utente.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Specifica se la LAN virtuale (VLAN) usata dal dispositivo cambia in base alle credenziali dell'utente.<br/>                                                                                                                   |



## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando usando il **comando netsh wlan set profileparameter.** Per altre informazioni, vedere [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
