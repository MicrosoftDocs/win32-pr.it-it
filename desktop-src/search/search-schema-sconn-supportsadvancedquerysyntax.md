---
description: L'elemento booleano <supportsAdvancedQuerySyntax> specifica se il provider di ricerca supporta la sintassi di query avanzata. Il valore predefinito è false. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306075"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>Elemento supportsAdvancedQuerySyntax (schema del connettore di ricerca)

L'elemento booleano <supportsAdvancedQuerySyntax> specifica se il provider di ricerca supporta la [sintassi di query avanzata](-search-3x-advancedquerysyntax.md). Il valore predefinito è false. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
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

Il valore `true` indica che il provider di ricerca supporta la sintassi di query avanzata inviata nelle query di ricerca.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



