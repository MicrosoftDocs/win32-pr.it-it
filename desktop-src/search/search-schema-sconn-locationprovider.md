---
description: L' <locationProvider> elemento facoltativo specifica il provider di ricerca che deve essere utilizzato dal connettore di ricerca del provider di servizi Web. Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306082"
---
# <a name="locationprovider-element-search-connector-schema"></a><span data-ttu-id="9a19f-104">Elemento locationProvider (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="9a19f-104">locationProvider Element (Search Connector Schema)</span></span>

<span data-ttu-id="9a19f-105">L' <locationProvider> elemento facoltativo specifica il provider di ricerca che deve essere utilizzato dal connettore di ricerca del provider di servizi Web.</span><span class="sxs-lookup"><span data-stu-id="9a19f-105">The optional <locationProvider> element specifies the search provider to be used by the web service provider search connector.</span></span> <span data-ttu-id="9a19f-106">Questo elemento contiene un attributo obbligatorio e un elemento figlio facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9a19f-106">This element contains one mandatory attribute and an optional child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a19f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a19f-107">Syntax</span></span>


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="9a19f-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="9a19f-108">Element Information</span></span>



| <span data-ttu-id="9a19f-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9a19f-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="9a19f-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="9a19f-110">Child Elements</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a19f-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="9a19f-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="9a19f-112">Elemento propertyBag (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="9a19f-112">propertyBag Element (Search Connector Schema)</span></span>](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a><span data-ttu-id="9a19f-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="9a19f-113">Attributes</span></span>



| <span data-ttu-id="9a19f-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="9a19f-114">Attribute</span></span> | <span data-ttu-id="9a19f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a19f-115">Description</span></span>                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | <span data-ttu-id="9a19f-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a19f-116">Required.</span></span> <span data-ttu-id="9a19f-117">Identificatore di classe (CLSID) del provider di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9a19f-117">The class identifier (CLSID) of the search provider.</span></span> |
| <span data-ttu-id="9a19f-118">codebase</span><span class="sxs-lookup"><span data-stu-id="9a19f-118">codebase</span></span>  | <span data-ttu-id="9a19f-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9a19f-119">Optional.</span></span>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="9a19f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a19f-120">Remarks</span></span>

<span data-ttu-id="9a19f-121">Il @clsid valore dell'attributo per il provider OpenSearch è {48E277F6-4e74-4cd6-BA6F-FA4F42898223}.</span><span class="sxs-lookup"><span data-stu-id="9a19f-121">The @clsid attribute value for the OpenSearch provider is {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.</span></span>

<span data-ttu-id="9a19f-122">I connettori di ricerca basati sul file System e sul gestore di protocollo possono usare [<simpleLocation>](search-schema-sconn-simplelocation.md) invece l'elemento.</span><span class="sxs-lookup"><span data-stu-id="9a19f-122">File system and protocol handler based search connectors can use the [<simpleLocation>](search-schema-sconn-simplelocation.md) element instead.</span></span> <span data-ttu-id="9a19f-123">Se <locationProvider> è presente, non deve essere presente alcun <simpleLocation> elemento nella descrizione del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9a19f-123">If <locationProvider> is present, there MUST NOT be a <simpleLocation> element in the Search Connector description.</span></span>

## <a name="example-of-a-locationprovider-element"></a><span data-ttu-id="9a19f-124">Esempio di elemento locationProvider</span><span class="sxs-lookup"><span data-stu-id="9a19f-124">Example of a locationProvider Element</span></span>


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



