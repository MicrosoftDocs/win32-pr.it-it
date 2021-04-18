---
description: Specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Elemento AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306781"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="05f26-103">Elemento AuthProtocol (contextType)</span><span class="sxs-lookup"><span data-stu-id="05f26-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="05f26-104">L'elemento **AuthProtocol (ContextType)** specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="05f26-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="05f26-105">L'elemento può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="05f26-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="05f26-106">Valore</span><span class="sxs-lookup"><span data-stu-id="05f26-106">Value</span></span>      | <span data-ttu-id="05f26-107">Significato</span><span class="sxs-lookup"><span data-stu-id="05f26-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="05f26-108">NESSUNO</span><span class="sxs-lookup"><span data-stu-id="05f26-108">"NONE"</span></span>     | <span data-ttu-id="05f26-109">Nessun protocollo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="05f26-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="05f26-110">PAP</span><span class="sxs-lookup"><span data-stu-id="05f26-110">"PAP"</span></span>      | <span data-ttu-id="05f26-111">Autenticazione della password non crittografata.</span><span class="sxs-lookup"><span data-stu-id="05f26-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="05f26-112">CHAP</span><span class="sxs-lookup"><span data-stu-id="05f26-112">"CHAP"</span></span>     | <span data-ttu-id="05f26-113">Challenge Handshake Authentication Protocol (CHAP).</span><span class="sxs-lookup"><span data-stu-id="05f26-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="05f26-114">MsCHAPV2</span><span class="sxs-lookup"><span data-stu-id="05f26-114">MsCHAPV2"</span></span> | <span data-ttu-id="05f26-115">Usare Microsoft Challenge Handshake Authentication Protocol (CHAP) v 2.0.</span><span class="sxs-lookup"><span data-stu-id="05f26-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="05f26-116">Questo elemento è facoltativo e viene usato solo per i profili GSM.</span><span class="sxs-lookup"><span data-stu-id="05f26-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="05f26-117">Se l'elemento non è specificato e il profilo è per un dispositivo GSM, il servizio Mobile Broadband userà **"None"**.</span><span class="sxs-lookup"><span data-stu-id="05f26-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="05f26-118">L'elemento **AuthProtocol** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="05f26-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f26-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05f26-119">Requirements</span></span>



| <span data-ttu-id="05f26-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f26-120">Requirement</span></span> | <span data-ttu-id="05f26-121">Valore</span><span class="sxs-lookup"><span data-stu-id="05f26-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="05f26-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05f26-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05f26-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="05f26-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="05f26-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05f26-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05f26-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="05f26-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="05f26-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05f26-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="05f26-127">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="05f26-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="05f26-128">**contextType**</span><span class="sxs-lookup"><span data-stu-id="05f26-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="05f26-129">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="05f26-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="05f26-130">**Contesto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="05f26-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




