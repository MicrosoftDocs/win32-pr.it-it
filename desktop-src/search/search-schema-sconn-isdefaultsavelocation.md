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
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="e8743-104">Elemento isDefaultSaveLocation (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="e8743-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="e8743-105">L'elemento booleano facoltativo <isDefaultSaveLocation> specifica se la posizione descritta nel connettore di ricerca deve essere utilizzata come percorso di salvataggio predefinito.</span><span class="sxs-lookup"><span data-stu-id="e8743-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="e8743-106">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="e8743-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8743-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8743-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="e8743-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="e8743-108">Element Information</span></span>



| <span data-ttu-id="e8743-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e8743-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e8743-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e8743-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="e8743-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="e8743-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="e8743-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8743-112">Remarks</span></span>

<span data-ttu-id="e8743-113">Quando un utente sceglie di salvare un elemento, Esplora risorse Salva l'elemento nel percorso specificato nell' <simpleLocation> elemento.</span><span class="sxs-lookup"><span data-stu-id="e8743-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="e8743-114">Gli utenti possono modificare questa impostazione usando la finestra di dialogo delle proprietà per il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e8743-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="e8743-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8743-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



