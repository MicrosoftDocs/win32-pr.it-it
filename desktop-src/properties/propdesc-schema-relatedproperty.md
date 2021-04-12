---
description: Novità di Windows 7. Identifica una proprietà correlata alla proprietà definita nel file di descrizione della proprietà.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344801"
---
# <a name="relatedproperty"></a>relatedProperty

Novità di Windows 7. Identifica una proprietà correlata alla proprietà definita nel file di descrizione della proprietà. È possibile che siano presenti tutti gli elementi [relatedProperty]() all'interno di un [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) in base alle esigenze.

## <a name="syntax"></a>Sintassi


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio |
|------------------------------------------------------------------|----------------|
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo        | Descrizione                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Pubblica. Obbligatorio. Nome canonico della relazione di proprietà. |
| propertyName     | Pubblica. Obbligatorio. Nome canonico della proprietà correlata.      |



 

## <a name="remarks"></a>Commenti

Questo elemento consente di eseguire il mapping di una proprietà a un'altra. Ad esempio, è possibile eseguire il mapping del testo della proprietà personalizzata fabrikam. StorageCapacity a System. Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
