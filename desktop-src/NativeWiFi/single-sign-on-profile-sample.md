---
description: Utilizzato per gli scenari che richiedono l'autenticazione 802.1 X prima dell'accesso a Windows.
ms.assetid: 76c8d416-3912-41b1-ac9d-3e6e86a76ceb
title: Esempio di profilo Single Sign-On
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 077ed95095150e81ad9a3d7412d1940dcb1b33e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318973"
---
# <a name="single-sign-on-profile-sample"></a><span data-ttu-id="ce863-103">Esempio di profilo Single Sign-On</span><span class="sxs-lookup"><span data-stu-id="ce863-103">Single Sign-On Profile Sample</span></span>

<span data-ttu-id="ce863-104">L'esempio di profilo Single Sign-On (SSO) può essere utilizzato per gli scenari che richiedono l'autenticazione 802.1 X prima dell'accesso a Windows.</span><span class="sxs-lookup"><span data-stu-id="ce863-104">The single sign-on (SSO) profile sample can be used for scenarios that require 802.1X authentication before Windows logon.</span></span>

<span data-ttu-id="ce863-105">Questo esempio è configurato per l'uso di Wi-Fi sicurezza protetta di Access 2 in esecuzione in modalità Enterprise (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="ce863-105">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="ce863-106">Il protocollo Protected Extensible Authentication con Microsoft Challenge Handshake Authentication Protocol versione 2 (PEAP-MSCHAPv2) viene usato per l'autenticazione di rete.</span><span class="sxs-lookup"><span data-stu-id="ce863-106">Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) is used for network authentication.</span></span> <span data-ttu-id="ce863-107">Le credenziali di accesso di Windows vengono utilizzate per l'autenticazione PEAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="ce863-107">The Windows logon credentials are used for PEAP-MSCHAPv2 authentication.</span></span>

<span data-ttu-id="ce863-108">Sebbene questo esempio sia configurato per l'utilizzo di WPA2-Enterprise e PEAP-MSCHAPv2, i profili SSO possono essere configurati con altri tipi di sicurezza e autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ce863-108">While this sample is configured to use WPA2-Enterprise and PEAP-MSCHAPv2, SSO profiles can be configured with other security and authentication types.</span></span>

<span data-ttu-id="ce863-109">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="ce863-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="ce863-110">L'impostazione predefinita per il [**commutatore autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è cambiata.</span><span class="sxs-lookup"><span data-stu-id="ce863-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="ce863-111">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="ce863-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="ce863-112">L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce863-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="ce863-113">Per ulteriori informazioni, fare riferimento alla descrizione dell'elemento dello schema [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ce863-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="ce863-114">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ce863-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="ce863-115">Il nome del profilo, come archiviato nell'archivio profili, deriva dal [**nome**](wlan-profileschema-name-ssid-element.md) figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ce863-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="ce863-116">Gli elementi figlio [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**AuthMode**](onexschema-authmode-onex-element.md)e [**singleSignOn**](onexschema-singlesignon-onex-element.md) dell'elemento [**Onex**](onexschema-onex-element.md) non sono supportati e devono essere rimossi dal profilo prima dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ce863-116">The [**cacheUserData**](onexschema-cacheuserdata-onex-element.md), [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md), [**authMode**](onexschema-authmode-onex-element.md), and [**singleSignOn**](onexschema-singlesignon-onex-element.md) children of the [**OneX**](onexschema-onex-element.md) element are not supported, and should be removed from the profile before use.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleSingleSignOn</name>
    <SSIDConfig>
        <SSID>
            <name>SampleSingleSignOn</name>
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
                <maxAuthFailures>3</maxAuthFailures>
                <authMode>user</authMode>
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
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="ce863-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce863-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce863-118">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="ce863-118">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



