---
title: Elemento EAP (proprietà di connessione)
description: Informazioni sull'elemento EAP. Questo elemento acquisisce il tipo di metodo selezionato e la configurazione specifica del metodo. | Elemento EAP (proprietà di connessione)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- EAPHost (elemento EAP)
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321336"
---
# <a name="eap-element-connection-properties"></a><span data-ttu-id="9fc7a-106">Elemento EAP (proprietà di connessione)</span><span class="sxs-lookup"><span data-stu-id="9fc7a-106">Eap Element (connection properties)</span></span>

<span data-ttu-id="9fc7a-107">L'elemento **EAP** acquisisce il tipo di metodo selezionato e la configurazione specifica del metodo.</span><span class="sxs-lookup"><span data-stu-id="9fc7a-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="9fc7a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fc7a-108">Remarks</span></span>

<span data-ttu-id="9fc7a-109">Il metodo può definire gli elementi costitutivi all'interno dell'elemento **EAP** .</span><span class="sxs-lookup"><span data-stu-id="9fc7a-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="9fc7a-110">Il metodo esegue inoltre la convalida dello schema sugli elementi in **EAP**.</span><span class="sxs-lookup"><span data-stu-id="9fc7a-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc7a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fc7a-111">Requirements</span></span>



| <span data-ttu-id="9fc7a-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="9fc7a-112">Role</span></span> | <span data-ttu-id="9fc7a-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="9fc7a-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="9fc7a-114">Client</span><span class="sxs-lookup"><span data-stu-id="9fc7a-114">Client</span></span><br/> | <span data-ttu-id="9fc7a-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fc7a-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fc7a-116">Server</span><span class="sxs-lookup"><span data-stu-id="9fc7a-116">Server</span></span><br/> | <span data-ttu-id="9fc7a-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fc7a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fc7a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fc7a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc7a-119">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="9fc7a-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9fc7a-120">Schema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="9fc7a-120">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





