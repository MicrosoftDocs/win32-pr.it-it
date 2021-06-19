---
description: Usa una chiave precondicondisa per l'autenticazione di rete. Questo profilo di esempio usa Wi-Fi protezione di Accesso protetto 2 in esecuzione in modalità personale (WPA2-Personal).
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: WPA2-Personal di profilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e0df238b83a27155e640d56fc81ed5606a76e3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394866"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="a27c9-104">WPA2-Personal di profilo</span><span class="sxs-lookup"><span data-stu-id="a27c9-104">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="a27c9-105">Questo profilo di esempio usa una chiave precondidicazione per l'autenticazione di rete.</span><span class="sxs-lookup"><span data-stu-id="a27c9-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="a27c9-106">La chiave viene condivisa con il client e il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="a27c9-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="a27c9-107">Questo profilo di esempio è configurato per l'Wi-Fi protezione di Accesso protetto 2 in esecuzione in modalità personale (WPA2-Personal).</span><span class="sxs-lookup"><span data-stu-id="a27c9-107">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="a27c9-108">Il Advanced Encryption Standard (AES) viene usato per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="a27c9-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="a27c9-109">**Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato:** Le modifiche vengono implementate in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato per ottimizzare le prestazioni di rete wireless.</span><span class="sxs-lookup"><span data-stu-id="a27c9-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="a27c9-110">L'impostazione predefinita per [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) quando questo elemento non è impostato in un profilo LAN wireless è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="a27c9-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="a27c9-111">L'impostazione predefinita viene modificata in "false" in Windows 7 e Windows Server 2008 R2 con il servizio LAN wireless installato.</span><span class="sxs-lookup"><span data-stu-id="a27c9-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="a27c9-112">L'impostazione predefinita è "true" in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a27c9-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a27c9-113">Per altre informazioni, vedere la descrizione dell'elemento dello schema [**autoSwitch.**](wlan-profileschema-autoswitch-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="a27c9-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="a27c9-114">**Windows XP con SP3 e API LAN wireless per Windows XP con SP2:** Il [**nome**](wlan-profileschema-name-wlanprofile-element.md) figlio dell'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a27c9-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="a27c9-115">Il nome del profilo, archiviato nell'archivio profili, deriva dal nome [**figlio**](wlan-profileschema-name-ssid-element.md) [**dell'elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)</span><span class="sxs-lookup"><span data-stu-id="a27c9-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="a27c9-116">La chiave condivisa è stata omessa da questo profilo di esempio.</span><span class="sxs-lookup"><span data-stu-id="a27c9-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="a27c9-117">Se si tenta di usare questo profilo di esempio per connettersi a una rete, verrà richiesto di immettere una chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="a27c9-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="a27c9-118">È possibile evitare questa richiesta aggiungendo un elemento figlio [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) all'elemento [**di**](wlan-profileschema-security-msm-element.md) sicurezza immediatamente dopo l'elemento [**authEncryption.**](wlan-profileschema-authencryption-security-element.md)</span><span class="sxs-lookup"><span data-stu-id="a27c9-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="a27c9-119">Il frammento di codice seguente illustra [**un elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) che contiene una chiave non crittografata.</span><span class="sxs-lookup"><span data-stu-id="a27c9-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="a27c9-120">È necessario sostituire il commento con la chiave non crittografata effettiva prima `<!-- insert key here -->` di usare questo frammento di codice in un profilo.</span><span class="sxs-lookup"><span data-stu-id="a27c9-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="a27c9-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a27c9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a27c9-122">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="a27c9-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



