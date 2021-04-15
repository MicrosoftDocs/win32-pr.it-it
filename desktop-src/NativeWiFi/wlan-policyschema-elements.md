---
description: Un profilo di criteri di rete LAN wireless (WLAN) nativo è costituito dagli elementi dello schema seguenti.
ms.assetid: e3f45b02-6aea-4df3-938e-c13e7c52ca04
title: Elementi dello schema WLAN_policy
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8346aab6aba209933b20790cf3747d5c0944f972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525764"
---
# <a name="wlan_policy-schema-elements"></a>\_Elementi dello schema del criterio WLAN

Un profilo di criteri di rete LAN wireless (WLAN) nativo è costituito dagli elementi dello schema seguenti. Tutti gli elementi denominati si trovano nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/policy/v1` .

Nell'elenco seguente vengono illustrati gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo. Viene applicato l'ordinamento degli elementi. Non tutti gli elementi sono in tutti i profili, perché alcuni elementi sono facoltativi.

Questo elenco non Mostra tutti i possibili elementi che possono essere visualizzati in un profilo, perché è possibile aggiungere elementi in **xs: qualsiasi** punto di inserimento.

-   [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
    -   [**nome (WLANPolicy)**](wlan-policyschema-name-wlanpolicy-element.md)
    -   [**Descrizione (WLANPolicy)**](wlan-policyschema-description-wlanpolicy-element.md)
    -   [**globalFlags (WLANPolicy)**](wlan-policyschema-globalflags-wlanpolicy-element.md)
        -   [**enableAutoConfig (globalFlags)**](wlan-policyschema-enableautoconfig-globalflags-element.md)
        -   [**showDeniedNetwork (globalFlags)**](wlan-policyschema-showdeniednetwork-globalflags-element.md)
        -   [**allowEveryoneToCreateAllUserProfiles (globalFlags)**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md)
    -   [**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
        -   [**Allow (networkFilter)**](wlan-policyschema-allowlist-networkfilter-element.md)
            -   [**rete (Consenti)**](wlan-policyschema-network-allowlist-element.md)
                -   [**NetworkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**blocco (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
            -   [**rete (blocco)**](wlan-policyschema-network-blocklist-element.md)
                -   [**NetworkName (networkItemType)**](wlan-policyschema-networkname-networkitemtype-element.md)
                -   [**networkType (networkItemType)**](wlan-policyschema-networktype-networkitemtype-element.md)
        -   [**denyAllIBSS (networkFilter)**](wlan-policyschema-denyallibss-networkfilter-element.md)
        -   [**denyAllESS (networkFilter)**](wlan-policyschema-denyalless-networkfilter-element.md)
    -   [**profilatura (WLANPolicy)**](wlan-policyschema-profilelist-wlanpolicy-element.md)

 

 



