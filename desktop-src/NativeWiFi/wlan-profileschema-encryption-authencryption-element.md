---
description: Specifica il tipo di crittografia dei dati da utilizzare per la connessione a una LAN wireless.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Elemento Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129730"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="09e1a-103">Elemento Encryption (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="09e1a-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="09e1a-104">L'elemento Encryption (authEncryption) specifica il tipo di crittografia dei dati da utilizzare per la connessione a una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="09e1a-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="09e1a-105">L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="09e1a-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e1a-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="09e1a-106">Remarks</span></span>

<span data-ttu-id="09e1a-107">Quando l'elemento di **crittografia** ha un valore WEP, il [**tipo**](wlan-profileschema-keytype-sharedkey-element.md) di elemento deve essere impostato su **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="09e1a-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="09e1a-108">Il metodo di crittografia AES è come specificato nelle specifiche [802.1 x](https://ieeexplore.ieee.org/document/1438730) e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="09e1a-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="09e1a-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="09e1a-109">Examples</span></span>

<span data-ttu-id="09e1a-110">Per visualizzare i profili di esempio che usano l'elemento **Encryption** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="09e1a-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09e1a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09e1a-111">Requirements</span></span>



| <span data-ttu-id="09e1a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e1a-112">Requirement</span></span> | <span data-ttu-id="09e1a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="09e1a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="09e1a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e1a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="09e1a-115">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="09e1a-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="09e1a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e1a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="09e1a-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09e1a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="09e1a-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="09e1a-118">Redistributable</span></span><br/>          | <span data-ttu-id="09e1a-119">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="09e1a-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="09e1a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09e1a-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="09e1a-121">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="09e1a-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="09e1a-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="09e1a-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="09e1a-123">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="09e1a-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="09e1a-124">**authEncryption (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="09e1a-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




