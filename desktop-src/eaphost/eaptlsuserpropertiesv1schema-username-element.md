---
title: Elemento UserName (TLS)
description: Informazioni sull'elemento UserName. Questo elemento acquisisce il nome utente da inviare nella risposta EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Elemento Username EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300480"
---
# <a name="username-element-tls"></a><span data-ttu-id="22704-105">Elemento UserName (TLS)</span><span class="sxs-lookup"><span data-stu-id="22704-105">Username element (TLS)</span></span>

<span data-ttu-id="22704-106">L'elemento **username** acquisisce il nome utente da inviare nella risposta EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="22704-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="22704-107">Se l'elemento **username** è assente, EAP-TLS usa il nome nel certificato a cui si fa riferimento nell'elemento [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="22704-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="22704-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22704-108">Requirements</span></span>



| <span data-ttu-id="22704-109">Ruolo</span><span class="sxs-lookup"><span data-stu-id="22704-109">Role</span></span> | <span data-ttu-id="22704-110">Versioni minime del sistema operativo supportate</span><span class="sxs-lookup"><span data-stu-id="22704-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="22704-111">Client</span><span class="sxs-lookup"><span data-stu-id="22704-111">Client</span></span><br/> | <span data-ttu-id="22704-112">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22704-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22704-113">Server</span><span class="sxs-lookup"><span data-stu-id="22704-113">Server</span></span><br/> | <span data-ttu-id="22704-114">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22704-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22704-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22704-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22704-116">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="22704-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="22704-117">Schema eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="22704-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





