---
description: L'elemento &lt; booleano facoltativo includeInStartMenuScope specifica se questo connettore di ricerca deve essere incluso nell'ambito menu Start &gt; di ricerca.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20696dc6d2bc41b3f693e771a59541204e376e7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882393"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a>Elemento includeInStartMenuScope (schema del connettore di ricerca)

L'elemento &lt; booleano facoltativo includeInStartMenuScope specifica se questo connettore di ricerca deve essere incluso nell'ambito menu Start &gt; di ricerca. Il valore predefinito è true per i connettori di ricerca che usano il file system come origine dati e false per i connettori di ricerca usati dai gestori delle proprietà. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Commenti

Se si include il connettore di ricerca nell'ambito menu Start, gli utenti possono cercare la posizione dalla casella di ricerca nella menu Start.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



