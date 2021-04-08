---
description: Contiene uno o più SSID per le reti LAN wireless.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Elemento SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882382"
---
# <a name="ssidconfig-wlanprofile-element"></a><span data-ttu-id="c2163-103">Elemento SSIDConfig (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="c2163-103">SSIDConfig (WLANProfile) Element</span></span>

<span data-ttu-id="c2163-104">L'elemento SSIDConfig (WLANProfile) contiene uno o più SSID per le reti LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="c2163-104">The SSIDConfig (WLANProfile) element contains one or more SSIDs for wireless LANs.</span></span>

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="nonBroadcast"
                type="boolean"
                minOccurs="0"
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

<span data-ttu-id="c2163-105">L'elemento **SSIDConfig** è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c2163-105">The **SSIDConfig** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c2163-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c2163-106">Child elements</span></span>



| <span data-ttu-id="c2163-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c2163-107">Element</span></span>                                                                    | <span data-ttu-id="c2163-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2163-108">Type</span></span>                                                              | <span data-ttu-id="c2163-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2163-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2163-110">**hex**</span><span class="sxs-lookup"><span data-stu-id="c2163-110">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | <span data-ttu-id="c2163-111">Contiene l'SSID di una LAN wireless in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="c2163-111">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c2163-112">**nome**</span><span class="sxs-lookup"><span data-stu-id="c2163-112">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                       |                                                                   | <span data-ttu-id="c2163-113">Contiene il nome del SSID di una LAN senza fili (maiuscole/minuscole).</span><span class="sxs-lookup"><span data-stu-id="c2163-113">Contains the (case-sensitive) name of the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c2163-114">**nonBroadcast**</span><span class="sxs-lookup"><span data-stu-id="c2163-114">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [<span data-ttu-id="c2163-115">boolean</span><span class="sxs-lookup"><span data-stu-id="c2163-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="c2163-116">Indica se la rete trasmette il relativo SSID.</span><span class="sxs-lookup"><span data-stu-id="c2163-116">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="c2163-117">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su ESS, questo valore può essere **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="c2163-117">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either **TRUE** or **FALSE**.</span></span> <span data-ttu-id="c2163-118">Il valore predefinito è **true** se questo elemento è assente.</span><span class="sxs-lookup"><span data-stu-id="c2163-118">The default value is **TRUE** if this element is absent.</span></span><br/> <span data-ttu-id="c2163-119">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su IBSS, questo valore deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="c2163-119">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be **FALSE**.</span></span><br/> <span data-ttu-id="c2163-120">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c2163-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="c2163-121">**SSID**</span><span class="sxs-lookup"><span data-stu-id="c2163-121">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | <span data-ttu-id="c2163-122">Contiene un SSID per una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="c2163-122">Contains an SSID for a wireless LAN.</span></span><br/> <span data-ttu-id="c2163-123">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** In un profilo può essere presente al massimo un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c2163-123">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a><span data-ttu-id="c2163-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2163-124">Examples</span></span>

<span data-ttu-id="c2163-125">Per visualizzare i profili di esempio che usano l'elemento **SSIDConfig** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="c2163-125">To view sample profiles that use the **SSIDConfig** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2163-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2163-126">Requirements</span></span>



| <span data-ttu-id="c2163-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2163-127">Requirement</span></span> | <span data-ttu-id="c2163-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c2163-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="c2163-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2163-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2163-130">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c2163-130">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2163-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2163-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2163-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2163-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="c2163-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c2163-133">Redistributable</span></span><br/>          | <span data-ttu-id="c2163-134">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="c2163-134">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c2163-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2163-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2163-136">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="c2163-136">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c2163-137">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="c2163-137">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="c2163-138">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="c2163-138">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c2163-139">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="c2163-139">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
