---
description: Un profilo criteri WLAN (Native Wifi Wireless LAN) è costituito dai seguenti elementi dello schema.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: WLAN_policy Schema Elements
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92bfca66e1eff2c8c180968c83b5dbb565d1d4aa27ace1ba89d1c70634d6e7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619546"
---
# <a name="wlan_policy-schema-elements"></a>Elementi dello \_ schema dei criteri WLAN

Un profilo criteri WLAN (Native Wifi Wireless LAN) è costituito dai seguenti elementi dello schema. Tutti gli elementi denominati sono nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/policy/v1` .

L'elenco seguente mostra gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo. Viene applicato l'ordinamento degli elementi. Non tutti gli elementi sono in ogni profilo, poiché alcuni elementi sono facoltativi.

Questo elenco non mostra tutti gli elementi possibili che possono essere visualizzati in un profilo, perché gli elementi possono essere aggiunti nei punti di inserimento **xs:any.**

-   [**Criteri WLAN**](wlan-policyschema-wlanpolicy-element.md)
    -   [**name (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**description (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**allowList (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**network (allowList)**](wlan-policyschema-network-allowlist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**blockList (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**network (blockList)**](wlan-policyschema-network-blocklist-element.md)
                -   [**networkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profileList (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



