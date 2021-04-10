---
description: Utilizzato per eseguire l'autenticazione a una rete wireless per la prima volta prima che il computer sia stato aggiunto a un dominio.
ms.assetid: e1a5ce76-9761-4c65-8b26-a44bf2eb1835
title: Esempio di profilo bootstrap
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 96c7daa6bdc72146400973d08c9e5780092b214a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232056"
---
# <a name="bootstrap-profile-sample"></a><span data-ttu-id="7ae47-103">Esempio di profilo bootstrap</span><span class="sxs-lookup"><span data-stu-id="7ae47-103">Bootstrap Profile Sample</span></span>

<span data-ttu-id="7ae47-104">L'esempio di profilo bootstrap può essere usato per eseguire l'autenticazione a una rete wireless per la prima volta prima che il computer sia stato aggiunto a un dominio.</span><span class="sxs-lookup"><span data-stu-id="7ae47-104">The Bootstrap profile sample can be used to authenticate to a wireless network for the first time before the computer has joined a domain.</span></span>

<span data-ttu-id="7ae47-105">Questo profilo non convalida i certificati presentati dal server Remote Authentication Dial-In User Service (RADIUS) e non deve essere usato dopo che il computer è stato aggiunto a un dominio.</span><span class="sxs-lookup"><span data-stu-id="7ae47-105">This profile does not validate the certificates presented by the Remote Authentication Dial-In User Service (RADIUS) server, and should not be used after the machine is joined to a domain.</span></span>

<span data-ttu-id="7ae47-106">Questo esempio è configurato per l'uso di Wi-Fi sicurezza protetta di Access 2 in esecuzione in modalità Enterprise (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="7ae47-106">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="7ae47-107">È possibile utilizzare altri tipi di sicurezza purché il metodo di autenticazione sia PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="7ae47-107">Other security types can be used as long as the authentication method is PEAP-MSCHAPv2.</span></span>

<span data-ttu-id="7ae47-108">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="7ae47-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="7ae47-109">L'impostazione predefinita per il [**commutatore autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è cambiata.</span><span class="sxs-lookup"><span data-stu-id="7ae47-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="7ae47-110">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="7ae47-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="7ae47-111">L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7ae47-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="7ae47-112">Per ulteriori informazioni, fare riferimento alla descrizione dell'elemento dello schema [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae47-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="7ae47-113">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="7ae47-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="7ae47-114">Il nome del profilo, come archiviato nell'archivio profili, deriva dal [**nome**](wlan-profileschema-name-ssid-element.md) figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae47-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="7ae47-115">Gli elementi figlio [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**AuthMode**](onexschema-authmode-onex-element.md)e [**singleSignOn**](onexschema-singlesignon-onex-element.md) dell'elemento [**Onex**](onexschema-onex-element.md) non sono supportati e devono essere rimossi dal profilo prima dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="7ae47-115">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleBootstrap</name>
    <SSIDConfig>
        <SSID>
            <name>SampleBootstrap</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <cacheUserData>true</cacheUserData>
                <authMode>machineOrUser</authMode>
                <singleSignOn>
                    <type>preLogon</type>
                    <maxDelay>10</maxDelay>
                </singleSignOn>
               <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>true</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
               </EAPConfig>
           </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="7ae47-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ae47-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae47-117">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="7ae47-117">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="7ae47-118">Aggiunta di un client wireless Windows Vista a un dominio</span><span class="sxs-lookup"><span data-stu-id="7ae47-118">Joining a Windows Vista Wireless Client to a Domain</span></span>](https://www.microsoft.com/technet/network/wifi/vista_bootstrap_wireless.mspx)
</dt> </dl>

 

 



