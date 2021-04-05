---
description: Contiene un SSID per una LAN wireless.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Elemento SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882674"
---
# <a name="ssid-ssidconfig-element"></a><span data-ttu-id="e978c-103">Elemento SSID (SSIDConfig)</span><span class="sxs-lookup"><span data-stu-id="e978c-103">SSID (SSIDConfig) Element</span></span>

<span data-ttu-id="e978c-104">L'elemento SSID (SSIDConfig) contiene un SSID per una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="e978c-104">The SSID (SSIDConfig) element contains an SSID for a wireless LAN.</span></span>

<span data-ttu-id="e978c-105">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** In un profilo può essere presente al massimo un elemento **SSID** .</span><span class="sxs-lookup"><span data-stu-id="e978c-105">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one **SSID** element can appear in a profile.</span></span>

``` syntax
<xs:element name="SSID"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="hex"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="32"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="name"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="32"
                         />
                    </xs:restriction>
                </xs:simpleType>
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

<span data-ttu-id="e978c-106">L'elemento **SSID** viene definito dall'elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e978c-106">The **SSID** element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e978c-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e978c-107">Child elements</span></span>



| <span data-ttu-id="e978c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e978c-108">Element</span></span>                                              | <span data-ttu-id="e978c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e978c-109">Type</span></span> | <span data-ttu-id="e978c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e978c-110">Description</span></span>                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [<span data-ttu-id="e978c-111">**hex**</span><span class="sxs-lookup"><span data-stu-id="e978c-111">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)   |      | <span data-ttu-id="e978c-112">Contiene l'SSID di una LAN wireless in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="e978c-112">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/> |
| [<span data-ttu-id="e978c-113">**nome**</span><span class="sxs-lookup"><span data-stu-id="e978c-113">**name**</span></span>](wlan-profileschema-name-ssid-element.md) |      | <span data-ttu-id="e978c-114">Contiene l'SSID per una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="e978c-114">Contains the SSID for a wireless LAN.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="e978c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e978c-115">Remarks</span></span>

<span data-ttu-id="e978c-116">Anche se gli elementi [**Hex**](wlan-profileschema-hex-ssid-element.md) e [**Name**](wlan-profileschema-name-ssid-element.md) sono facoltativi, è necessario che almeno un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) venga visualizzato come figlio dell'elemento **SSID** .</span><span class="sxs-lookup"><span data-stu-id="e978c-116">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the **SSID** element.</span></span>

<span data-ttu-id="e978c-117">Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) viene convertito nell'SSID (se presente) e l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e978c-117">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored.</span></span> <span data-ttu-id="e978c-118">Se l'elemento **esadecimale** non è presente, l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene convertito in un SSID mediante la conversione da Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="e978c-118">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="e978c-119">Quando un SSID viene archiviato in un profilo, l'elemento [**esadecimale**](wlan-profileschema-hex-ssid-element.md) viene sempre generato.</span><span class="sxs-lookup"><span data-stu-id="e978c-119">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="e978c-120">L'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene generato solo se la conversione da ASCII a Unicode del SSID e della generazione del profilo XML ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e978c-120">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="e978c-121">Alcune informazioni provenienti dall'SSID originale potrebbero andare perse quando vengono convertite in un [**nome**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="e978c-121">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e978c-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="e978c-122">Examples</span></span>

<span data-ttu-id="e978c-123">Per visualizzare i profili di esempio che usano l'elemento **SSID** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e978c-123">To view sample profiles that use the **SSID** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e978c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e978c-124">Requirements</span></span>



| <span data-ttu-id="e978c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e978c-125">Requirement</span></span> | <span data-ttu-id="e978c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e978c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="e978c-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e978c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e978c-128">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="e978c-128">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e978c-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e978c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e978c-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e978c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e978c-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e978c-131">Redistributable</span></span><br/>          | <span data-ttu-id="e978c-132">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="e978c-132">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e978c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e978c-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="e978c-134">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="e978c-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e978c-135">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="e978c-135">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="e978c-136">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="e978c-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e978c-137">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="e978c-137">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




