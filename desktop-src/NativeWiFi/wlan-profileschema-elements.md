---
description: Lo \_ schema del profilo WLAN definisce gli elementi seguenti.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Elementi dello schema WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752306"
---
# <a name="wlan_profile-schema-elements"></a>\_Elementi dello schema del profilo WLAN

Lo \_ schema del profilo WLAN definisce gli elementi seguenti. La maggior parte degli elementi si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v1` , ad eccezione di [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), che si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v2` .

Nell'elenco seguente vengono illustrati gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo. Viene applicato l'ordinamento degli elementi. Non tutti gli elementi sono in tutti i profili, perché alcuni elementi sono facoltativi.

Questo elenco non Mostra tutti i possibili elementi che possono essere visualizzati in un profilo wireless, in quanto è possibile aggiungere elementi in **xs: qualsiasi** punto di inserimento.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**nome (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**esadecimale (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**nome (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**non broadcast (SSIDConfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (WLANProfile)**](wlan-profileschema-hotspot2-element.md)
        -   [**NomeDominio (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**NAIRealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**RoamingConsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (WLANProfile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**connectionMode (WLANProfile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**autoswitch (WLANProfile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**CSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**connettività (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phyType (connettività)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**sicurezza (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**authEncryption (sicurezza)**](wlan-profileschema-authencryption-security-element.md)
                -   [**autenticazione (authEncryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**crittografia (authEncryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useOneX (authEncryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (sicurezza)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**Tipo di sharedKey**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**protetto (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**Material (sharedKey)**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**Indice di indicizzazione (sicurezza)**](wlan-profileschema-keyindex-security-element.md)
            -   [**PMKCacheMode (sicurezza)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**PMKCacheTTL (sicurezza)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**PMKCacheSize (sicurezza)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**preAuthMode (sicurezza)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**preAuthThrottle (sicurezza)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (OUIHeader)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**tipo (OUIHeader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**connettività (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**sicurezza (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**useMSOneX (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



