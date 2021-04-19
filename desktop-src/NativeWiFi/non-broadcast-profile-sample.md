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
# <a name="non-broadcast-profile-sample"></a><span data-ttu-id="af694-103">Esempio di profilo non broadcast</span><span class="sxs-lookup"><span data-stu-id="af694-103">Non-Broadcast Profile Sample</span></span>

<span data-ttu-id="af694-104">L'esempio di profilo non broadcast può essere usato per connettersi a reti che non trasmettono il nome di rete o l'SSID.</span><span class="sxs-lookup"><span data-stu-id="af694-104">The non-broadcast profile sample can be used to connect to networks which do not broadcast their network name or SSID.</span></span>

<span data-ttu-id="af694-105">Questo profilo di esempio è configurato per l'uso di Wi-Fi sicurezza dell'accesso protetto in esecuzione in modalità personale (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="af694-105">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="af694-106">Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="af694-106">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span> <span data-ttu-id="af694-107">I profili che usano altri tipi di crittografia e sicurezza possono anche essere configurati come profili non broadcast.</span><span class="sxs-lookup"><span data-stu-id="af694-107">Profiles that use other security and cipher types can also be configured as non-broadcast profiles.</span></span>

<span data-ttu-id="af694-108">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="af694-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="af694-109">Il nome del profilo, come archiviato nell'archivio profili, deriva dal [**nome**](wlan-profileschema-name-ssid-element.md) figlio dell'elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="af694-109">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="af694-110">La chiave condivisa è stata omessa da questo profilo di esempio.</span><span class="sxs-lookup"><span data-stu-id="af694-110">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="af694-111">Se si tenta di utilizzare questo profilo di esempio per connettersi a una rete, verrà richiesto di immettere una chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="af694-111">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="af694-112">È possibile evitare questa richiesta aggiungendo un elemento figlio [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) all'elemento [**Security**](wlan-profileschema-security-msm-element.md) immediatamente dopo l'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="af694-112">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="af694-113">Il frammento di codice seguente mostra un elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) che contiene una chiave non crittografata.</span><span class="sxs-lookup"><span data-stu-id="af694-113">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="af694-114">È necessario sostituire il commento `<!-- insert key here -->` con la chiave non crittografata effettiva prima di usare questo frammento in un profilo.</span><span class="sxs-lookup"><span data-stu-id="af694-114">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="af694-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af694-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af694-116">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="af694-116">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



