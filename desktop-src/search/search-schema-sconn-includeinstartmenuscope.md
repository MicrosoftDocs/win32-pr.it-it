---
description: L'elemento booleano facoltativo <includeInStartMenuScope> specifica se questo connettore di ricerca deve essere incluso nell'ambito di ricerca del menu Start.
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Elemento includeInStartMenuScope (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306084"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="df3db-103">Elemento includeInStartMenuScope (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="df3db-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="df3db-104">L'elemento booleano facoltativo <includeInStartMenuScope> specifica se questo connettore di ricerca deve essere incluso nell'ambito di ricerca del menu Start.</span><span class="sxs-lookup"><span data-stu-id="df3db-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="df3db-105">Il valore predefinito è true per i connettori di ricerca che usano il file system come origine dati e false per i connettori di ricerca usati dai gestori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="df3db-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="df3db-106">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="df3db-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df3db-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="df3db-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="df3db-108">Element Information</span></span>



| <span data-ttu-id="df3db-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="df3db-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="df3db-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="df3db-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="df3db-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="df3db-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="df3db-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="df3db-112">Remarks</span></span>

<span data-ttu-id="df3db-113">Se si include il connettore di ricerca nell'ambito del menu Start, gli utenti possono cercare il percorso dalla casella di ricerca nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="df3db-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="df3db-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="df3db-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



