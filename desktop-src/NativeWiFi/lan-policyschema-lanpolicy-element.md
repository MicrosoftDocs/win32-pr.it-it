---
description: Contiene criteri LAN cablati.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 468e9fb0500c4a514b7b0a9dddea023f0851b9f7ba783504548f2285810ffffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780181"
---
# <a name="lanpolicy-element"></a>Elemento LANPolicy

L'elemento LANPolicy contiene criteri LAN cablati. Questo elemento è l'elemento radice univoco per un profilo di criteri di rete cablata.

Lo spazio dei nomi di destinazione per **l'elemento LANPolicy** è `https://www.microsoft.com/networking/LAN/policy/v1` .

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
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
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
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



| Elemento                                                                           | Tipo                                                     | Descrizione                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**description**](lan-policyschema-description-lanpolicy-element.md)             | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene la descrizione di un criterio lan cablato. <br/>                                                                                                                          |
| [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) | boolean                                                  | Specifica se i computer usano il servizio di configurazione automatica incorporato per gestire le connessioni alle reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1X.<br/> |
| [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | Contiene le impostazioni globali per la configurazione automatica delle reti cablate. <br/>                                                                                          |
| [**Nome**](lan-policyschema-name-lanpolicy-element.md)                           | [**nameType**](lan-policyschema-nametype-simpletype.md) | Contiene il nome di un criterio LAN cablato. <br/>                                                                                                                                 |
| [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | Contiene un elenco di profili da applicare a livello di dominio o di computer. <br/>                                                                                                |



## <a name="remarks"></a>Commenti

Per visualizzare l'elenco degli elementi figlio in una struttura ad albero, vedere Elementi dello schema dei [ \_ criteri LAN](lan-policyschema-elements.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




