---
title: Elemento SimpleCertSelection (CertSelection)
description: Informazioni sull'elemento SimpleCertSelection (CertSelection). Questo elemento determina il modo in cui l'utente seleziona un certificato.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Elemento SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047373"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="2e8ac-105">Elemento SimpleCertSelection (CertSelection)</span><span class="sxs-lookup"><span data-stu-id="2e8ac-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="2e8ac-106">L'elemento **SimpleCertSelection (CertSelection)** determina il modo in cui l'utente seleziona un certificato.</span><span class="sxs-lookup"><span data-stu-id="2e8ac-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="2e8ac-107">L'elemento **SimpleCertSelection** è definito dal tipo complesso [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2e8ac-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e8ac-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e8ac-108">Remarks</span></span>

<span data-ttu-id="2e8ac-109">Per impostazione predefinita, **SimpleCertSelection** è true.</span><span class="sxs-lookup"><span data-stu-id="2e8ac-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="2e8ac-110">Se **SimpleCertSelection** è true, EAP-TLS esegue una semplice ricerca di certificati senza elenchi a discesa per la selezione dei certificati.</span><span class="sxs-lookup"><span data-stu-id="2e8ac-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="2e8ac-111">Se **SimpleCertSelection** è false, EAP-TLS illustra all'utente il certificato appropriato da selezionare.</span><span class="sxs-lookup"><span data-stu-id="2e8ac-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e8ac-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e8ac-112">Requirements</span></span>



| <span data-ttu-id="2e8ac-113">Ruolo</span><span class="sxs-lookup"><span data-stu-id="2e8ac-113">Role</span></span> | <span data-ttu-id="2e8ac-114">Sistema operativo minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e8ac-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="2e8ac-115">Client</span><span class="sxs-lookup"><span data-stu-id="2e8ac-115">Client</span></span><br/> | <span data-ttu-id="2e8ac-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e8ac-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2e8ac-117">Server</span><span class="sxs-lookup"><span data-stu-id="2e8ac-117">Server</span></span><br/> | <span data-ttu-id="2e8ac-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e8ac-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e8ac-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e8ac-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="2e8ac-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="2e8ac-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2e8ac-121">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="2e8ac-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="2e8ac-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="2e8ac-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2e8ac-123">**CertificateStore (CredentialsSourceParameters)**</span><span class="sxs-lookup"><span data-stu-id="2e8ac-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="2e8ac-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2e8ac-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2e8ac-125">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="2e8ac-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2e8ac-126">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2e8ac-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2e8ac-127">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2e8ac-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





