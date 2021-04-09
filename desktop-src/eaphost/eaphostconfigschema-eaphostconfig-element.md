---
title: Elemento EapHostConfig
description: Contiene l'elemento EapMethod e la configurazione o l'elemento ConfigBlob. Gli elementi config e ConfigBlob non possono essere usati contemporaneamente.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Elemento EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047786"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="2284c-105">Elemento EapHostConfig</span><span class="sxs-lookup"><span data-stu-id="2284c-105">EapHostConfig Element</span></span>

<span data-ttu-id="2284c-106">L'elemento **EapHostConfig** contiene l'elemento [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) e l'elemento [**config**](eaphostconfigschema-config-eaphostconfig-element.md) o [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2284c-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="2284c-107">Gli elementi [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="2284c-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="2284c-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2284c-108">Child elements</span></span>



| <span data-ttu-id="2284c-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2284c-109">Element</span></span>                                                                    | <span data-ttu-id="2284c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2284c-110">Type</span></span>                                                                                     | <span data-ttu-id="2284c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2284c-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2284c-112">**File di configurazione**</span><span class="sxs-lookup"><span data-stu-id="2284c-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="2284c-113">**BaseEapMethodConfig**</span><span class="sxs-lookup"><span data-stu-id="2284c-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="2284c-114">Viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="2284c-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="2284c-115">**ConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="2284c-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="2284c-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="2284c-116">hexBinary</span></span>                                                                                | <span data-ttu-id="2284c-117">Viene usato quando la configurazione del metodo è in formato BLOB binario anziché in formato testo stringa.</span><span class="sxs-lookup"><span data-stu-id="2284c-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="2284c-118">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="2284c-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="2284c-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="2284c-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="2284c-120">Identifica il metodo a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="2284c-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="2284c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2284c-121">Remarks</span></span>

<span data-ttu-id="2284c-122">L'elemento **processContents** consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="2284c-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="2284c-123">L'elemento **processContents** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2284c-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2284c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2284c-124">Requirements</span></span>



| <span data-ttu-id="2284c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2284c-125">Requirement</span></span> | <span data-ttu-id="2284c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2284c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2284c-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2284c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2284c-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2284c-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2284c-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2284c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2284c-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2284c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2284c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2284c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2284c-132">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="2284c-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2284c-133">Schema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="2284c-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





