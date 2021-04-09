---
description: Usa il protocollo EAP-TLS (Extensible Authentication Protocol Transport Level Security) con certificati per eseguire l'autenticazione alla rete.
ms.assetid: ded07fda-ea7f-4c5a-9433-60196c3f14af
title: Esempio di WPA2-Enterprise con il profilo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd85d30bed631a55f0e7e622aac4a8ade17ba3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049507"
---
# <a name="wpa2-enterprise-with-tls-profile-sample"></a>Esempio di WPA2-Enterprise con il profilo TLS

Questo profilo di esempio usa EAP-TLS (Extensible Authentication Protocol Transport Level Security) con certificati per eseguire l'autenticazione alla rete.

Questo esempio è configurato per l'uso di Wi-Fi sicurezza protetta di Access 2 in esecuzione in modalità Enterprise (WPA2-Enterprise). Il tipo di sicurezza WPA2-Enterprise USA 802.1 X per lo scambio di autenticazione con il back-end. Il tipo di crittografia Advanced Encryption Standard (AES) viene utilizzato per la crittografia.

Le credenziali EAP-TLS sono ottenute dall'archivio certificati. Se l'autenticazione basata sulle credenziali nell'archivio certificati non riesce, all'utente viene richiesto di fornire credenziali valide. Non vengono utilizzati server alternativi, autorità di certificazione radice o nomi utente per l'autenticazione se il primo tentativo non riesce.

La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio delle [proprietà di connessione EAP-TLS](../eaphost/eap-tls-connection-properties.md) .

**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless. L'impostazione predefinita per il [**commutatore autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è cambiata. L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista. Per ulteriori informazioni, fare riferimento alla descrizione dell'elemento dello schema [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** EAP-TLS non è supportato.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> </dl>

 

 
