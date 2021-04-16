---
title: Identity-elemento
description: Informazioni sull'elemento Identity EAPHost. Questo elemento acquisisce l'identità utilizzata per l'autenticazione.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Elemento Identity EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474278"
---
# <a name="identity-element"></a><span data-ttu-id="08b1f-105">Identity-elemento</span><span class="sxs-lookup"><span data-stu-id="08b1f-105">Identity Element</span></span>

<span data-ttu-id="08b1f-106">L'elemento **Identity** acquisisce l'identità utilizzata per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="08b1f-106">The **Identity** element captures the identity used for authentication.</span></span>

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a><span data-ttu-id="08b1f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="08b1f-107">Remarks</span></span>

<span data-ttu-id="08b1f-108">L'elemento **Identity** è astratto; ogni metodo deve definire e utilizzare un elemento derivato nei documenti dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="08b1f-108">The **Identity** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b1f-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08b1f-109">Requirements</span></span>



| <span data-ttu-id="08b1f-110">Ruolo</span><span class="sxs-lookup"><span data-stu-id="08b1f-110">Role</span></span> | <span data-ttu-id="08b1f-111">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="08b1f-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="08b1f-112">Client</span><span class="sxs-lookup"><span data-stu-id="08b1f-112">Client</span></span><br/> | <span data-ttu-id="08b1f-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08b1f-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="08b1f-114">Server</span><span class="sxs-lookup"><span data-stu-id="08b1f-114">Server</span></span><br/> | <span data-ttu-id="08b1f-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08b1f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08b1f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08b1f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b1f-117">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="08b1f-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="08b1f-118">Schema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="08b1f-118">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





