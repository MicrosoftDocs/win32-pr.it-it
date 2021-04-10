---
title: Tipo complesso BaseEapMethodUserCredentials
description: Informazioni sul tipo complesso BaseEapMethodUserCredentials. Questo tipo è un elemento segnaposto per i dati delle credenziali del metodo.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730178"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="d9b91-105">Tipo complesso BaseEapMethodUserCredentials</span><span class="sxs-lookup"><span data-stu-id="d9b91-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="d9b91-106">Il tipo complesso **BaseEapMethodUserCredentials** è un elemento segnaposto per i dati delle credenziali del metodo.</span><span class="sxs-lookup"><span data-stu-id="d9b91-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
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

## <a name="remarks"></a><span data-ttu-id="d9b91-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9b91-107">Remarks</span></span>

<span data-ttu-id="d9b91-108">Il metodo EAP esegue la convalida dello schema sul contenuto di **BaseEapMethodUserCredentials**.</span><span class="sxs-lookup"><span data-stu-id="d9b91-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b91-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9b91-109">Requirements</span></span>



| <span data-ttu-id="d9b91-110">Ruolo</span><span class="sxs-lookup"><span data-stu-id="d9b91-110">Role</span></span> | <span data-ttu-id="d9b91-111">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="d9b91-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d9b91-112">Client</span><span class="sxs-lookup"><span data-stu-id="d9b91-112">Client</span></span><br/> | <span data-ttu-id="d9b91-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9b91-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9b91-114">Server</span><span class="sxs-lookup"><span data-stu-id="d9b91-114">Server</span></span><br/> | <span data-ttu-id="d9b91-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9b91-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9b91-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9b91-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b91-117">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="d9b91-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d9b91-118">Schema baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="d9b91-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





