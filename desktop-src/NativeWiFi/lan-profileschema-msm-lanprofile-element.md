---
description: Contiene le impostazioni CSM (media-Specific Module).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Elemento MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232428"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="05812-103">Elemento MSM (LANProfile)</span><span class="sxs-lookup"><span data-stu-id="05812-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="05812-104">L'elemento MSM (LANProfile) contiene le impostazioni CSM (media-Specific Module).</span><span class="sxs-lookup"><span data-stu-id="05812-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
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

<span data-ttu-id="05812-105">L'elemento **MSM** è definito dall'elemento [**LANProfile**](lan-profileschema-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="05812-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="05812-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="05812-106">Child elements</span></span>



| <span data-ttu-id="05812-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="05812-107">Element</span></span>                                                                 | <span data-ttu-id="05812-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="05812-108">Type</span></span>    | <span data-ttu-id="05812-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05812-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05812-110">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="05812-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="05812-111">boolean</span><span class="sxs-lookup"><span data-stu-id="05812-111">boolean</span></span> | <span data-ttu-id="05812-112">Specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="05812-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="05812-113">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="05812-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="05812-114">boolean</span><span class="sxs-lookup"><span data-stu-id="05812-114">boolean</span></span> | <span data-ttu-id="05812-115">Specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 X per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="05812-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="05812-116">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="05812-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="05812-117">Contiene le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="05812-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="05812-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05812-118">Requirements</span></span>



| <span data-ttu-id="05812-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="05812-119">Requirement</span></span> | <span data-ttu-id="05812-120">Valore</span><span class="sxs-lookup"><span data-stu-id="05812-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05812-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05812-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05812-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05812-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05812-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05812-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05812-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05812-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05812-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05812-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="05812-126">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="05812-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="05812-127">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="05812-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="05812-128">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="05812-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="05812-129">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="05812-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




