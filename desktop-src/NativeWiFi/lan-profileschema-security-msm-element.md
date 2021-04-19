---
description: Contiene le impostazioni di sicurezza per le reti cablate.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Elemento Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323790"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="108ce-103">Elemento Security (MSM) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="108ce-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="108ce-104">L'elemento Security (MSM) contiene le impostazioni di sicurezza per le reti cablate.</span><span class="sxs-lookup"><span data-stu-id="108ce-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="108ce-105">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="108ce-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="108ce-106">L'elemento di **sicurezza** è definito dall'elemento [**MSM**](lan-profileschema-msm-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="108ce-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="108ce-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="108ce-107">Child elements</span></span>



| <span data-ttu-id="108ce-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="108ce-108">Element</span></span>                                                                 | <span data-ttu-id="108ce-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="108ce-109">Type</span></span>    | <span data-ttu-id="108ce-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="108ce-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="108ce-111">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="108ce-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="108ce-112">boolean</span><span class="sxs-lookup"><span data-stu-id="108ce-112">boolean</span></span> | <span data-ttu-id="108ce-113">Specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="108ce-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="108ce-114">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="108ce-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="108ce-115">boolean</span><span class="sxs-lookup"><span data-stu-id="108ce-115">boolean</span></span> | <span data-ttu-id="108ce-116">Specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 X per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="108ce-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="108ce-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="108ce-117">Requirements</span></span>



| <span data-ttu-id="108ce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="108ce-118">Requirement</span></span> | <span data-ttu-id="108ce-119">Valore</span><span class="sxs-lookup"><span data-stu-id="108ce-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="108ce-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108ce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="108ce-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="108ce-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="108ce-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108ce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="108ce-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="108ce-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="108ce-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="108ce-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="108ce-125">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="108ce-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="108ce-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="108ce-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="108ce-127">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="108ce-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="108ce-128">**CSM (LANProfile)**</span><span class="sxs-lookup"><span data-stu-id="108ce-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




