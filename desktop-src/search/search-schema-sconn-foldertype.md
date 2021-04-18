---
description: L' <folderType> elemento specifica il GUID per il tipo di cartella. Questo elemento è obbligatorio se l' <templateInfo> elemento esiste. Non ha attributi e nessun elemento figlio.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: Elemento folderType (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484404"
---
# <a name="foldertype-element-search-connector-schema"></a><span data-ttu-id="8f0c2-105">Elemento folderType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="8f0c2-105">folderType Element (Search Connector Schema)</span></span>

<span data-ttu-id="8f0c2-106">L' <folderType> elemento specifica il GUID per il tipo di cartella.</span><span class="sxs-lookup"><span data-stu-id="8f0c2-106">The <folderType> element specifies GUID for the folder type.</span></span> <span data-ttu-id="8f0c2-107">Questo elemento è obbligatorio se l' <templateInfo> elemento esiste.</span><span class="sxs-lookup"><span data-stu-id="8f0c2-107">This element is required if the <templateInfo> element exists.</span></span> <span data-ttu-id="8f0c2-108">Non ha attributi e nessun elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="8f0c2-108">It has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f0c2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f0c2-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="8f0c2-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8f0c2-110">Element Information</span></span>



| <span data-ttu-id="8f0c2-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="8f0c2-111">Parent Element</span></span>                                                                         | <span data-ttu-id="8f0c2-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8f0c2-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="8f0c2-113">Elemento templateInfo (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="8f0c2-113">templateInfo Element (Search Connector Schema)</span></span>](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="8f0c2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f0c2-114">Remarks</span></span>

<span data-ttu-id="8f0c2-115">Il GUID predefinito è {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, un tipo di cartella generale per i connettori di ricerca federata (OpenSearch).</span><span class="sxs-lookup"><span data-stu-id="8f0c2-115">The default GUID is {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, a general folder type for federated search (OpenSearch) connectors.</span></span>

## <a name="example-of-a-foldertype-element"></a><span data-ttu-id="8f0c2-116">Esempio di elemento folderType</span><span class="sxs-lookup"><span data-stu-id="8f0c2-116">Example of a folderType Element</span></span>


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



