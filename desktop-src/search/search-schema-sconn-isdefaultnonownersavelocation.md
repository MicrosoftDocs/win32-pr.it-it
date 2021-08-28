---
description: L'elemento booleano facoltativo &lt; isDefaultNonOwnerSaveLocation specifica se il percorso descritto nel connettore di ricerca deve essere usato come percorso di salvataggio predefinito quando un utente di un altro computer in un gruppo Home sceglie di salvare un &gt; elemento.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Elemento isDefaultNonOwnerSaveLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2a20912b10864d856bd4513e31a37eeee5c2a0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881933"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>Elemento isDefaultNonOwnerSaveLocation (schema del connettore di ricerca)

L'elemento booleano facoltativo &lt; isDefaultNonOwnerSaveLocation specifica se il percorso descritto nel connettore di ricerca deve essere usato come percorso di salvataggio predefinito quando un utente di un altro computer in un gruppo Home sceglie di salvare un &gt; elemento. Questo elemento non ha elementi figlio e nessun attributo.

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

Se true, quando un utente di un altro computer in un gruppo Home sceglie di salvare un elemento, Windows Explorer salva l'elemento nel percorso specificato &lt; nell'elemento &gt; simpleLocation.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



