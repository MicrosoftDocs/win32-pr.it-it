---
title: Tipo complesso BaseEapParameters-proprietà di connessione
description: Definisce l'elemento segnaposto per il tipo di metodo e la configurazione specifica del metodo.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323809"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="2ae9a-104">Tipo complesso BaseEapParameters-proprietà di connessione</span><span class="sxs-lookup"><span data-stu-id="2ae9a-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="2ae9a-105">Il tipo complesso **BaseEapParameters** definisce l'elemento segnaposto per il tipo di metodo e la configurazione specifica del metodo.</span><span class="sxs-lookup"><span data-stu-id="2ae9a-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2ae9a-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2ae9a-106">Child elements</span></span>



| <span data-ttu-id="2ae9a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="2ae9a-107">Element</span></span>                                                                            | <span data-ttu-id="2ae9a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ae9a-108">Type</span></span>    | <span data-ttu-id="2ae9a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ae9a-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="2ae9a-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="2ae9a-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="2ae9a-111">numero intero</span><span class="sxs-lookup"><span data-stu-id="2ae9a-111">integer</span></span> | <span data-ttu-id="2ae9a-112">Qualsiasi istanza dello schema è consentita in questo punto.</span><span class="sxs-lookup"><span data-stu-id="2ae9a-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2ae9a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ae9a-113">Remarks</span></span>

<span data-ttu-id="2ae9a-114">In **BaseEapParameters** il metodo può definire gli elementi costitutivi.</span><span class="sxs-lookup"><span data-stu-id="2ae9a-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="2ae9a-115">Il metodo esegue anche la convalida dello schema sugli elementi in **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="2ae9a-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae9a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ae9a-116">Requirements</span></span>



| <span data-ttu-id="2ae9a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae9a-117">Requirement</span></span> | <span data-ttu-id="2ae9a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2ae9a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ae9a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae9a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae9a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ae9a-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ae9a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ae9a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae9a-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ae9a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ae9a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ae9a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae9a-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="2ae9a-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2ae9a-125">Schema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2ae9a-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





