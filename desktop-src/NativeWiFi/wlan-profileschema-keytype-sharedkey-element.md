---
description: Indica se la chiave condivisa sarà una chiave di rete o una passphrase.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento Type (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312843"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="a72f8-103">Elemento Type (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="a72f8-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="a72f8-104">L'elemento Key Type (sharedKey) indica se la chiave condivisa sarà una chiave di rete o una passphrase.</span><span class="sxs-lookup"><span data-stu-id="a72f8-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a72f8-105">L'elemento è definito dall'elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a72f8-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a72f8-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="a72f8-106">Remarks</span></span>

<span data-ttu-id="a72f8-107">Quando l'elemento di [**crittografia**](wlan-profileschema-encryption-authencryption-element.md) ha un valore WEP, il **tipo** di elemento deve essere impostato su **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="a72f8-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="a72f8-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="a72f8-108">Examples</span></span>

<span data-ttu-id="a72f8-109">Per visualizzare i profili di esempio che usano l'elemento di **tipo** , vedere esempio di [profilo non broadcast](non-broadcast-profile-sample.md), esempio di profilo [WPA-Personal](wpa-personal-profile-sample.md)e [esempio di profilo WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a72f8-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a72f8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a72f8-110">Requirements</span></span>



| <span data-ttu-id="a72f8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a72f8-111">Requirement</span></span> | <span data-ttu-id="a72f8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a72f8-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a72f8-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a72f8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a72f8-114">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a72f8-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a72f8-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a72f8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a72f8-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a72f8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a72f8-117">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a72f8-117">Redistributable</span></span><br/>          | <span data-ttu-id="a72f8-118">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="a72f8-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a72f8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a72f8-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="a72f8-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a72f8-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a72f8-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a72f8-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="a72f8-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a72f8-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a72f8-123">**sharedKey (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="a72f8-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




