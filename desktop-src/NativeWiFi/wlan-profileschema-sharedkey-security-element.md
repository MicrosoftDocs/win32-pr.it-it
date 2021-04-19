---
description: Contiene informazioni sulla chiave condivisa.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Elemento sharedKey (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313322"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="b6543-103">Elemento sharedKey (Security)</span><span class="sxs-lookup"><span data-stu-id="b6543-103">sharedKey (security) Element</span></span>

<span data-ttu-id="b6543-104">L'elemento sharedKey (Security) contiene informazioni sulla chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="b6543-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="b6543-105">Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.</span><span class="sxs-lookup"><span data-stu-id="b6543-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
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

<span data-ttu-id="b6543-106">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b6543-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b6543-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b6543-107">Child elements</span></span>



| <span data-ttu-id="b6543-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6543-108">Element</span></span>                                                                 | <span data-ttu-id="b6543-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6543-109">Type</span></span>                                                              | <span data-ttu-id="b6543-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6543-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6543-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="b6543-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="b6543-112">string</span><span class="sxs-lookup"><span data-stu-id="b6543-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="b6543-113">Contiene la chiave di rete o la passphrase.</span><span class="sxs-lookup"><span data-stu-id="b6543-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="b6543-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="b6543-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="b6543-115">Tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="b6543-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="b6543-116">**protetto**</span><span class="sxs-lookup"><span data-stu-id="b6543-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="b6543-117">boolean</span><span class="sxs-lookup"><span data-stu-id="b6543-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="b6543-118">Indica se la chiave è crittografata.</span><span class="sxs-lookup"><span data-stu-id="b6543-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="b6543-119">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere FALSE.</span><span class="sxs-lookup"><span data-stu-id="b6543-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b6543-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6543-120">Remarks</span></span>

<span data-ttu-id="b6543-121">Per Windows Vista e Windows Server 2008, i dati associati all'elemento **sharedKey** vengono crittografati prima di essere salvati nell'archivio profili.</span><span class="sxs-lookup"><span data-stu-id="b6543-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="b6543-122">Per Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2, i dati non vengono crittografati.</span><span class="sxs-lookup"><span data-stu-id="b6543-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="b6543-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="b6543-123">Examples</span></span>

<span data-ttu-id="b6543-124">Per visualizzare i profili di esempio che usano l'elemento **sharedKey** , vedere esempio di [profilo non broadcast](non-broadcast-profile-sample.md), esempio di profilo [WPA-Personal](wpa-personal-profile-sample.md)e [esempio di profilo WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b6543-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6543-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6543-125">Requirements</span></span>



| <span data-ttu-id="b6543-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6543-126">Requirement</span></span> | <span data-ttu-id="b6543-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b6543-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b6543-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6543-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6543-129">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="b6543-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6543-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6543-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6543-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6543-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b6543-132">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b6543-132">Redistributable</span></span><br/>          | <span data-ttu-id="b6543-133">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="b6543-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b6543-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6543-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6543-135">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b6543-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b6543-136">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="b6543-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="b6543-137">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b6543-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b6543-138">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="b6543-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
