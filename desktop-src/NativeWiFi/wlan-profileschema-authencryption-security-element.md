---
description: Specifica la coppia di autenticazione e crittografia da usare per questo profilo.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Elemento authEncryption (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308890"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="b2302-103">Elemento authEncryption (Security)</span><span class="sxs-lookup"><span data-stu-id="b2302-103">authEncryption (security) Element</span></span>

<span data-ttu-id="b2302-104">L'elemento authEncryption (Security) specifica la coppia di autenticazione e crittografia da usare per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="b2302-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="useOneX"
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

<span data-ttu-id="b2302-105">L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b2302-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b2302-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b2302-106">Child elements</span></span>



| <span data-ttu-id="b2302-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b2302-107">Element</span></span>                                                                            | <span data-ttu-id="b2302-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2302-108">Type</span></span>                                                              | <span data-ttu-id="b2302-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2302-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2302-110">**autenticazione**</span><span class="sxs-lookup"><span data-stu-id="b2302-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="b2302-111">Specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="b2302-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="b2302-112">**crittografia**</span><span class="sxs-lookup"><span data-stu-id="b2302-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="b2302-113">Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="b2302-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="b2302-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="b2302-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="b2302-115">boolean</span><span class="sxs-lookup"><span data-stu-id="b2302-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="b2302-116">Indica se viene utilizzato 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="b2302-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="b2302-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2302-117">Remarks</span></span>

<span data-ttu-id="b2302-118">L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento **authEncryption** .</span><span class="sxs-lookup"><span data-stu-id="b2302-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="b2302-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="b2302-119">Examples</span></span>

<span data-ttu-id="b2302-120">Per visualizzare i profili di esempio che usano l'elemento **authEncryption** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b2302-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="b2302-121">Per visualizzare un profilo di esempio che usa l'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) , vedere [esempio di profilo FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="b2302-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2302-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2302-122">Requirements</span></span>



| <span data-ttu-id="b2302-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2302-123">Requirement</span></span> | <span data-ttu-id="b2302-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b2302-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b2302-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2302-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2302-126">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="b2302-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b2302-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2302-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2302-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2302-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="b2302-129">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b2302-129">Redistributable</span></span><br/>          | <span data-ttu-id="b2302-130">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="b2302-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b2302-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2302-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2302-132">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="b2302-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="b2302-133">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b2302-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b2302-134">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="b2302-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="b2302-135">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b2302-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b2302-136">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="b2302-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
