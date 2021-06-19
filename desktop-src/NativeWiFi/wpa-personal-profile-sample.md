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
# <a name="wpa-personal-profile-sample"></a><span data-ttu-id="3b8a8-104">WPA-Personal di profilo</span><span class="sxs-lookup"><span data-stu-id="3b8a8-104">WPA-Personal Profile Sample</span></span>

<span data-ttu-id="3b8a8-105">Questo profilo di esempio usa una chiave precondicazione per l'autenticazione di rete.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="3b8a8-106">La chiave viene condivisa con il client e il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="3b8a8-107">Questo profilo di esempio è configurato per l'Wi-Fi protezione dall'accesso protetto in esecuzione in modalità personale (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="3b8a8-107">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="3b8a8-108">Il protocollo TKIP (Temporal Key Integrity Protocol) viene usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-108">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span>

<span data-ttu-id="3b8a8-109">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="3b8a8-110">L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="3b8a8-111">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="3b8a8-112">L'impostazione predefinita era "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="3b8a8-113">Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="3b8a8-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="3b8a8-114">**Windows XP con SP3 e API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="3b8a8-115">Il nome del profilo, archiviato nell'archivio profili, deriva dal nome [**figlio**](wlan-profileschema-name-ssid-element.md) [**dell'elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)</span><span class="sxs-lookup"><span data-stu-id="3b8a8-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="3b8a8-116">La chiave condivisa è stata omessa da questo profilo di esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="3b8a8-117">Se si tenta di usare questo profilo di esempio per connettersi a una rete, verrà richiesto di immettere una chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="3b8a8-118">È possibile evitare questa richiesta aggiungendo un elemento figlio [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) all'elemento [**di**](wlan-profileschema-security-msm-element.md) sicurezza immediatamente dopo l'elemento [**authEncryption.**](wlan-profileschema-authencryption-security-element.md)</span><span class="sxs-lookup"><span data-stu-id="3b8a8-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="3b8a8-119">Il frammento di codice seguente illustra [**un elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) che contiene una chiave non crittografata.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="3b8a8-120">È necessario sostituire il commento con la chiave non crittografata effettiva prima `<!-- insert key here -->` di usare questo frammento di codice in un profilo.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="3b8a8-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b8a8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b8a8-122">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="3b8a8-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



