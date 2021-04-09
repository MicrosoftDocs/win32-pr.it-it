---
title: Elemento LogonDomain (EapType)
description: Informazioni sull'elemento LogonDomain (EapType). Questo elemento identifica il dominio dell'utente o del computer da autenticare.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Elemento LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047348"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="e7503-105">Elemento LogonDomain (EapType)</span><span class="sxs-lookup"><span data-stu-id="e7503-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="e7503-106">L'elemento **LogonDomain (EapType)** identifica il dominio dell'utente o del computer da autenticare.</span><span class="sxs-lookup"><span data-stu-id="e7503-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="e7503-107">L'elemento **LogonDomain** è definito dall'elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e7503-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7503-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7503-108">Remarks</span></span>

<span data-ttu-id="e7503-109">Se l'elemento **LogonDomain (EapType)** non è presente, viene usato il dominio da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="e7503-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="e7503-110">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e7503-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7503-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7503-111">Requirements</span></span>



| <span data-ttu-id="e7503-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="e7503-112">Role</span></span> | <span data-ttu-id="e7503-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="e7503-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="e7503-114">Client</span><span class="sxs-lookup"><span data-stu-id="e7503-114">Client</span></span><br/> | <span data-ttu-id="e7503-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7503-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7503-116">Server</span><span class="sxs-lookup"><span data-stu-id="e7503-116">Server</span></span><br/> | <span data-ttu-id="e7503-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7503-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7503-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7503-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7503-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e7503-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e7503-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e7503-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e7503-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e7503-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e7503-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="e7503-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="e7503-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="e7503-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e7503-124">Schema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="e7503-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





