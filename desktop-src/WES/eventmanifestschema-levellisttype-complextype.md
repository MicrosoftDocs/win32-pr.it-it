---
title: Tipo complesso LevelListType
description: Definisce un elenco di livelli di gravità che specificano il livello di dettaglio di un evento.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- Log eventi di tipo complesso LevelListType
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479198"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="50b8b-104">Tipo complesso LevelListType</span><span class="sxs-lookup"><span data-stu-id="50b8b-104">LevelListType Complex Type</span></span>

<span data-ttu-id="50b8b-105">Definisce un elenco di livelli di gravità che specificano il livello di dettaglio di un evento.</span><span class="sxs-lookup"><span data-stu-id="50b8b-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="50b8b-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="50b8b-106">Child elements</span></span>



| <span data-ttu-id="50b8b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="50b8b-107">Element</span></span>                                                          | <span data-ttu-id="50b8b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="50b8b-108">Type</span></span>                                                           | <span data-ttu-id="50b8b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50b8b-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50b8b-110">**livello**</span><span class="sxs-lookup"><span data-stu-id="50b8b-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="50b8b-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="50b8b-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="50b8b-112">Definisce un valore di gravità che determina il livello di dettaglio degli eventi durante la registrazione.</span><span class="sxs-lookup"><span data-stu-id="50b8b-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="50b8b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50b8b-113">Requirements</span></span>



| <span data-ttu-id="50b8b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b8b-114">Requirement</span></span> | <span data-ttu-id="50b8b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="50b8b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50b8b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50b8b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50b8b-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50b8b-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50b8b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50b8b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50b8b-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50b8b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





