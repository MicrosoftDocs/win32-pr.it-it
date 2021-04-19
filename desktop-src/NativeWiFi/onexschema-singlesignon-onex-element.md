---
description: Specifica le informazioni di configurazione di rete Single Sign-On (SSO).
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
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311666"
---
# <a name="singlesignon-onex-element"></a>Elemento singleSignOn (OneX)

L'elemento singleSignOn (OneX) specifica le informazioni di configurazione di rete Single Sign-On (SSO).

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

L'elemento **singleSignOn** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo    | Descrizione                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione del Single Sign-On abbia esito negativo.<br/>                                                                                                                      |
| [**tipo**](onexschema-type-singlesignon-element.md)                               |         | Specifica quando Single Sign-On viene eseguito. Se impostata su `preLogon` , Single Sign-on viene eseguita prima dell'accesso dell'utente. Quando è impostata su `postLogon` , Single Sign-on viene eseguita immediatamente dopo l'accesso dell'utente.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | boolean | Specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.<br/>                                                                                                                   |



## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** . Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 
