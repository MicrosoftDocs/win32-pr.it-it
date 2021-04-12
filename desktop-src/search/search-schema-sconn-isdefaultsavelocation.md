---
description: L'elemento booleano facoltativo <isDefaultSaveLocation> specifica se la posizione descritta nel connettore di ricerca deve essere utilizzata come percorso di salvataggio predefinito. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Elemento isDefaultSaveLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342911"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>Elemento isDefaultSaveLocation (schema del connettore di ricerca)

L'elemento booleano facoltativo <isDefaultSaveLocation> specifica se la posizione descritta nel connettore di ricerca deve essere utilizzata come percorso di salvataggio predefinito. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

Quando un utente sceglie di salvare un elemento, Esplora risorse Salva l'elemento nel percorso specificato nell' <simpleLocation> elemento. Gli utenti possono modificare questa impostazione usando la finestra di dialogo delle proprietà per il connettore di ricerca.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



