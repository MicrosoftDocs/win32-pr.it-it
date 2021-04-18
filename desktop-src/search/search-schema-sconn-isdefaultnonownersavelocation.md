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
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="b95eb-103">Elemento isDefaultNonOwnerSaveLocation (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="b95eb-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="b95eb-104">L'elemento booleano facoltativo <isDefaultNonOwnerSaveLocation> specifica se il percorso descritto nel connettore di ricerca deve essere utilizzato come percorso di salvataggio predefinito quando un utente di un altro computer in un gruppo Home sceglie di salvare un elemento.</span><span class="sxs-lookup"><span data-stu-id="b95eb-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="b95eb-105">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="b95eb-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95eb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b95eb-106">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="b95eb-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b95eb-107">Element Information</span></span>



| <span data-ttu-id="b95eb-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="b95eb-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="b95eb-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b95eb-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="b95eb-110">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="b95eb-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="b95eb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b95eb-111">Remarks</span></span>

<span data-ttu-id="b95eb-112">Se true, quando un utente di un altro computer in un gruppo Home sceglie di salvare un elemento, Esplora risorse Salva l'elemento nel percorso specificato nell' <simpleLocation> elemento.</span><span class="sxs-lookup"><span data-stu-id="b95eb-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="b95eb-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="b95eb-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



