---
description: L' <imageLink> elemento facoltativo specifica un'anteprima per questo connettore di ricerca. Questo elemento ha un elemento figlio obbligatorio e nessun attributo.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Elemento Collegamentoimmagine (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306086"
---
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="4736c-104">Elemento Collegamentoimmagine (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="4736c-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="4736c-105">L' <imageLink> elemento facoltativo specifica un'anteprima per questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4736c-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="4736c-106">Questo elemento ha un elemento figlio obbligatorio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="4736c-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4736c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4736c-107">Syntax</span></span>


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="4736c-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="4736c-108">Element Information</span></span>



| <span data-ttu-id="4736c-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="4736c-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="4736c-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4736c-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4736c-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="4736c-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="4736c-112">Elemento URL Collegamentoimmagine (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="4736c-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="4736c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4736c-113">Remarks</span></span>

<span data-ttu-id="4736c-114">Il valore Collegamentoimmagine può essere un percorso di file system locale o un URL.</span><span class="sxs-lookup"><span data-stu-id="4736c-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="4736c-115">Il file di immagine può essere qualsiasi tipo di immagine di base supportato da Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="4736c-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="4736c-116">Esempio di elemento Collegamentoimmagine</span><span class="sxs-lookup"><span data-stu-id="4736c-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



