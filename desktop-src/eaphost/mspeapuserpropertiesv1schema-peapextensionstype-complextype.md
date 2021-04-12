---
title: Tipo complesso PeapExtensionsType (proprietà di connessione)
description: Informazioni sul tipo complesso PeapExtensionsType. Questo tipo consente miglioramenti futuri allo schema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- PeapExtensionsType di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339278"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a><span data-ttu-id="af4e5-105">Tipo complesso PeapExtensionsType (proprietà di connessione)</span><span class="sxs-lookup"><span data-stu-id="af4e5-105">PeapExtensionsType complex type (connection properties)</span></span>

<span data-ttu-id="af4e5-106">Il tipo complesso **PeapExtensionsType** consente miglioramenti futuri allo schema.</span><span class="sxs-lookup"><span data-stu-id="af4e5-106">The **PeapExtensionsType** complex type enables future enhancements to the schema.</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="af4e5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="af4e5-107">Remarks</span></span>

<span data-ttu-id="af4e5-108">Il tipo complesso **PeapExtensionsType** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="af4e5-108">The **PeapExtensionsType** complex type is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="af4e5-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af4e5-109">Requirements</span></span>



| <span data-ttu-id="af4e5-110">Ruolo</span><span class="sxs-lookup"><span data-stu-id="af4e5-110">Role</span></span> | <span data-ttu-id="af4e5-111">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="af4e5-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="af4e5-112">Client</span><span class="sxs-lookup"><span data-stu-id="af4e5-112">Client</span></span><br/> | <span data-ttu-id="af4e5-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af4e5-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af4e5-114">Server</span><span class="sxs-lookup"><span data-stu-id="af4e5-114">Server</span></span><br/> | <span data-ttu-id="af4e5-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af4e5-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af4e5-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af4e5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af4e5-117">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="af4e5-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="af4e5-118">Schema mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="af4e5-118">mspeapuserpropertiesv1 Schema</span></span>](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





