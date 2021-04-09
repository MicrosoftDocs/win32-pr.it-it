---
title: Elemento autorizzato (EapMethodType)
description: Informazioni sull'elemento autorizzato (EapMethodType). L'elemento autorizzato (EapMethodType) si riferisce all'autore del metodo.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento autorizzato EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963466"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="1b3e5-105">Elemento autorizzato (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="1b3e5-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="1b3e5-106">L'elemento autorizzato **(EapMethodType)** si riferisce all'autore del metodo.</span><span class="sxs-lookup"><span data-stu-id="1b3e5-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="1b3e5-107">L'autorizzazione è un numero univoco emesso da IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="1b3e5-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="1b3e5-108">L'elemento **autorizzato** è definito dal tipo complesso [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1b3e5-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b3e5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b3e5-109">Remarks</span></span>

<span data-ttu-id="1b3e5-110">Gli elementi **autorizzazioned** e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) non devono essere uguali per un metodo specifico.</span><span class="sxs-lookup"><span data-stu-id="1b3e5-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3e5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b3e5-111">Requirements</span></span>



| <span data-ttu-id="1b3e5-112">Ruolo</span><span class="sxs-lookup"><span data-stu-id="1b3e5-112">Role</span></span> | <span data-ttu-id="1b3e5-113">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="1b3e5-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="1b3e5-114">Client</span><span class="sxs-lookup"><span data-stu-id="1b3e5-114">Client</span></span><br/> | <span data-ttu-id="1b3e5-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b3e5-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b3e5-116">Server</span><span class="sxs-lookup"><span data-stu-id="1b3e5-116">Server</span></span><br/> | <span data-ttu-id="1b3e5-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b3e5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b3e5-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b3e5-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b3e5-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="1b3e5-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1b3e5-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="1b3e5-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="1b3e5-121">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="1b3e5-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1b3e5-122">Schema eapcommon</span><span class="sxs-lookup"><span data-stu-id="1b3e5-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





