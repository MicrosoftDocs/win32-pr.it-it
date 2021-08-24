---
description: Novità per Windows 7. Identifica una proprietà correlata alla proprietà definita nel file di descrizione della proprietà.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285c0f8b0731ba790cd57105f907cd4df85b6faa41c3f649588aca7ef457418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938681"
---
# <a name="relatedproperty"></a>relatedProperty

Novità per Windows 7. Identifica una proprietà correlata alla proprietà definita nel file di descrizione della proprietà. All'interno di un oggetto [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) possono essere presenti tutti gli elementi [relatedProperty]() necessari.

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
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo        | Descrizione                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Pubblica. Obbligatorio. Nome canonico della relazione di proprietà. |
| propertyName     | Pubblica. Obbligatorio. Nome canonico della proprietà correlata.      |



 

## <a name="remarks"></a>Commenti

Questo elemento consente di eseguire il mapping di una proprietà a un'altra. Ad esempio, è possibile eseguire il mapping del testo della proprietà personalizzata Fabrikam.StorageCapacity a System.Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
