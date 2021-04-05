---
description: Contiene l'SSID di una LAN wireless.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Elemento Name (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883922"
---
# <a name="name-ssid-element"></a><span data-ttu-id="0e0de-103">Elemento Name (SSID)</span><span class="sxs-lookup"><span data-stu-id="0e0de-103">name (SSID) Element</span></span>

<span data-ttu-id="0e0de-104">L'elemento Name (SSID) contiene il valore SSID di una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="0e0de-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
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
```

<span data-ttu-id="0e0de-105">L'elemento è definito dall'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0e0de-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e0de-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e0de-106">Remarks</span></span>

<span data-ttu-id="0e0de-107">I nomi fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0e0de-107">Names are case-sensitive.</span></span>

<span data-ttu-id="0e0de-108">Anche se gli elementi [**Hex**](wlan-profileschema-hex-ssid-element.md) e **Name** sono facoltativi, è necessario che almeno un elemento **Hex** o **Name** venga visualizzato come figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0e0de-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="0e0de-109">Quando le informazioni sul profilo vengono convertite in un SSID, l'elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) viene convertito nell'SSID (se presente) e l'elemento **Name** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0e0de-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="0e0de-110">Se l'elemento **esadecimale** non è presente, l'elemento **Name** viene convertito in un SSID mediante la conversione da Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="0e0de-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="0e0de-111">Quando un SSID viene archiviato in un profilo, l'elemento [**esadecimale**](wlan-profileschema-hex-ssid-element.md) viene sempre generato.</span><span class="sxs-lookup"><span data-stu-id="0e0de-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="0e0de-112">L'elemento **Name** viene generato solo se la conversione da ASCII a Unicode del SSID e della generazione del profilo XML ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e0de-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="0e0de-113">Alcune informazioni provenienti dall'SSID originale potrebbero andare perse quando vengono convertite in un **nome**.</span><span class="sxs-lookup"><span data-stu-id="0e0de-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="0e0de-114">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** I caratteri di escape XML, ad esempio &, non vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="0e0de-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="0e0de-115">Evitare di utilizzare caratteri di escape XML nei nomi SSID per i profili distribuiti in Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="0e0de-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="0e0de-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e0de-116">Examples</span></span>

<span data-ttu-id="0e0de-117">Per visualizzare i profili di esempio che usano l'elemento **Name** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0e0de-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e0de-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e0de-118">Requirements</span></span>



| <span data-ttu-id="0e0de-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e0de-119">Requirement</span></span> | <span data-ttu-id="0e0de-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0e0de-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="0e0de-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e0de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e0de-122">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="0e0de-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e0de-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e0de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e0de-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e0de-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="0e0de-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="0e0de-125">Redistributable</span></span><br/>          | <span data-ttu-id="0e0de-126">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="0e0de-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0e0de-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e0de-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e0de-128">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="0e0de-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0e0de-129">**SSID**</span><span class="sxs-lookup"><span data-stu-id="0e0de-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="0e0de-130">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="0e0de-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0e0de-131">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="0e0de-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




