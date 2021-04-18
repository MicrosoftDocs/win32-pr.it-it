---
description: Definisce un elenco di strutture che contengono valori dei contatori.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Tipo complesso struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312108"
---
# <a name="structs-complex-type"></a><span data-ttu-id="98a64-103">Tipo complesso struct</span><span class="sxs-lookup"><span data-stu-id="98a64-103">structs Complex Type</span></span>

<span data-ttu-id="98a64-104">Definisce un elenco di strutture che contengono valori dei contatori.</span><span class="sxs-lookup"><span data-stu-id="98a64-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="98a64-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="98a64-105">Child elements</span></span>



| <span data-ttu-id="98a64-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="98a64-106">Element</span></span>    | <span data-ttu-id="98a64-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="98a64-107">Type</span></span>                                                           | <span data-ttu-id="98a64-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98a64-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="98a64-109">**struct**</span><span class="sxs-lookup"><span data-stu-id="98a64-109">**struct**</span></span> | [<span data-ttu-id="98a64-110">**uomo: struct**</span><span class="sxs-lookup"><span data-stu-id="98a64-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="98a64-111">Nome di una struttura che contiene i valori del contatore.</span><span class="sxs-lookup"><span data-stu-id="98a64-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="98a64-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98a64-112">Requirements</span></span>



| <span data-ttu-id="98a64-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="98a64-113">Requirement</span></span> | <span data-ttu-id="98a64-114">Valore</span><span class="sxs-lookup"><span data-stu-id="98a64-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98a64-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98a64-115">Minimum supported client</span></span><br/> | <span data-ttu-id="98a64-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98a64-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98a64-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98a64-117">Minimum supported server</span></span><br/> | <span data-ttu-id="98a64-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98a64-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




