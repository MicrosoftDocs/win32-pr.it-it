---
description: Elemento radice che identifica un profilo Mobile Broadband.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Elemento MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 049ec22c170afda3a46620e2e94e2a16ae2708b4d6a69fcd0262baa69352a0a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943361"
---
# <a name="mbnprofile-element"></a>Elemento MBNProfile

**L'elemento MBNProfile** è l'elemento radice che identifica un profilo Mobile Broadband.

Può essere presente un solo elemento di questo tipo per documento.

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                          | Tipo                                                           | Descrizione                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [**AutoConnectOnInternet**](schema-autoconnectoninternet-mbnprofile-element.md) | boolean                                                        | Indica se il dispositivo si connetterà automaticamente.<br/> |
| [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md)               |                                                                | Impostazioni di connessione automatica del dispositivo.<br/>           |
| [**Context**](schema-context-mbnprofile-element.md)                             | [**Contexttype**](schema-contexttype-complextype.md)          | Parametri di configurazione della connessione dati.<br/>              |
| [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | Provider di rete preferiti per il roaming.<br/>       |
| [**Descrizione**](schema-description-mbnprofile-element.md)                     | [**nameType**](schema-nametype-simpletype.md)                 | Descrizione del profilo.<br/>                    |
| [**HomeProviderName**](schema-homeprovidername-mbnprofile-element.md)           | [**providerNameType**](schema-providernametype-simpletype.md) | Nome del provider home.<br/>                     |
| [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md)                   | [**iconFileType**](schema-iconfiletype-simpletype.md)         | Percorso del file dell'icona.<br/>                         |
| [**IsDefault**](schema-isdefault-mbnprofile-element.md)                         | boolean                                                        | Indica se il profilo è quello predefinito.<br/>            |
| [**Nome**](schema-name-mbnprofile-element.md)                                   | [**nameType**](schema-nametype-simpletype.md)                 | Nome del profilo.<br/>                           |
| [**ProfileCreationType**](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | Informazioni sull'autore del profilo.<br/>         |
| [**SimIccID**](schema-simiccid-mbnprofile-element.md)                           | [**simIccIDType**](schema-simiccidtype-simpletype.md)         | Numero di identificazione SIM per i dispositivi GSM.<br/>     |
| [**SubscriberID**](schema-subscriberid-mbnprofile-element.md)                   | [**subscriberIdType**](schema-subscriberidtype-simpletype.md) | Identificatore univoco del profilo.<br/>              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



 

 




