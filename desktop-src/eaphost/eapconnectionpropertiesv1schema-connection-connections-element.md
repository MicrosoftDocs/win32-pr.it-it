---
title: Elemento Connection (Connections)
description: Definisce ogni impostazione di configurazione e la associa a un nome. L'elemento Connection è facoltativo.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Elemento Connection EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301770"
---
# <a name="connection-connections-element"></a><span data-ttu-id="b3cbf-105">Elemento Connection (Connections)</span><span class="sxs-lookup"><span data-stu-id="b3cbf-105">Connection (Connections) Element</span></span>

<span data-ttu-id="b3cbf-106">L'elemento **Connection (Connections)** definisce ogni impostazione di configurazione e la associa a un nome.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="b3cbf-107">L'elemento **Connection** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b3cbf-108">L'elemento **Connection** è definito dall'elemento [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b3cbf-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b3cbf-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b3cbf-109">Child elements</span></span>



| <span data-ttu-id="b3cbf-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b3cbf-110">Element</span></span>                                                                 | <span data-ttu-id="b3cbf-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3cbf-111">Type</span></span>   | <span data-ttu-id="b3cbf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3cbf-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3cbf-113">**EAP**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="b3cbf-114">Identifica l'elemento di configurazione EAP.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="b3cbf-115">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="b3cbf-116">string</span><span class="sxs-lookup"><span data-stu-id="b3cbf-116">string</span></span> | <span data-ttu-id="b3cbf-117">Acquisisce il nome della connessione da definire, per facilitare l'identificazione di più connessioni.</span><span class="sxs-lookup"><span data-stu-id="b3cbf-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="b3cbf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3cbf-118">Requirements</span></span>



| <span data-ttu-id="b3cbf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cbf-119">Requirement</span></span> | <span data-ttu-id="b3cbf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b3cbf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3cbf-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cbf-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3cbf-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3cbf-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cbf-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3cbf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3cbf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3cbf-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="b3cbf-126">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b3cbf-127">**Connessioni**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="b3cbf-128">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b3cbf-129">**Connessioni**</span><span class="sxs-lookup"><span data-stu-id="b3cbf-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="b3cbf-130">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="b3cbf-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b3cbf-131">Schema eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b3cbf-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





