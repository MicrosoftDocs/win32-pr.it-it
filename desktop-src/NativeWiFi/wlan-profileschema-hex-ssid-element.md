---
description: Contiene l'SSID di una LAN wireless in formato esadecimale.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Hex (SSID) (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307828"
---
# <a name="hex-ssid-element"></a><span data-ttu-id="9fc52-103">Hex (SSID) (elemento)</span><span class="sxs-lookup"><span data-stu-id="9fc52-103">hex (SSID) Element</span></span>

<span data-ttu-id="9fc52-104">L'elemento esadecimale (SSID) contiene l'SSID di una LAN wireless in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="9fc52-104">The hex (SSID) element contains the SSID of a wireless LAN in hexadecimal format.</span></span>

``` syntax
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
```

<span data-ttu-id="9fc52-105">L'elemento è definito dall'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc52-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc52-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fc52-106">Remarks</span></span>

<span data-ttu-id="9fc52-107">Anche se gli elementi **Hex** e [**Name**](wlan-profileschema-name-ssid-element.md) sono facoltativi, è necessario che almeno un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) venga visualizzato come figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9fc52-107">Although the **hex** and [**name**](wlan-profileschema-name-ssid-element.md) elements are optional, at least one **hex** or [**name**](wlan-profileschema-name-ssid-element.md) element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="9fc52-108">Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento **Hex** viene convertito nell'SSID (se presente) e l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9fc52-108">When profile information is converted to an SSID, the **hex** element is converted to the SSID (if present) and the [**name**](wlan-profileschema-name-ssid-element.md) element is ignored .</span></span> <span data-ttu-id="9fc52-109">Se l'elemento **esadecimale** non è presente, l'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene convertito in un SSID mediante la conversione da Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="9fc52-109">If the **hex** element is not present, the [**name**](wlan-profileschema-name-ssid-element.md) element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="9fc52-110">Quando un SSID viene archiviato in un profilo, l'elemento **esadecimale** viene sempre generato.</span><span class="sxs-lookup"><span data-stu-id="9fc52-110">When an SSID is stored in a profile, the **hex** element is always generated.</span></span> <span data-ttu-id="9fc52-111">L'elemento [**Name**](wlan-profileschema-name-ssid-element.md) viene generato solo se la conversione da ASCII a Unicode del SSID e della generazione del profilo XML ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9fc52-111">The [**name**](wlan-profileschema-name-ssid-element.md) element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="9fc52-112">Alcune informazioni provenienti dall'SSID originale potrebbero andare perse quando vengono convertite in un [**nome**](wlan-profileschema-name-ssid-element.md).</span><span class="sxs-lookup"><span data-stu-id="9fc52-112">Some information from the original SSID may be lost when it is converted to a [**name**](wlan-profileschema-name-ssid-element.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9fc52-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fc52-113">Examples</span></span>

<span data-ttu-id="9fc52-114">Per visualizzare un profilo di esempio che usa l'elemento **esadecimale** , vedere [esempio di profilo FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9fc52-114">To view a sample profile that uses the **hex** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc52-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fc52-115">Requirements</span></span>



| <span data-ttu-id="9fc52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc52-116">Requirement</span></span> | <span data-ttu-id="9fc52-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9fc52-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9fc52-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc52-119">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="9fc52-119">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9fc52-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc52-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fc52-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="9fc52-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9fc52-122">Redistributable</span></span><br/>          | <span data-ttu-id="9fc52-123">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="9fc52-123">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9fc52-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fc52-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fc52-125">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="9fc52-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc52-126">**SSID**</span><span class="sxs-lookup"><span data-stu-id="9fc52-126">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="9fc52-127">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="9fc52-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc52-128">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="9fc52-128">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




