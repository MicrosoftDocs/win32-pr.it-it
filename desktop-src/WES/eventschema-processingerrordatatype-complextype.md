---
title: Tipo complesso ProcessingErrorDataType
description: Definisce un errore che si è verificato durante il rendering dei dati dell'evento per l'evento.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Log eventi di tipo complesso ProcessingErrorDataType
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120770"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="c342d-104">Tipo complesso ProcessingErrorDataType</span><span class="sxs-lookup"><span data-stu-id="c342d-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="c342d-105">Definisce un errore che si è verificato durante il rendering dei dati dell'evento per l'evento.</span><span class="sxs-lookup"><span data-stu-id="c342d-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="c342d-106">Questo problema può verificarsi se i dati dell'evento non corrispondono alla definizione del modello di dati dell'evento nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="c342d-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
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

## <a name="child-elements"></a><span data-ttu-id="c342d-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c342d-107">Child elements</span></span>



| <span data-ttu-id="c342d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c342d-108">Element</span></span>                                                                          | <span data-ttu-id="c342d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c342d-109">Type</span></span>        | <span data-ttu-id="c342d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c342d-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c342d-111">**DataItemName**</span><span class="sxs-lookup"><span data-stu-id="c342d-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="c342d-112">string</span><span class="sxs-lookup"><span data-stu-id="c342d-112">string</span></span>      | <span data-ttu-id="c342d-113">Nome dell'elemento di dati dell'evento che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="c342d-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="c342d-114">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c342d-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="c342d-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c342d-115">unsignedInt</span></span> | <span data-ttu-id="c342d-116">Codice di errore dell'errore che si è verificato durante il rendering dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c342d-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="c342d-117">**EventPayload**</span><span class="sxs-lookup"><span data-stu-id="c342d-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="c342d-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="c342d-118">hexBinary</span></span>   | <span data-ttu-id="c342d-119">BLOB binario che contiene tutti i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c342d-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="c342d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c342d-120">Requirements</span></span>



| <span data-ttu-id="c342d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c342d-121">Requirement</span></span> | <span data-ttu-id="c342d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c342d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c342d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c342d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c342d-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c342d-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c342d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c342d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c342d-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c342d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





