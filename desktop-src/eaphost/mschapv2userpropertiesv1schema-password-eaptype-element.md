---
title: Password (EapType)-elemento
description: Informazioni sull'elemento password (EapType). Questo elemento identifica la password dell'utente o del computer da autenticare.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047378"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="fbd41-105">Password (EapType)-elemento</span><span class="sxs-lookup"><span data-stu-id="fbd41-105">Password (EapType) Element</span></span>

<span data-ttu-id="fbd41-106">L'elemento **password (EapType)** identifica la password dell'utente o del computer da autenticare.</span><span class="sxs-lookup"><span data-stu-id="fbd41-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="fbd41-107">L'elemento **password** è definito dall'elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fbd41-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbd41-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbd41-108">Remarks</span></span>

<span data-ttu-id="fbd41-109">Se l'elemento **password (EapType)** non è presente, l'hash della password viene ottenuto da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="fbd41-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="fbd41-110">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbd41-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd41-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbd41-111">Requirements</span></span>



| <span data-ttu-id="fbd41-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="fbd41-112">Role</span></span> | <span data-ttu-id="fbd41-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="fbd41-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="fbd41-114">Client</span><span class="sxs-lookup"><span data-stu-id="fbd41-114">Client</span></span><br/> | <span data-ttu-id="fbd41-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbd41-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbd41-116">Server</span><span class="sxs-lookup"><span data-stu-id="fbd41-116">Server</span></span><br/> | <span data-ttu-id="fbd41-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fbd41-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbd41-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbd41-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbd41-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fbd41-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fbd41-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="fbd41-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="fbd41-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fbd41-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fbd41-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="fbd41-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="fbd41-123">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="fbd41-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fbd41-124">Schema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fbd41-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





