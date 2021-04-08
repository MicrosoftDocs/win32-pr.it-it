---
description: Indica la modalità operativa della rete.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: Elemento connectionType (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879993"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="d5afa-103">Elemento connectionType (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="d5afa-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="d5afa-104">L'elemento connectionType (WLANProfile) indica la modalità operativa della rete.</span><span class="sxs-lookup"><span data-stu-id="d5afa-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="d5afa-105">Il valore **ESS** indica una rete di infrastruttura, mentre **IBSS** indica una rete ad hoc.</span><span class="sxs-lookup"><span data-stu-id="d5afa-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="d5afa-106">L'elemento **ConnectionType** è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d5afa-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d5afa-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="d5afa-107">Examples</span></span>

<span data-ttu-id="d5afa-108">Per visualizzare i profili di esempio che usano l'elemento **ConnectionType** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d5afa-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5afa-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5afa-109">Requirements</span></span>



| <span data-ttu-id="d5afa-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5afa-110">Requirement</span></span> | <span data-ttu-id="d5afa-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d5afa-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d5afa-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5afa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d5afa-113">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="d5afa-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d5afa-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5afa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d5afa-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5afa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d5afa-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d5afa-116">Redistributable</span></span><br/>          | <span data-ttu-id="d5afa-117">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="d5afa-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d5afa-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5afa-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5afa-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="d5afa-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d5afa-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d5afa-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d5afa-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="d5afa-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d5afa-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d5afa-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




