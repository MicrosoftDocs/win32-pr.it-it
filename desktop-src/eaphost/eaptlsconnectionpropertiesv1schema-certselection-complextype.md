---
title: Tipo complesso CertSelection
description: Informazioni sul tipo complesso CertSelection. Questo tipo determina il modo in cui l'utente seleziona un certificato.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339262"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="a8da3-105">Tipo complesso CertSelection</span><span class="sxs-lookup"><span data-stu-id="a8da3-105">CertSelection Complex Type</span></span>

<span data-ttu-id="a8da3-106">Il tipo complesso **CertSelection** determina il modo in cui l'utente seleziona un certificato.</span><span class="sxs-lookup"><span data-stu-id="a8da3-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a8da3-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a8da3-107">Child elements</span></span>



| <span data-ttu-id="a8da3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8da3-108">Element</span></span>                                                                                                     | <span data-ttu-id="a8da3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8da3-109">Type</span></span>    | <span data-ttu-id="a8da3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8da3-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8da3-111">**SimpleCertSelection**</span><span class="sxs-lookup"><span data-stu-id="a8da3-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="a8da3-112">boolean</span><span class="sxs-lookup"><span data-stu-id="a8da3-112">boolean</span></span> | <span data-ttu-id="a8da3-113">È TRUE per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8da3-113">Is TRUE by default.</span></span> <span data-ttu-id="a8da3-114">Se [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) è true, EAP-TLS esegue una semplice ricerca di certificati senza elenchi a discesa per la selezione dei certificati.</span><span class="sxs-lookup"><span data-stu-id="a8da3-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="a8da3-115">Se **SimpleCertSelection** è false, EAP-TLS illustra all'utente il certificato appropriato da selezionare.</span><span class="sxs-lookup"><span data-stu-id="a8da3-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a8da3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8da3-116">Requirements</span></span>



| <span data-ttu-id="a8da3-117">Ruolo</span><span class="sxs-lookup"><span data-stu-id="a8da3-117">Role</span></span> | <span data-ttu-id="a8da3-118">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="a8da3-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="a8da3-119">Client</span><span class="sxs-lookup"><span data-stu-id="a8da3-119">Client</span></span><br/> | <span data-ttu-id="a8da3-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8da3-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8da3-121">Server</span><span class="sxs-lookup"><span data-stu-id="a8da3-121">Server</span></span><br/> | <span data-ttu-id="a8da3-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8da3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8da3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8da3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8da3-124">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="a8da3-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a8da3-125">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a8da3-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a8da3-126">Tipi complessi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="a8da3-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





