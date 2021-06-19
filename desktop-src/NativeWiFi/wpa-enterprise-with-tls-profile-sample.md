---
description: Usa Extensible Authentication Protocol Transport Level Security (EAP-TLS) con certificati per l'autenticazione alla rete (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: WPA-Enterprise esempio di profilo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d6f236429c94e9602e173c2d6c3eb1e3bc8111f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395036"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a><span data-ttu-id="6eef3-103">WPA-Enterprise esempio di profilo TLS</span><span class="sxs-lookup"><span data-stu-id="6eef3-103">WPA-Enterprise with TLS Profile Sample</span></span>

<span data-ttu-id="6eef3-104">Questo profilo di esempio usa Extensible Authentication Protocol Transport Level Security (EAP-TLS) con certificati per l'autenticazione nella rete.</span><span class="sxs-lookup"><span data-stu-id="6eef3-104">This sample profile uses Extensible Authentication Protocol Transport Level Security (EAP-TLS) with certificates to authenticate to the network.</span></span>

<span data-ttu-id="6eef3-105">Questo esempio è configurato per l'Wi-Fi sicurezza dell'accesso protetto in esecuzione in modalità Enterprise (WPA-Enterprise).</span><span class="sxs-lookup"><span data-stu-id="6eef3-105">This sample is configured to use Wi-Fi Protected Access security running in Enterprise mode (WPA-Enterprise).</span></span> <span data-ttu-id="6eef3-106">Il WPA-Enterprise di sicurezza usa 802.1X per lo scambio di autenticazione con il back-end.</span><span class="sxs-lookup"><span data-stu-id="6eef3-106">The WPA-Enterprise security type uses 802.1X for the authentication exchange with the backend.</span></span> <span data-ttu-id="6eef3-107">Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="6eef3-107">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="6eef3-108">Le credenziali EAP-TLS vengono ottenute dall'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="6eef3-108">The EAP-TLS credentials are obtained from the certificate store.</span></span> <span data-ttu-id="6eef3-109">Se l'autenticazione basata sulle credenziali nell'archivio certificati ha esito negativo, all'utente viene richiesto di fornire credenziali valide.</span><span class="sxs-lookup"><span data-stu-id="6eef3-109">If authentication based on the credentials in the certificate store fails, the user is prompted to provide valid credentials.</span></span> <span data-ttu-id="6eef3-110">Se il primo tentativo non riesce, non vengono usati server alternativi, autorità di certificazione radice o nomi utente per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6eef3-110">No alternate servers, root certificate authorities, or user names are used for authentication if the first attempt fails.</span></span>

<span data-ttu-id="6eef3-111">La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio di proprietà [di connessione EAP-TLS.](../eaphost/eap-tls-connection-properties.md)</span><span class="sxs-lookup"><span data-stu-id="6eef3-111">The EAPHost configuration used in this wireless profile sample was derived from the [EAP-TLS Connection Properties](../eaphost/eap-tls-connection-properties.md) sample.</span></span>

<span data-ttu-id="6eef3-112">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="6eef3-112">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="6eef3-113">L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6eef3-113">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="6eef3-114">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="6eef3-114">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="6eef3-115">L'impostazione predefinita era "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6eef3-115">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="6eef3-116">Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="6eef3-116">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="6eef3-117">**Windows XP con SP3 e API LAN wireless per Windows XP con SP2:** EAP-TLS non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6eef3-117">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** EAP-TLS is not supported.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6eef3-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6eef3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eef3-119">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="6eef3-119">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
