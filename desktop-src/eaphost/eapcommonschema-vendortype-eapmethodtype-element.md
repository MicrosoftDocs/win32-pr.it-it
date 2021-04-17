---
title: Elemento VendorType (EapMethodType)
description: Informazioni sull'elemento VendorType (EapMethodType). Questo elemento è il tipo definito dal fornitore per il metodo.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorType EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474219"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="d5672-105">Elemento VendorType (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="d5672-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="d5672-106">L'elemento **VendorType (EapMethodType)** è il tipo definito dal fornitore per il metodo.</span><span class="sxs-lookup"><span data-stu-id="d5672-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="d5672-107">L'elemento **VendorType** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d5672-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="d5672-108">Se usato, **VendorType** è un numero univoco emesso da IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="d5672-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="d5672-109">L'elemento **VendorType** è definito dal tipo complesso [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d5672-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5672-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5672-110">Requirements</span></span>



| <span data-ttu-id="d5672-111">Ruolo</span><span class="sxs-lookup"><span data-stu-id="d5672-111">Role</span></span> | <span data-ttu-id="d5672-112">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="d5672-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="d5672-113">Client</span><span class="sxs-lookup"><span data-stu-id="d5672-113">Client</span></span><br/> | <span data-ttu-id="d5672-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5672-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d5672-115">Server</span><span class="sxs-lookup"><span data-stu-id="d5672-115">Server</span></span><br/> | <span data-ttu-id="d5672-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5672-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5672-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5672-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5672-118">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d5672-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d5672-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="d5672-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="d5672-120">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="d5672-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d5672-121">Schema eapcommon</span><span class="sxs-lookup"><span data-stu-id="d5672-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





