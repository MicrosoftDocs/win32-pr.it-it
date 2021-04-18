---
title: Tipo complesso headerFieldType
description: Definisce gli elementi utilizzati per creare un campo di intestazione in un messaggio di posta elettronica.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Utilità di pianificazione di tipo complesso headerFieldType
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301334"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="57234-104">Tipo complesso headerFieldType</span><span class="sxs-lookup"><span data-stu-id="57234-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="57234-105">Definisce gli elementi utilizzati per creare un campo di intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="57234-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="57234-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="57234-106">Child elements</span></span>



| <span data-ttu-id="57234-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="57234-107">Element</span></span>                                                            | <span data-ttu-id="57234-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="57234-108">Type</span></span>                                                                    | <span data-ttu-id="57234-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57234-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="57234-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="57234-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="57234-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="57234-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="57234-112">Specifica il nome del campo di intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="57234-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="57234-113">**Valore**</span><span class="sxs-lookup"><span data-stu-id="57234-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="57234-114">**string**</span><span class="sxs-lookup"><span data-stu-id="57234-114">**string**</span></span>                                                              | <span data-ttu-id="57234-115">Specifica il valore di un campo di intestazione in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="57234-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="57234-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57234-116">Requirements</span></span>



| <span data-ttu-id="57234-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="57234-117">Requirement</span></span> | <span data-ttu-id="57234-118">Valore</span><span class="sxs-lookup"><span data-stu-id="57234-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57234-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57234-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57234-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57234-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57234-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57234-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57234-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57234-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





