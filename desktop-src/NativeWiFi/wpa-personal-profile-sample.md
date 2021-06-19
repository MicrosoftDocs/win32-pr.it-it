---
description: Usa una chiave precondicondisa per l'autenticazione di rete. Questo profilo di esempio usa Wi-Fi di accesso protetto in esecuzione in modalità personale (WPA-Personal).
ms.assetid: f04de28b-a98d-40cd-91c8-e446cf669555
title: WPA-Personal di profilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334076d4b0cf10372ed845265a1fff652f0879b9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395026"
---
# <a name="wpa-personal-profile-sample"></a>WPA-Personal di profilo

Questo profilo di esempio usa una chiave precondicazione per l'autenticazione di rete. La chiave viene condivisa con il client e il punto di accesso. Questo profilo di esempio è configurato per l'Wi-Fi protezione dall'accesso protetto in esecuzione in modalità personale (WPA-Personal). Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia.

**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless. L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stato modificato. L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. L'impostazione predefinita era "true" in Windows Server 2008 e Windows Vista. Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)

**Windows XP con SP3 e API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato. Il nome del profilo, archiviato nell'archivio profili, deriva dal nome [**figlio**](wlan-profileschema-name-ssid-element.md) [**dell'elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPAPSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPAPSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

La chiave condivisa è stata omessa da questo profilo di esempio. Se si tenta di usare questo profilo di esempio per connettersi a una rete, verrà richiesto di immettere una chiave condivisa. È possibile evitare questa richiesta aggiungendo un elemento figlio [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) all'elemento [**di**](wlan-profileschema-security-msm-element.md) sicurezza immediatamente dopo l'elemento [**authEncryption.**](wlan-profileschema-authencryption-security-element.md)

Il frammento di codice seguente illustra [**un elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) che contiene una chiave non crittografata. È necessario sostituire il commento con la chiave non crittografata effettiva prima `<!-- insert key here -->` di usare questo frammento di codice in un profilo.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> </dl>

 

 



