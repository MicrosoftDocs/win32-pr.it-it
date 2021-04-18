---
description: L'elemento booleano facoltativo <isDefaultNonOwnerSaveLocation> specifica se il percorso descritto nel connettore di ricerca deve essere utilizzato come percorso di salvataggio predefinito quando un utente di un altro computer in un gruppo Home sceglie di salvare un elemento.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306083"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Elemento isDefaultNonOwnerSaveLocation (schema del connettore di ricerca)

L'elemento booleano facoltativo <isDefaultNonOwnerSaveLocation> specifica se il percorso descritto nel connettore di ricerca deve essere utilizzato come percorso di salvataggio predefinito quando un utente di un altro computer in un gruppo Home sceglie di salvare un elemento. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Se true, quando un utente di un altro computer in un gruppo Home sceglie di salvare un elemento, Esplora risorse Salva l'elemento nel percorso specificato nell' <simpleLocation> elemento.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



