---
description: L' <domain> elemento facoltativo specifica l'URL del servizio di ricerca utilizzato da questo connettore di ricerca. Viene visualizzata nel riquadro dei dettagli. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento Domain (Schema connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878790"
---
# <a name="domain-element-search-connector-schema"></a>Elemento Domain (Schema connettore di ricerca)

L' <domain> elemento facoltativo specifica l'URL del servizio di ricerca utilizzato da questo connettore di ricerca. Viene visualizzata nel riquadro dei dettagli. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

L'URL deve essere il dominio di primo livello per il provider di ricerca. Ad esempio: https://www.example.com.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



