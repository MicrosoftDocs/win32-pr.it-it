---
description: L' <url> elemento specifica un URL per l'anteprima per questo connettore di ricerca. Se <imageLink> esiste, questo elemento è obbligatorio. Non ha elementi figlio e nessun attributo.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Elemento URL Collegamentoimmagine (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306087"
---
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="5e81a-105">Elemento URL Collegamentoimmagine (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="5e81a-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="5e81a-106">L' <url> elemento specifica un URL per l'anteprima per questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="5e81a-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="5e81a-107">Se <imageLink> esiste, questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5e81a-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="5e81a-108">Non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="5e81a-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e81a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e81a-109">Syntax</span></span>


```
<!-- url -->
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



## <a name="element-information"></a><span data-ttu-id="5e81a-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5e81a-110">Element Information</span></span>



| <span data-ttu-id="5e81a-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5e81a-111">Parent Element</span></span>                                                                   | <span data-ttu-id="5e81a-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5e81a-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5e81a-113">Elemento Collegamentoimmagine (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="5e81a-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="5e81a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e81a-114">Remarks</span></span>

<span data-ttu-id="5e81a-115">Il valore può essere un percorso di file system locale o un URL.</span><span class="sxs-lookup"><span data-stu-id="5e81a-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="5e81a-116">Il file di immagine può essere qualsiasi tipo di immagine di base supportato da Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="5e81a-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="5e81a-117">Esempio di elemento imageLinkurl</span><span class="sxs-lookup"><span data-stu-id="5e81a-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



