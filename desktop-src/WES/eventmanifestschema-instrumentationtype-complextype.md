---
title: Tipo complesso InstrumentationType
description: Definisce il contenuto della sezione di strumentazione del manifesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Log eventi di tipo complesso InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302546"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="90693-104">Tipo complesso InstrumentationType</span><span class="sxs-lookup"><span data-stu-id="90693-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="90693-105">Definisce il contenuto della sezione di strumentazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="90693-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="90693-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="90693-106">Child elements</span></span>



| <span data-ttu-id="90693-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="90693-107">Element</span></span>                                                                  | <span data-ttu-id="90693-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="90693-108">Type</span></span>                                                             | <span data-ttu-id="90693-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90693-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="90693-110">**eventi**</span><span class="sxs-lookup"><span data-stu-id="90693-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="90693-111">**EventsType**</span><span class="sxs-lookup"><span data-stu-id="90693-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="90693-112">Contiene un elenco di provider definiti dal manifesto.</span><span class="sxs-lookup"><span data-stu-id="90693-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="90693-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90693-113">Requirements</span></span>



| <span data-ttu-id="90693-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="90693-114">Requirement</span></span> | <span data-ttu-id="90693-115">Valore</span><span class="sxs-lookup"><span data-stu-id="90693-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="90693-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90693-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90693-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90693-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="90693-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90693-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90693-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90693-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





