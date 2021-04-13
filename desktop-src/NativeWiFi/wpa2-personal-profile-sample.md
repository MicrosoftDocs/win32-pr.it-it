---
description: Usa una chiave precondivisa per l'autenticazione di rete.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Esempio di profilo di WPA2-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0054bc28962113a85bb909d4e8cd173b3bc16974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348121"
---
# <a name="wpa2-personal-profile-sample"></a>Esempio di profilo di WPA2-Personal

Questo profilo di esempio usa una chiave precondivisa per l'autenticazione di rete. La chiave viene condivisa con il client e il punto di accesso. Questo profilo di esempio è configurato per l'uso di Wi-Fi sicurezza con accesso protetto 2 in esecuzione in modalità personale (WPA2-Personal). Il tipo di crittografia Advanced Encryption Standard (AES) viene utilizzato per la crittografia.

**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche sono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless. L'impostazione predefinita per il [**commutatore autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è cambiata. L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato. L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista. Per ulteriori informazioni, fare riferimento alla descrizione dell'elemento dello schema [**autoswitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato. Il nome del profilo, come archiviato nell'archivio profili, deriva dal [**nome**](wlan-profileschema-name-ssid-element.md) figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

La chiave condivisa è stata omessa da questo profilo di esempio. Se si tenta di utilizzare questo profilo di esempio per connettersi a una rete, verrà richiesto di immettere una chiave condivisa. È possibile evitare questa richiesta aggiungendo un elemento figlio [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) all'elemento [**Security**](wlan-profileschema-security-msm-element.md) immediatamente dopo l'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

Il frammento di codice seguente mostra un elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) che contiene una chiave non crittografata. È necessario sostituire il commento `<!-- insert key here -->` con la chiave non crittografata effettiva prima di usare questo frammento in un profilo.

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

 

 



