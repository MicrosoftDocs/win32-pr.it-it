---
title: Elemento EapType (proprietà utente di base)
description: Informazioni sull'elemento EapType. Questo elemento acquisisce la configurazione specifica del metodo all'interno dell'elemento EAP. | Elemento EapType (proprietà utente di base)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321689"
---
# <a name="eaptype-element-base-user-properties"></a><span data-ttu-id="0fd6d-106">Elemento EapType (proprietà utente di base)</span><span class="sxs-lookup"><span data-stu-id="0fd6d-106">EapType element (base user properties)</span></span>

<span data-ttu-id="0fd6d-107">L'elemento **EapType** acquisisce la configurazione specifica del metodo all'interno dell'elemento EAP.</span><span class="sxs-lookup"><span data-stu-id="0fd6d-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="0fd6d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fd6d-108">Remarks</span></span>

<span data-ttu-id="0fd6d-109">L'elemento **EapType** è astratto; ogni metodo deve definire e utilizzare un elemento derivato nei documenti dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0fd6d-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd6d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fd6d-110">Requirements</span></span>



| <span data-ttu-id="0fd6d-111">Ruolo</span><span class="sxs-lookup"><span data-stu-id="0fd6d-111">Role</span></span> | <span data-ttu-id="0fd6d-112">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="0fd6d-112">Minimum supported OS version</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fd6d-113">Client</span><span class="sxs-lookup"><span data-stu-id="0fd6d-113">Client</span></span><br/> | <span data-ttu-id="0fd6d-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fd6d-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0fd6d-115">Server</span><span class="sxs-lookup"><span data-stu-id="0fd6d-115">Server</span></span><br/> | <span data-ttu-id="0fd6d-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fd6d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fd6d-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fd6d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd6d-118">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="0fd6d-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0fd6d-119">Schema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0fd6d-119">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





