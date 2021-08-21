---
description: Usato per connettersi a una rete che richiede impostazioni di sicurezza conformi agli standard FIPS (Federal Information Processing Standards) 140-2.
ms.assetid: 169df4a3-e8b9-4f05-874f-a7eef6658d01
title: Esempio di profilo FIPS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 688a5811407d8a0d48963a54db9fc0d717b75a719ba8879ba20f1e83cbf7012e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801291"
---
# <a name="fips-profile-sample"></a>Esempio di profilo FIPS

L'esempio di profilo FIPS può essere usato per connettersi a una rete che richiede impostazioni di sicurezza conformi agli standard FIPS (Federal Information Processing Standards) 140-2. Per altre informazioni su FIPS, vedere [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).

**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless. L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stato modificato. L'impostazione predefinita viene modificata in "false" Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. L'impostazione predefinita era "true" Windows Server 2008 e Windows Vista. Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato. Il nome del profilo, archiviato nell'archivio profili, deriva dal nome [**figlio**](wlan-profileschema-name-ssid-element.md) [**dell'elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md) [**L'elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) non è supportato.

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>FIPS_TEST</name>
    <SSIDConfig>
        <SSID>
            <hex>464950535F54455354</hex>
            <name>FIPS_TEST</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
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
                <FIPSMode xmlns="https://www.microsoft.com/networking/WLAN/profile/v2">true</FIPSMode>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig">
                    <EapMethod>
                        <Type xmlns="https://www.microsoft.com/provisioning/EapCommon">25</Type>
                        <VendorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorId>
                        <VendorType xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorType>
                        <AuthorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</AuthorId>
                    </EapMethod>
                    <ConfigBlob></ConfigBlob>
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

 

 



