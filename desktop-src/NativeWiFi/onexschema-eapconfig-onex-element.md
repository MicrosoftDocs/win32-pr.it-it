---
description: Specifica la configurazione EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Elemento EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311675"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="fe8a3-103">Elemento EAPConfig (OneX)</span><span class="sxs-lookup"><span data-stu-id="fe8a3-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="fe8a3-104">L'elemento **EAPConfig** (Onex) specifica la configurazione EAPHost.</span><span class="sxs-lookup"><span data-stu-id="fe8a3-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="fe8a3-105">A differenza della maggior parte degli elementi nello schema del profilo 802.1 X, questo elemento si trova nello `https://www.microsoft.com/provisioning/EapHostConfig` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fe8a3-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="fe8a3-106">Gli elementi figlio sono definiti nello [schema eaphostconfig](../eaphost/eaphostconfigschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="fe8a3-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="fe8a3-107">L'elemento [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) è figlio dell'elemento **EAPConfig** .</span><span class="sxs-lookup"><span data-stu-id="fe8a3-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="fe8a3-108">L'elemento **EAPConfig** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8a3-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8a3-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe8a3-109">Requirements</span></span>



| <span data-ttu-id="fe8a3-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe8a3-110">Requirement</span></span> | <span data-ttu-id="fe8a3-111">Valore</span><span class="sxs-lookup"><span data-stu-id="fe8a3-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fe8a3-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe8a3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8a3-113">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="fe8a3-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe8a3-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe8a3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8a3-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe8a3-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fe8a3-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fe8a3-116">Redistributable</span></span><br/>          | <span data-ttu-id="fe8a3-117">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="fe8a3-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fe8a3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe8a3-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe8a3-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fe8a3-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fe8a3-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="fe8a3-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="fe8a3-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fe8a3-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fe8a3-122">**OneX**</span><span class="sxs-lookup"><span data-stu-id="fe8a3-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
