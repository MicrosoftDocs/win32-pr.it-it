---
title: Tipo complesso BaseEapMethodConfig
description: Informazioni sul tipo complesso BaseEapMethodConfig. Questo tipo è un elemento segnaposto per la configurazione del metodo.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- BaseEapMethodConfig di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399740"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="39f4e-105">Tipo complesso BaseEapMethodConfig</span><span class="sxs-lookup"><span data-stu-id="39f4e-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="39f4e-106">Il tipo complesso **BaseEapMethodConfig** è un elemento segnaposto per la configurazione del metodo.</span><span class="sxs-lookup"><span data-stu-id="39f4e-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="39f4e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="39f4e-107">Remarks</span></span>

<span data-ttu-id="39f4e-108">Il metodo EAP esegue la convalida dello schema sul contenuto dell'elemento **BaseEapMethodConfig** .</span><span class="sxs-lookup"><span data-stu-id="39f4e-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f4e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39f4e-109">Requirements</span></span>



| <span data-ttu-id="39f4e-110">Ruolo</span><span class="sxs-lookup"><span data-stu-id="39f4e-110">Role</span></span> | <span data-ttu-id="39f4e-111">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="39f4e-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="39f4e-112">Client</span><span class="sxs-lookup"><span data-stu-id="39f4e-112">Client</span></span><br/> | <span data-ttu-id="39f4e-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39f4e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39f4e-114">Server</span><span class="sxs-lookup"><span data-stu-id="39f4e-114">Server</span></span><br/> | <span data-ttu-id="39f4e-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39f4e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39f4e-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39f4e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f4e-117">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="39f4e-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="39f4e-118">Schema baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="39f4e-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





