---
description: Definisce un profilo WLAN utilizzato dal servizio di configurazione automatica WiFi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Schema WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128839"
---
# <a name="wlan_profile-schema"></a>\_Schema profilo WLAN

Lo \_ schema del profilo WLAN definisce un profilo WLAN utilizzato dal servizio di configurazione automatica WiFi nativo.

Il servizio di configurazione automatica accetta i profili wireless dall'agente di Criteri di gruppo, l'interfaccia di scripting (**netsh**), l'interfaccia utente o dall'interfaccia di configurazione flash USB.

Un profilo ricevuto da uno di questi sistemi viene mappato allo \_ schema del profilo WLAN e archiviato nell'archivio profili. I profili possono essere esportati dall'archivio profili usando i comandi netsh o usando elementi API, ad esempio [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

L'elemento radice di un profilo WLAN è l'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) . Ogni profilo avrà esattamente un elemento radice. L'elemento **WLANProfile** si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v1` .

Per visualizzare i profili WLAN di esempio, vedere esempi di profili [wireless](wireless-profile-samples.md).

-   [\_Elementi dello schema del profilo WLAN](wlan-profileschema-elements.md)
-   [\_Tipi semplici dello schema del profilo WLAN](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
