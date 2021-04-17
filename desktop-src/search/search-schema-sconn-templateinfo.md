---
description: Questo <templateInfo> elemento facoltativo specifica un tipo di cartella per visualizzare i risultati di una query su questo connettore di ricerca. Questo elemento non ha attributi e un solo figlio obbligatorio.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Elemento templateInfo (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306074"
---
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="fee41-104">Elemento templateInfo (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="fee41-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="fee41-105">Questo <templateInfo> elemento facoltativo specifica un tipo di cartella per visualizzare i risultati di una query su questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fee41-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="fee41-106">Questo elemento non ha attributi e un solo figlio obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fee41-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fee41-107">Syntax</span></span>


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="fee41-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fee41-108">Element Information</span></span>



| <span data-ttu-id="fee41-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="fee41-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="fee41-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fee41-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="fee41-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="fee41-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="fee41-112">Elemento folderType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="fee41-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="fee41-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fee41-113">Remarks</span></span>

<span data-ttu-id="fee41-114">Se non si specifica un tipo di cartella particolare nell' <templateInfo> elemento, Windows usa il tipo di cartella del connettore di ricerca generale {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span><span class="sxs-lookup"><span data-stu-id="fee41-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="fee41-115">Esempio di elemento templateInfo</span><span class="sxs-lookup"><span data-stu-id="fee41-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



