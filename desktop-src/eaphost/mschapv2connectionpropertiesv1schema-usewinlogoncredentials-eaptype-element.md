---
title: Elemento UseWinLogonCredentials (EapType)
description: Informazioni sull'elemento UseWinLogonCredentials (EapType). Questo elemento controlla l'uso di credenziali WinLogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730370"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="a5b18-105">Elemento UseWinLogonCredentials (EapType)</span><span class="sxs-lookup"><span data-stu-id="a5b18-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="a5b18-106">L'elemento **UseWinLogonCredentials (EapType)** controlla l'uso delle credenziali WinLogin.</span><span class="sxs-lookup"><span data-stu-id="a5b18-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="a5b18-107">L'elemento **UseWinLogonCredentials** è definito dall'elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b18-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b18-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5b18-108">Remarks</span></span>

<span data-ttu-id="a5b18-109">Se TRUE, EAP MS-CHAPv2 ottiene le credenziali da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="a5b18-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="a5b18-110">Se FALSE, EAP MS-CHAPv2 ottiene le credenziali dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a5b18-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="a5b18-111">L'elemento **UseWinLogonCredentials (EapType)** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a5b18-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b18-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5b18-112">Requirements</span></span>



| <span data-ttu-id="a5b18-113">Ruolo</span><span class="sxs-lookup"><span data-stu-id="a5b18-113">Role</span></span> | <span data-ttu-id="a5b18-114">Versioni minime del sistema operativo supportate</span><span class="sxs-lookup"><span data-stu-id="a5b18-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="a5b18-115">Client</span><span class="sxs-lookup"><span data-stu-id="a5b18-115">Client</span></span><br/> | <span data-ttu-id="a5b18-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5b18-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5b18-117">Server</span><span class="sxs-lookup"><span data-stu-id="a5b18-117">Server</span></span><br/> | <span data-ttu-id="a5b18-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a5b18-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5b18-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5b18-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5b18-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a5b18-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a5b18-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="a5b18-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="a5b18-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a5b18-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a5b18-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="a5b18-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="a5b18-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="a5b18-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a5b18-125">Schema mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a5b18-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





