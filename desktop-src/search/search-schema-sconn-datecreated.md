---
description: L'elemento dateCreated facoltativo identifica la data e l'ora di creazione del connettore di &lt; ricerca usando lo standard &gt; ISO 8601. Non ha elementi figlio e nessun attributo.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff7c739bcad9e3a6594008597c0392398f22864
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882510"
---
# <a name="datecreated-element-search-connector-schema"></a>Elemento dateCreated (schema del connettore di ricerca)

L'elemento dateCreated facoltativo identifica la data e l'ora di creazione del connettore di &lt; ricerca usando lo standard &gt; ISO 8601. Non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
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

Il formato del valore di questo elemento segue lo standard ISO 8601. Un uso comune è uno dei seguenti:

-   \[AAAA \] - \[ MM \] - \[ GG \] T \[ \] hh: mm : \[ \] \[ ss ± \] \[ hh \] : mm \[ \] ("1981-04-05T14:30:30-05:00")
-   \[AAAA \] \[ MM \] \[ GG \] T \[ hh mm \] \[ \] \[ ss \] Z ("19810405T193030Z")

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



