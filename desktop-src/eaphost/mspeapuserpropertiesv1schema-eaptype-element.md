---
title: Elemento EapType (mspeapuserpropertiesv1schema)
description: Questo elemento è un tipo derivato dell'elemento EapType dello schema baseeapuserpropertiesv1. Per mspeapuserpropertiesv1schema.
ms.assetid: 921c1f95-900a-4fd2-bb42-341e5ba39b23
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ccedc72baf3a677acc3a318895defbc97bb26287
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334339"
---
# <a name="eaptype-element-mspeapuserpropertiesv1schema"></a><span data-ttu-id="74bd8-105">Elemento EapType (mspeapuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="74bd8-105">EapType Element (mspeapuserpropertiesv1schema)</span></span>

<span data-ttu-id="74bd8-106">L'elemento **EapType** è un tipo derivato dell'elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) dello schema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="74bd8-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType
        "
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="74bd8-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="74bd8-107">Child elements</span></span>



| <span data-ttu-id="74bd8-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="74bd8-108">Element</span></span>                                                                               | <span data-ttu-id="74bd8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="74bd8-109">Type</span></span>                                                                                      | <span data-ttu-id="74bd8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74bd8-110">Description</span></span>                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74bd8-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="74bd8-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md)                              |                                                                                           | <span data-ttu-id="74bd8-112">L'elemento [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) identifica il metodo interno e le credenziali da utilizzare con il metodo.</span><span class="sxs-lookup"><span data-stu-id="74bd8-112">The [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) element identifies the inner method and the credentials to be used with that method.</span></span> <span data-ttu-id="74bd8-113">Quando la configurazione PEAP è configurata per l'accesso Guest PEAP, questo elemento è assente.</span><span class="sxs-lookup"><span data-stu-id="74bd8-113">When PEAP configuration is configured for PEAP guest access, this element is absent.</span></span><br/>                                  |
| [<span data-ttu-id="74bd8-114">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="74bd8-114">**PeapExtensions**</span></span>](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) | [<span data-ttu-id="74bd8-115">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="74bd8-115">**PeapExtensionsType**</span></span>](mspeapuserpropertiesv1schema-peapextensionstype-complextype.md) | <span data-ttu-id="74bd8-116">L'elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="74bd8-116">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <br/> <span data-ttu-id="74bd8-117">L'elemento [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74bd8-117">The [**PeapExtensions**](mspeapuserpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="74bd8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74bd8-118">Requirements</span></span>



| <span data-ttu-id="74bd8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="74bd8-119">Requirement</span></span> | <span data-ttu-id="74bd8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="74bd8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74bd8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74bd8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="74bd8-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74bd8-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74bd8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74bd8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="74bd8-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74bd8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74bd8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74bd8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bd8-126">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="74bd8-126">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="74bd8-127">Schema mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="74bd8-127">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





