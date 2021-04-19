---
description: Specifica le informazioni di configurazione 802.1 X per un profilo LAN cablato o wireless.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Elemento OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311667"
---
# <a name="onex-element"></a><span data-ttu-id="82552-103">Elemento OneX</span><span class="sxs-lookup"><span data-stu-id="82552-103">OneX Element</span></span>

<span data-ttu-id="82552-104">L'elemento OneX specifica le informazioni di configurazione 802.1 X per un profilo LAN cablato o wireless.</span><span class="sxs-lookup"><span data-stu-id="82552-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="82552-105">Questo elemento è l'elemento radice univoco per un profilo 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="82552-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="82552-106">Lo spazio dei nomi di destinazione per l'elemento OneX è `https://www.microsoft.com/networking/OneX/v1` .</span><span class="sxs-lookup"><span data-stu-id="82552-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="82552-107">La maggior parte degli elementi figlio dell'elemento OneX si trova nello `OneX` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="82552-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="82552-108">Si verifica un'eccezione: l'elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) si trova nello `https://www.microsoft.com/provisioning/EapHostConfig` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="82552-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="82552-109">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** È supportato solo l'elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="82552-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="82552-110">Gli altri elementi, se presenti in un profilo, verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="82552-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
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
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
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

## <a name="child-elements"></a><span data-ttu-id="82552-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="82552-111">Child elements</span></span>



| <span data-ttu-id="82552-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="82552-112">Element</span></span>                                                                            | <span data-ttu-id="82552-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="82552-113">Type</span></span>    | <span data-ttu-id="82552-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82552-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82552-115">**authMode**</span><span class="sxs-lookup"><span data-stu-id="82552-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="82552-116">Specifica il tipo di credenziali utilizzate per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="82552-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="82552-117">**authPeriod**</span><span class="sxs-lookup"><span data-stu-id="82552-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="82552-118">Specifica il periodo di tempo massimo, in secondi, durante il quale un client attende una risposta dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="82552-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="82552-119">**cacheUserData**</span><span class="sxs-lookup"><span data-stu-id="82552-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="82552-120">boolean</span><span class="sxs-lookup"><span data-stu-id="82552-120">boolean</span></span> | <span data-ttu-id="82552-121">Specifica se le credenziali utente vengono memorizzate nella cache per le connessioni successive.</span><span class="sxs-lookup"><span data-stu-id="82552-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="82552-122">**EAPConfig**</span><span class="sxs-lookup"><span data-stu-id="82552-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="82552-123">Specifica la configurazione EAPHost.</span><span class="sxs-lookup"><span data-stu-id="82552-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="82552-124">**heldPeriod**</span><span class="sxs-lookup"><span data-stu-id="82552-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="82552-125">Specifica l'intervallo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito.</span><span class="sxs-lookup"><span data-stu-id="82552-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="82552-126">**maxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="82552-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="82552-127">Specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.</span><span class="sxs-lookup"><span data-stu-id="82552-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="82552-128">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="82552-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="82552-129">Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione del Single Sign-On abbia esito negativo.</span><span class="sxs-lookup"><span data-stu-id="82552-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="82552-130">**maxStart**</span><span class="sxs-lookup"><span data-stu-id="82552-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="82552-131">Specifica il numero massimo di messaggi di EAPOL-Start inviati.</span><span class="sxs-lookup"><span data-stu-id="82552-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="82552-132">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="82552-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="82552-133">Specifica Single Sign-On informazioni sulla configurazione di rete.</span><span class="sxs-lookup"><span data-stu-id="82552-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="82552-134">**startPeriod**</span><span class="sxs-lookup"><span data-stu-id="82552-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="82552-135">Specifica il tempo di attesa, in secondi, prima dell'invio di un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="82552-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="82552-136">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="82552-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="82552-137">Specifica il metodo di trasmissione usato per i pacchetti avvio EAPOL.</span><span class="sxs-lookup"><span data-stu-id="82552-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="82552-138">**tipo**</span><span class="sxs-lookup"><span data-stu-id="82552-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="82552-139">Specifica quando Single Sign-On viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82552-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="82552-140">Se impostata su `preLogon` , Single Sign-on viene eseguita prima dell'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="82552-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="82552-141">Quando è impostata su `postLogon` , Single Sign-on viene eseguita immediatamente dopo l'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="82552-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="82552-142">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="82552-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="82552-143">boolean</span><span class="sxs-lookup"><span data-stu-id="82552-143">boolean</span></span> | <span data-ttu-id="82552-144">Specifica se la LAN virtuale (VLAN) usata dal dispositivo viene modificata in base alle credenziali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="82552-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="82552-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="82552-145">Remarks</span></span>

<span data-ttu-id="82552-146">Per visualizzare l'elenco di elementi figlio in una struttura simile a un albero, vedere [elementi dello schema Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="82552-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82552-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82552-147">Requirements</span></span>



| <span data-ttu-id="82552-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="82552-148">Requirement</span></span> | <span data-ttu-id="82552-149">Valore</span><span class="sxs-lookup"><span data-stu-id="82552-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="82552-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82552-150">Minimum supported client</span></span><br/> | <span data-ttu-id="82552-151">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="82552-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="82552-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82552-152">Minimum supported server</span></span><br/> | <span data-ttu-id="82552-153">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82552-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="82552-154">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="82552-154">Redistributable</span></span><br/>          | <span data-ttu-id="82552-155">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="82552-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




