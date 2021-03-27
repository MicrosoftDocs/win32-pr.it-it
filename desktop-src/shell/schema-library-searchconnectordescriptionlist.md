---
description: Questo <searchConnectorDescriptionList> elemento contiene un elenco di connettori di ricerca che eseguono il mapping alle posizioni incluse nella libreria. Ogni connettore di ricerca viene definito da un <searchConnectorDescription> elemento. Questo elemento è facoltativo e non ha attributi.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Elemento searchConnectorDescriptionList (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980463"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="4c58c-105">Elemento searchConnectorDescriptionList (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="4c58c-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="4c58c-106">Questo <searchConnectorDescriptionList> elemento contiene un elenco di connettori di ricerca che eseguono il mapping alle posizioni incluse nella libreria.</span><span class="sxs-lookup"><span data-stu-id="4c58c-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="4c58c-107">Ogni connettore di ricerca viene definito da un <searchConnectorDescription> elemento.</span><span class="sxs-lookup"><span data-stu-id="4c58c-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="4c58c-108">Questo elemento è facoltativo e non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="4c58c-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c58c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c58c-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="4c58c-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4c58c-110">Element Information</span></span>



| <span data-ttu-id="4c58c-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4c58c-111">Parent Element</span></span>                                                               | <span data-ttu-id="4c58c-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4c58c-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c58c-113">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="4c58c-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="4c58c-114">Elemento searchConnectorDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="4c58c-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="4c58c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c58c-115">Remarks</span></span>

<span data-ttu-id="4c58c-116">Non è possibile includere in una libreria i connettori di ricerca per gli ambiti di ricerca federata e di gestori di protocollo di Windows.</span><span class="sxs-lookup"><span data-stu-id="4c58c-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c58c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c58c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c58c-118">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="4c58c-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="4c58c-119">[Cerca nello schema di descrizione del connettore](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4c58c-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
