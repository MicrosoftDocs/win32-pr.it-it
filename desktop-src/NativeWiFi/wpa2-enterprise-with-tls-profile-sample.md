---
description: Usa Extensible Authentication Protocol Transport Level Security (EAP-TLS) con certificati per l'autenticazione in rete (WPA2-Enterprise).
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: WPA2-Enterprise esempio di profilo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba561f552614896ca5da1522180a53146dc5ce54
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394822"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a><span data-ttu-id="bcefe-103">WPA2-Enterprise esempio di profilo TLS</span><span class="sxs-lookup"><span data-stu-id="bcefe-103">WPA2-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="bcefe-104">Questo profilo di esempio usa Extensible Authentication Protocol Transport Level Security (EAP-TLS) con certificati per l'autenticazione alla rete.</span><span class="sxs-lookup"><span data-stu-id="bcefe-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="bcefe-105">Questo esempio è configurato per l'Wi-Fi sicurezza di Protected Access 2 in esecuzione in modalità Enterprise (WPA2-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="bcefe-105">This sample is configured to use Wi-Fi Protected Access 2 security running in Enterprise mode (WPA2-Enterprise).</span></span> <span data-ttu-id="bcefe-106">Il WPA2-Enterprise di sicurezza usa 802.1X per lo scambio di autenticazione con il back-end.</span><span class="sxs-lookup"><span data-stu-id="bcefe-106">The WPA2-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="bcefe-107">Il Advanced Encryption Standard di crittografia AES (Advanced Encryption Standard) viene usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="bcefe-107">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="bcefe-108">Le credenziali EAP-TLS vengono ottenute dall'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="bcefe-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="bcefe-109">Se l'autenticazione basata sulle credenziali nell'archivio certificati non riesce, all'utente viene richiesto di fornire credenziali valide.</span><span class="sxs-lookup"><span data-stu-id="bcefe-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="bcefe-110">Se il primo tentativo non riesce, non vengono utilizzati server alternativi, autorità di certificazione radice o nomi utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="bcefe-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="bcefe-111">La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio delle proprietà di connessione [EAP-TLS.](../eaphost/eap-tls-connection-properties.md)</span><span class="sxs-lookup"><span data-stu-id="bcefe-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="bcefe-112">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="bcefe-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="bcefe-113">L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="bcefe-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="bcefe-114">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="bcefe-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="bcefe-115">L'impostazione predefinita era "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bcefe-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="bcefe-116">Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="bcefe-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="bcefe-117">**Windows XP con SP3 e API LAN wireless per Windows XP con SP2:** EAP-TLS non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bcefe-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterpriseTLS</name>
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
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
 
                        <EapMethod>
                            <eapCommon:Type>13</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                        </EapMethod>
                        <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                                xmlns:eapTls="https://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">

                            <baseEap:Eap>
                                <baseEap:Type>13</baseEap:Type> 
                                <eapTls:EapType>
                                    <eapTls:CredentialsSource>
                                        <eapTls:CertificateStore />
                                    </eapTls:CredentialsSource>
                                    <eapTls:ServerValidation>
                                        <eapTls:DisableUserPromptForServerValidation>false</eapTls:DisableUserPromptForServerValidation> 
                                        <eapTls:ServerNames /> 
                                    </eapTls:ServerValidation> 
                                   <eapTls:DifferentUsername>false</eapTls:DifferentUsername> 
                               </eapTls:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="bcefe-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bcefe-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcefe-119">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="bcefe-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
