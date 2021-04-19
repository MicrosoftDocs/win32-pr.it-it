---
description: Specifica le informazioni di configurazione di rete Single Sign-On (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Elemento singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311666"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="b5ae3-103">Elemento singleSignOn (OneX)</span><span class="sxs-lookup"><span data-stu-id="b5ae3-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="b5ae3-104">L'elemento singleSignOn (OneX) specifica le informazioni di configurazione di rete Single Sign-On (SSO).</span><span class="sxs-lookup"><span data-stu-id="b5ae3-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="b5ae3-105">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-105">This element is optional.</span></span> <span data-ttu-id="b5ae3-106">Non usare l'elemento singleSignOn in un profilo se la rete non lo richiede.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="b5ae3-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="b5ae3-108">L'elemento **singleSignOn** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b5ae3-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b5ae3-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b5ae3-109">Child elements</span></span>



| <span data-ttu-id="b5ae3-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b5ae3-110">Element</span></span>                                                                            | <span data-ttu-id="b5ae3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5ae3-111">Type</span></span>    | <span data-ttu-id="b5ae3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5ae3-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5ae3-113">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="b5ae3-114">Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione del Single Sign-On abbia esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="b5ae3-115">**tipo**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="b5ae3-116">Specifica quando Single Sign-On viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="b5ae3-117">Se impostata su `preLogon` , Single Sign-on viene eseguita prima dell'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="b5ae3-118">Quando è impostata su `postLogon` , Single Sign-on viene eseguita immediatamente dopo l'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="b5ae3-119">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="b5ae3-120">boolean</span><span class="sxs-lookup"><span data-stu-id="b5ae3-120">boolean</span></span> | <span data-ttu-id="b5ae3-121">Specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b5ae3-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="b5ae3-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5ae3-122">Remarks</span></span>

<span data-ttu-id="b5ae3-123">Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="b5ae3-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="b5ae3-124">Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b5ae3-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ae3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5ae3-125">Requirements</span></span>



| <span data-ttu-id="b5ae3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ae3-126">Requirement</span></span> | <span data-ttu-id="b5ae3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b5ae3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5ae3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5ae3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ae3-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5ae3-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b5ae3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5ae3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ae3-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5ae3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5ae3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5ae3-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5ae3-133">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b5ae3-134">**OneX**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="b5ae3-135">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b5ae3-136">**OneX**</span><span class="sxs-lookup"><span data-stu-id="b5ae3-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
