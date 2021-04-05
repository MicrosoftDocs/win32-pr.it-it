---
description: Usa il protocollo EAP-TLS (Extensible Authentication Protocol Transport Level Security) con certificati per eseguire l'autenticazione alla rete.
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: Esempio di WPA-Enterprise con il profilo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5300f8886d55ac713b0206b45f20857f22b2772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968306"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="1669e-103">Esempio di WPA-Enterprise con il profilo TLS</span><span class="sxs-lookup"><span data-stu-id="1669e-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="1669e-104">Questo profilo di esempio usa EAP-TLS (Extensible Authentication Protocol Transport Level Security) con certificati per eseguire l'autenticazione alla rete.</span><span class="sxs-lookup"><span data-stu-id="1669e-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="1669e-105">Questo esempio è configurato per l'uso di Wi-Fi sicurezza dell'accesso protetto in esecuzione in modalità Enterprise (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="1669e-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="1669e-106">Il tipo di sicurezza WPA-Enterprise USA 802.1 X per lo scambio di autenticazione con il back-end.</span><span class="sxs-lookup"><span data-stu-id="1669e-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="1669e-107">Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="1669e-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="1669e-108">Le credenziali EAP-TLS sono ottenute dall'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="1669e-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="1669e-109">Se l'autenticazione basata sulle credenziali nell'archivio certificati non riesce, all'utente viene richiesto di fornire credenziali valide.</span><span class="sxs-lookup"><span data-stu-id="1669e-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="1669e-110">Non vengono utilizzati server alternativi, autorità di certificazione radice o nomi utente per l'autenticazione se il primo tentativo non riesce.</span><span class="sxs-lookup"><span data-stu-id="1669e-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="1669e-111">La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio delle [proprietà di connessione EAP-TLS](../eaphost/eap-tls-connection-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="1669e-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="1669e-112">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="1669e-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="1669e-113">L'impostazione predefinita per il [**commutatore autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è cambiata.</span><span class="sxs-lookup"><span data-stu-id="1669e-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="1669e-114">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="1669e-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="1669e-115">L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1669e-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="1669e-116">Per ulteriori informazioni, fare riferimento alla descrizione dell'elemento dello schema [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1669e-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="1669e-117">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** EAP-TLS non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1669e-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAEnterpriseTLS</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAEnterpriseTLS</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA</authentication>
                <encryption>TKIP</encryption>
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

## <a name="related-topics"></a><span data-ttu-id="1669e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1669e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1669e-119">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="1669e-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
