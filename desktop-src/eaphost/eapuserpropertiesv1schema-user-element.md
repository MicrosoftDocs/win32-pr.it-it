---
title: Elemento User
description: Informazioni sull'elemento User. Questo elemento non viene usato quando si usano i metodi legacy tramite le API EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Elemento utente EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730362"
---
# <a name="user-element"></a><span data-ttu-id="cdf72-105">Elemento User</span><span class="sxs-lookup"><span data-stu-id="cdf72-105">User Element</span></span>

<span data-ttu-id="cdf72-106">L'elemento **User** non viene usato quando si usano i metodi legacy tramite le API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="cdf72-106">The **User** element is not used when using legacy methods via the EAPHost APIs.</span></span>

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="cdf72-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="cdf72-107">Child elements</span></span>



| <span data-ttu-id="cdf72-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cdf72-108">Element</span></span>                                                  | <span data-ttu-id="cdf72-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdf72-109">Type</span></span> | <span data-ttu-id="cdf72-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdf72-110">Description</span></span>                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="cdf72-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="cdf72-111">**Eap**</span></span>](baseeapuserpropertiesv1schema-eap-element.md) |      | <span data-ttu-id="cdf72-112">Acquisisce le informazioni sulle credenziali specifiche del metodo e del tipo di metodo.</span><span class="sxs-lookup"><span data-stu-id="cdf72-112">Captures the method type and method specific credential information.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cdf72-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdf72-113">Requirements</span></span>



| <span data-ttu-id="cdf72-114">Ruolo</span><span class="sxs-lookup"><span data-stu-id="cdf72-114">Role</span></span> | <span data-ttu-id="cdf72-115">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="cdf72-115">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="cdf72-116">Client</span><span class="sxs-lookup"><span data-stu-id="cdf72-116">Client</span></span><br/> | <span data-ttu-id="cdf72-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdf72-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdf72-118">Server</span><span class="sxs-lookup"><span data-stu-id="cdf72-118">Server</span></span><br/> | <span data-ttu-id="cdf72-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdf72-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cdf72-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdf72-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf72-121">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="cdf72-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cdf72-122">Schema eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdf72-122">eapuserpropertiesv1 Schema</span></span>](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





