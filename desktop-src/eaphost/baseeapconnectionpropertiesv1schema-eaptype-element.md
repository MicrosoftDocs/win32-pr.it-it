---
title: Elemento EapType (proprietà di connessione dello schema v1)
description: Informazioni sull'elemento EapType. Questo elemento acquisisce la configurazione specifica del metodo all'interno dell'elemento EAP. | Elemento EapType (proprietà di connessione dello schema v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761662"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="6204d-106">Elemento EapType (proprietà di connessione dello schema v1)</span><span class="sxs-lookup"><span data-stu-id="6204d-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="6204d-107">L'elemento **EapType** acquisisce la configurazione specifica del metodo all'interno dell'elemento EAP.</span><span class="sxs-lookup"><span data-stu-id="6204d-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="6204d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="6204d-108">Remarks</span></span>

<span data-ttu-id="6204d-109">L'elemento **EapType** è astratto; ogni metodo deve definire e utilizzare un elemento derivato nei documenti dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6204d-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="6204d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6204d-110">Requirements</span></span>



| <span data-ttu-id="6204d-111">Ruolo</span><span class="sxs-lookup"><span data-stu-id="6204d-111">Role</span></span> | <span data-ttu-id="6204d-112">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="6204d-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="6204d-113">Client</span><span class="sxs-lookup"><span data-stu-id="6204d-113">Client</span></span><br/> | <span data-ttu-id="6204d-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6204d-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6204d-115">Server</span><span class="sxs-lookup"><span data-stu-id="6204d-115">Server</span></span><br/> | <span data-ttu-id="6204d-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6204d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6204d-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6204d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6204d-118">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="6204d-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6204d-119">Schema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6204d-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





