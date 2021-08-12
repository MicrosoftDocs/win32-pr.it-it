---
description: Usa Extensible Authentication Protocol Transport Level Security (EAP-TLS) con certificati per l'autenticazione in rete (WPA-Enterprise).
ms.assetid: fceeae22-3761-48ab-a190-1a7b1568ed64
title: WPA-Enterprise esempio di profilo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9ebb9fa779c1a1d9a4e77c20d462f31fcafc9ec562e47ae106386b58c112a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619044"
---
# <a name="wpa-enterprise-with-tls-profile-sample"></a>WPA-Enterprise esempio di profilo TLS

Questo profilo di esempio usa Extensible Authentication Protocol Transport Level Security (EAP-TLS) con certificati per l'autenticazione alla rete.

Questo esempio è configurato per l'Wi-Fi sicurezza da accesso protetto in esecuzione in modalità Enterprise (WPA-Enterprise). Il WPA-Enterprise di sicurezza usa 802.1X per lo scambio di autenticazione con il back-end. Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia.

Le credenziali EAP-TLS vengono ottenute dall'archivio certificati. Se l'autenticazione basata sulle credenziali nell'archivio certificati non riesce, all'utente viene richiesto di fornire credenziali valide. Se il primo tentativo non riesce, non vengono utilizzati server alternativi, autorità di certificazione radice o nomi utente per l'autenticazione.

La configurazione EAPHost usata in questo esempio di profilo wireless è stata derivata dall'esempio delle proprietà di connessione [EAP-TLS.](../eaphost/eap-tls-connection-properties.md)

**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless. L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stata modificata. L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. L'impostazione predefinita era "true" Windows Server 2008 e Windows Vista. Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** EAP-TLS non è supportato.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> </dl>

 

 
