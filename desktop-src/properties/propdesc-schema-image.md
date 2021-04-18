---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento Image (schema della descrizione della proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310122"
---
# <a name="image"></a>image

Deve essere presente un solo elemento [Image]() per ogni elemento padre.

## <a name="syntax"></a>Sintassi


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elementi padre                                                                  | Elementi figlio |
|----------------------------------------------------------------------------------|----------------|
| [enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md) | nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione       |
|-----------|-------------------|
| res       | Pubblica. Obbligatorio. |



 

 

 
