---
description: Definisce una struttura che contiene uno o più valori dei contatori.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Tipo complesso struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312111"
---
# <a name="struct-complex-type"></a><span data-ttu-id="eb3e5-103">Tipo complesso struct</span><span class="sxs-lookup"><span data-stu-id="eb3e5-103">struct Complex Type</span></span>

<span data-ttu-id="eb3e5-104">Definisce una struttura che contiene uno o più valori dei contatori.</span><span class="sxs-lookup"><span data-stu-id="eb3e5-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="eb3e5-105">Attributi</span><span class="sxs-lookup"><span data-stu-id="eb3e5-105">Attributes</span></span>



| <span data-ttu-id="eb3e5-106">Nome</span><span class="sxs-lookup"><span data-stu-id="eb3e5-106">Name</span></span> | <span data-ttu-id="eb3e5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb3e5-107">Type</span></span>                                                                    | <span data-ttu-id="eb3e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb3e5-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3e5-109">name</span><span class="sxs-lookup"><span data-stu-id="eb3e5-109">name</span></span> | [<span data-ttu-id="eb3e5-110">**uomo: CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="eb3e5-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="eb3e5-111">Nome della struttura.</span><span class="sxs-lookup"><span data-stu-id="eb3e5-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="eb3e5-112">tipo</span><span class="sxs-lookup"><span data-stu-id="eb3e5-112">type</span></span> | [<span data-ttu-id="eb3e5-113">**uomo: CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="eb3e5-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="eb3e5-114">Nome simbolico che identifica la struttura.</span><span class="sxs-lookup"><span data-stu-id="eb3e5-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="eb3e5-115">Lo strumento [CTRPP](ctrpp.md) crea una variabile struct con questo nome che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="eb3e5-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eb3e5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb3e5-116">Requirements</span></span>



| <span data-ttu-id="eb3e5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3e5-117">Requirement</span></span> | <span data-ttu-id="eb3e5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="eb3e5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eb3e5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb3e5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb3e5-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb3e5-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eb3e5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb3e5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb3e5-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb3e5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




