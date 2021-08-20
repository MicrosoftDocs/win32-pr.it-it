---
description: Usa Protected Extensible Authentication Protocol con Microsoft Challenge Handshake Authentication Protocol versione 2, con WPA2-Enterprise.
ms.assetid: fcbc74a6-1990-45a0-af2e-1c343a84497a
title: WPA2-Enterprise esempio di PEAP-MSCHAPv2 profilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b746cd39826ed5aacb07118f2d989ebc97a380579b28a742a5732f0f4e86078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983938"
---
# <a name="wpa2-enterprise-with-peap-mschapv2-profile-sample"></a>WPA2-Enterprise esempio di PEAP-MSCHAPv2 profilo

Questo profilo di esempio usa protected extensible authentication protocol con Microsoft Challenge Handshake Authentication Protocol versione 2 (PEAP-MSCHAPv2) con *UserName* Password per l'autenticazione **/**  alla rete. All'utente viene richiesto di immettere le credenziali.

Questo esempio è configurato per l'Wi-Fi sicurezza di Protected Access 2 in esecuzione in modalità Enterprise (WPA2-Enterprise). Il WPA2-Enterprise di sicurezza usa 802.1X per lo scambio di autenticazione con il back-end. Per la Advanced Encryption Standard viene usato il tipo di crittografia Advanced Encryption Standard (AES).

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato. Il nome del profilo, archiviato nell'archivio profili, deriva dal nome [**figlio**](wlan-profileschema-name-ssid-element.md) [**dell'elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2EnterprisePEAPMSCHAP</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2EnterprisePEAPMSCHAP</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> </dl>

 

 



