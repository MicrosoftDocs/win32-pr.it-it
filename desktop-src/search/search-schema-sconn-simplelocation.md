---
description: L' <simpleLocation> elemento specifica il percorso per i connettori di ricerca che sono basati sul file System o sul gestore del protocollo. Questo elemento ha due elementi figlio e nessun attributo.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Elemento simpleLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342901"
---
# <a name="simplelocation-element-search-connector-schema"></a><span data-ttu-id="b90de-104">Elemento simpleLocation (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="b90de-104">simpleLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="b90de-105">L' <simpleLocation> elemento specifica il percorso per i connettori di ricerca che sono basati sul file System o sul gestore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="b90de-105">The <simpleLocation> element specifies the location for search connectors that are file-system based or protocol-handler based.</span></span> <span data-ttu-id="b90de-106">Questo elemento ha due elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="b90de-106">This element has two child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90de-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b90de-107">Syntax</span></span>


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="b90de-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b90de-108">Element Information</span></span>



| <span data-ttu-id="b90de-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="b90de-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="b90de-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b90de-110">Child Elements</span></span>                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b90de-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="b90de-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="b90de-112">Elemento URL simpleLocation (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="b90de-112">simpleLocation url Element (Search Connector Schema)</span></span>](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | <span data-ttu-id="b90de-113">serialized: questo elemento contiene il ShellLink con codifica Base64 che punta alla posizione definita nell' <url> elemento.</span><span class="sxs-lookup"><span data-stu-id="b90de-113">serialized: This element contains the base64-encoded ShellLink pointing to the location defined in the <url> element.</span></span> <span data-ttu-id="b90de-114">Windows 7 crea il ShellLink dal valore dell' <url> elemento e aggiorna correttamente questo campo al primo caricamento della libreria, quindi deve essere lasciato vuoto dall'autore.</span><span class="sxs-lookup"><span data-stu-id="b90de-114">Windows 7 creates the ShellLink from the value of the <url> element and properly updates this field on the first load of this library, so it should be left empty by the author.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b90de-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b90de-115">Remarks</span></span>

<span data-ttu-id="b90de-116">Questo elemento può essere utilizzato anziché <locationProvider> quando il percorso si trova nel file System o il connettore è un gestore di protocollo noto, ad esempio MAPI:).</span><span class="sxs-lookup"><span data-stu-id="b90de-116">This element can be used instead of <locationProvider> when the location is on the file system or the connector is a known protocol handler (like mapi:).</span></span> <span data-ttu-id="b90de-117">Se <simpleLocation> è presente, non deve essere un <locationProvider> elemento.</span><span class="sxs-lookup"><span data-stu-id="b90de-117">If <simpleLocation> is present, there MUST NOT be a <locationProvider> element.</span></span> <span data-ttu-id="b90de-118">Per i connettori di ricerca del provider di servizi Web, usare [<locationProvider>](search-schema-sconn-locationprovider.md) invece l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b90de-118">For web service provider search connectors, use the [<locationProvider>](search-schema-sconn-locationprovider.md) element instead.</span></span>

## <a name="examples"></a><span data-ttu-id="b90de-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="b90de-119">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



