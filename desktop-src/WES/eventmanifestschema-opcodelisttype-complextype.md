---
title: Tipo complesso OpcodeListType
description: Definisce un elenco di codici operativi usati per identificare le operazioni di un componente dell'applicazione.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Log eventi di tipo complesso OpcodeListType
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476528"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="7b3b0-104">Tipo complesso OpcodeListType</span><span class="sxs-lookup"><span data-stu-id="7b3b0-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="7b3b0-105">Definisce un elenco di codici operativi usati per identificare le operazioni di un componente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b3b0-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7b3b0-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7b3b0-106">Child elements</span></span>



| <span data-ttu-id="7b3b0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7b3b0-107">Element</span></span>                                                             | <span data-ttu-id="7b3b0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b3b0-108">Type</span></span>                                                             | <span data-ttu-id="7b3b0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b3b0-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="7b3b0-110">**codice operativo**</span><span class="sxs-lookup"><span data-stu-id="7b3b0-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="7b3b0-111">**OpcodeType**</span><span class="sxs-lookup"><span data-stu-id="7b3b0-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="7b3b0-112">Definisce un'operazione all'interno di un componente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b3b0-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7b3b0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b3b0-113">Requirements</span></span>



| <span data-ttu-id="7b3b0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3b0-114">Requirement</span></span> | <span data-ttu-id="7b3b0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7b3b0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b3b0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b3b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3b0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b3b0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7b3b0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b3b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3b0-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b3b0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





