---
title: Connections-elemento
description: Informazioni sull'elemento Connections. Questo elemento raccoglie e contiene zero o più elementi di connessione.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Elemento Connections EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300465"
---
# <a name="connections-element"></a><span data-ttu-id="72e07-105">Connections-elemento</span><span class="sxs-lookup"><span data-stu-id="72e07-105">Connections Element</span></span>

<span data-ttu-id="72e07-106">L'elemento **Connections** raccoglie e contiene zero o più elementi [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="72e07-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="72e07-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="72e07-107">Child elements</span></span>



| <span data-ttu-id="72e07-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="72e07-108">Element</span></span>                                                                              | <span data-ttu-id="72e07-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="72e07-109">Type</span></span>   | <span data-ttu-id="72e07-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72e07-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72e07-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="72e07-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="72e07-112">Identifica l'elemento di configurazione EAP.</span><span class="sxs-lookup"><span data-stu-id="72e07-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="72e07-113">**Connessioni**</span><span class="sxs-lookup"><span data-stu-id="72e07-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="72e07-114">Definisce ogni impostazione di configurazione e la associa a un nome.</span><span class="sxs-lookup"><span data-stu-id="72e07-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="72e07-115">L'elemento [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="72e07-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="72e07-116">**Nome**</span><span class="sxs-lookup"><span data-stu-id="72e07-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="72e07-117">string</span><span class="sxs-lookup"><span data-stu-id="72e07-117">string</span></span> | <span data-ttu-id="72e07-118">Acquisisce il nome della connessione da definire, per facilitare l'identificazione di più connessioni.</span><span class="sxs-lookup"><span data-stu-id="72e07-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="72e07-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="72e07-119">Remarks</span></span>

<span data-ttu-id="72e07-120">L'elemento **Connections** non viene usato con i metodi legacy tramite le API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="72e07-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e07-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72e07-121">Requirements</span></span>



| <span data-ttu-id="72e07-122">Ruolo</span><span class="sxs-lookup"><span data-stu-id="72e07-122">Role</span></span> | <span data-ttu-id="72e07-123">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="72e07-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="72e07-124">Client</span><span class="sxs-lookup"><span data-stu-id="72e07-124">Client</span></span><br/> | <span data-ttu-id="72e07-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72e07-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72e07-126">Server</span><span class="sxs-lookup"><span data-stu-id="72e07-126">Server</span></span><br/> | <span data-ttu-id="72e07-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72e07-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72e07-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72e07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e07-129">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="72e07-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="72e07-130">Schema eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="72e07-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





