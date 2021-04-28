---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento image (schema di descrizione proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104989"
---
# <a name="image"></a>image

Deve essere presente un solo [elemento image]() per ogni elemento padre.

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
| [enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione       |
|-----------|-------------------|
| res       | Pubblica. Obbligatorio. |



 

 

 
