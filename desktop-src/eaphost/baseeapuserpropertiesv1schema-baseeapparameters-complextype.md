---
title: Tipo complesso BaseEapParameters-proprietà utente
description: Definisce l'elemento che ha specificato il metodo legacy selezionato e le credenziali specifiche del metodo.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323771"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="aa8c8-104">Tipo complesso BaseEapParameters-proprietà utente</span><span class="sxs-lookup"><span data-stu-id="aa8c8-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="aa8c8-105">Il tipo complesso **BaseEapParameters** definisce l'elemento che ha specificato il metodo legacy selezionato e le credenziali specifiche del metodo.</span><span class="sxs-lookup"><span data-stu-id="aa8c8-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="aa8c8-106">Il metodo può definire gli elementi costitutivi all'interno di **BaseEapParameters**; il metodo esegue anche la convalida dello schema sugli elementi in **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="aa8c8-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="aa8c8-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="aa8c8-107">Child elements</span></span>



| <span data-ttu-id="aa8c8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa8c8-108">Element</span></span>                                                                      | <span data-ttu-id="aa8c8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa8c8-109">Type</span></span>    | <span data-ttu-id="aa8c8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa8c8-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa8c8-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="aa8c8-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="aa8c8-112">numero intero</span><span class="sxs-lookup"><span data-stu-id="aa8c8-112">integer</span></span> | <span data-ttu-id="aa8c8-113">Definisce l'elemento segnaposto per il tipo di metodo selezionato e le credenziali specifiche del metodo.</span><span class="sxs-lookup"><span data-stu-id="aa8c8-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="aa8c8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa8c8-114">Requirements</span></span>



| <span data-ttu-id="aa8c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa8c8-115">Requirement</span></span> | <span data-ttu-id="aa8c8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="aa8c8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa8c8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa8c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8c8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa8c8-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa8c8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa8c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8c8-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa8c8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa8c8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa8c8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa8c8-122">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="aa8c8-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="aa8c8-123">Schema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="aa8c8-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





