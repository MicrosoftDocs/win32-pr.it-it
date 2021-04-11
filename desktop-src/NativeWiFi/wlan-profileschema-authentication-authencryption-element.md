---
description: Specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Authentication (authEncryption)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226489"
---
# <a name="authentication-authencryption-element"></a><span data-ttu-id="fe80d-103">Authentication (authEncryption)-elemento</span><span class="sxs-lookup"><span data-stu-id="fe80d-103">authentication (authEncryption) Element</span></span>

<span data-ttu-id="fe80d-104">L'elemento Authentication (authEncryption) specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="fe80d-104">The authentication (authEncryption) element specifies the authentication method to be used to connect to the wireless LAN.</span></span>

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="fe80d-105">L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fe80d-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe80d-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe80d-106">Remarks</span></span>

<span data-ttu-id="fe80d-107">Nella tabella seguente vengono descritti i valori di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="fe80d-107">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="fe80d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="fe80d-108">Value</span></span>   | <span data-ttu-id="fe80d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe80d-109">Description</span></span>                            |
|---------|----------------------------------------|
| <span data-ttu-id="fe80d-110">apre</span><span class="sxs-lookup"><span data-stu-id="fe80d-110">open</span></span>    | <span data-ttu-id="fe80d-111">Aprire l'autenticazione 802,11.</span><span class="sxs-lookup"><span data-stu-id="fe80d-111">Open 802.11 authentication.</span></span>            |
| <span data-ttu-id="fe80d-112">shared</span><span class="sxs-lookup"><span data-stu-id="fe80d-112">shared</span></span>  | <span data-ttu-id="fe80d-113">Autenticazione 802,11 condivisa.</span><span class="sxs-lookup"><span data-stu-id="fe80d-113">Shared 802.11 authentication.</span></span>          |
| <span data-ttu-id="fe80d-114">WPA</span><span class="sxs-lookup"><span data-stu-id="fe80d-114">WPA</span></span>     | <span data-ttu-id="fe80d-115">Autenticazione WPA-Enterprise 802,11.</span><span class="sxs-lookup"><span data-stu-id="fe80d-115">WPA-Enterprise 802.11 authentication.</span></span>  |
| <span data-ttu-id="fe80d-116">WPAPSK</span><span class="sxs-lookup"><span data-stu-id="fe80d-116">WPAPSK</span></span>  | <span data-ttu-id="fe80d-117">Autenticazione WPA-Personal 802,11.</span><span class="sxs-lookup"><span data-stu-id="fe80d-117">WPA-Personal 802.11 authentication.</span></span>    |
| <span data-ttu-id="fe80d-118">WPA2</span><span class="sxs-lookup"><span data-stu-id="fe80d-118">WPA2</span></span>    | <span data-ttu-id="fe80d-119">Autenticazione WPA2-Enterprise 802,11.</span><span class="sxs-lookup"><span data-stu-id="fe80d-119">WPA2-Enterprise 802.11 authentication.</span></span> |
| <span data-ttu-id="fe80d-120">WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="fe80d-120">WPA2PSK</span></span> | <span data-ttu-id="fe80d-121">Autenticazione WPA2-Personal 802,11.</span><span class="sxs-lookup"><span data-stu-id="fe80d-121">WPA2-Personal 802.11 authentication.</span></span>   |



 

<span data-ttu-id="fe80d-122">Per ulteriori informazioni sui metodi di autenticazione 802,11, vedere le specifiche [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="fe80d-122">For more information about 802.11 authentication methods, see the [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730), and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="fe80d-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe80d-123">Examples</span></span>

<span data-ttu-id="fe80d-124">Per visualizzare i profili di esempio che usano l'elemento **Authentication** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="fe80d-124">To view sample profiles that use the **authentication** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe80d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe80d-125">Requirements</span></span>



| <span data-ttu-id="fe80d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe80d-126">Requirement</span></span> | <span data-ttu-id="fe80d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fe80d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fe80d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe80d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fe80d-129">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="fe80d-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe80d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe80d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fe80d-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe80d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fe80d-132">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fe80d-132">Redistributable</span></span><br/>          | <span data-ttu-id="fe80d-133">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="fe80d-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fe80d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe80d-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe80d-135">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fe80d-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fe80d-136">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="fe80d-136">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="fe80d-137">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fe80d-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fe80d-138">**authEncryption (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="fe80d-138">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




