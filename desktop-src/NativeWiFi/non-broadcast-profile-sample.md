---
description: Usato per connettersi alle reti che non trasmettono il nome di rete o l'SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Esempio di profilo non broadcast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311678"
---
# <a name="non-broadcast-profile-sample"></a>Esempio di profilo non broadcast

L'esempio di profilo non broadcast può essere usato per connettersi a reti che non trasmettono il nome di rete o l'SSID.

Questo profilo di esempio è configurato per l'uso di Wi-Fi sicurezza dell'accesso protetto in esecuzione in modalità personale (WPA-Personal). Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia. I profili che usano altri tipi di crittografia e sicurezza possono anche essere configurati come profili non broadcast.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato. Il nome del profilo, come archiviato nell'archivio profili, deriva dal [**nome**](wlan-profileschema-name-ssid-element.md) figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
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

 

 



