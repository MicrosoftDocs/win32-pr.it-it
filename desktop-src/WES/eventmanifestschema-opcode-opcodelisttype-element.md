---
title: Elemento Opcode (OpcodeListType)
description: Contiene un valore numerico che identifica l'attività o un punto all'interno di un'attività che l'applicazione stava eseguendo durante la generazione dell'evento (ad esempio, l'inizializzazione o la chiusura).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- opcode element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121335"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="be83a-104">Elemento Opcode (OpcodeListType)</span><span class="sxs-lookup"><span data-stu-id="be83a-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="be83a-105">Contiene un valore numerico che identifica l'attività o un punto all'interno di un'attività che l'applicazione stava eseguendo durante la generazione dell'evento (ad esempio, l'inizializzazione o la chiusura).</span><span class="sxs-lookup"><span data-stu-id="be83a-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="be83a-106">L'elemento **OpCode** è definito dal tipo complesso [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="be83a-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="be83a-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be83a-107">Requirements</span></span>



| <span data-ttu-id="be83a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="be83a-108">Requirement</span></span> | <span data-ttu-id="be83a-109">Valore</span><span class="sxs-lookup"><span data-stu-id="be83a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="be83a-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be83a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="be83a-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be83a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="be83a-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be83a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="be83a-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be83a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be83a-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be83a-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="be83a-115">**Elementi padre**</span><span class="sxs-lookup"><span data-stu-id="be83a-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="be83a-116">**OpCodes (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="be83a-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="be83a-117">**OpCodes (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="be83a-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="be83a-118">**OpCodes (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="be83a-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





