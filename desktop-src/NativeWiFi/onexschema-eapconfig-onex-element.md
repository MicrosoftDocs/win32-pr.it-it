---
description: specifica la configurazione EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 539f30d6730ec0735006f9dd3812322468ce71c7b0fbd90610b6cd589e0d60bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684881"
---
# <a name="eapconfig-onex-element"></a>Elemento EAPConfig (OneX)

**L'elemento EAPConfig** (OneX) specifica la configurazione EAPHost.

A differenza della maggior parte degli elementi nello schema del profilo 802.1X, questo elemento si trova nello spazio dei `https://www.microsoft.com/provisioning/EapHostConfig` nomi . I relativi elementi figlio sono definiti nello [schema eaphostconfig](../eaphost/eaphostconfigschema-schema.md). [**L'elemento EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) è un elemento figlio dell'elemento **EAPConfig.**

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**L'elemento EAPConfig** è definito dall'elemento [**OneX.**](onexschema-onex-element.md)

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

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
