---
description: Definisce un profilo WLAN utilizzato dal servizio AutoConfig Wifi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: WLAN_profile Schema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91bd1a5d04bcc265f2b9ba7c0533bb0beb4e2c861f01c8b5e286d59f8b4bcfc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619068"
---
# <a name="wlan_profile-schema"></a>Schema del profilo WLAN \_

Lo schema del profilo WLAN \_ definisce un profilo WLAN usato dal servizio AutoConfig Wifi nativo.

Il servizio AutoConfig accetta profili wireless da Criteri di gruppo Agent, dall'interfaccia di scripting (**netsh**), dall'interfaccia utente o dall'interfaccia di configurazione flash USB.

Un profilo ricevuto da uno di questi sistemi viene mappato allo schema del profilo WLAN e \_ archiviato nell'archivio profili. I profili possono essere esportati dall'archivio profili usando i comandi netsh o elementi API come [**WlanGetProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)

L'elemento radice di un profilo WLAN è [**l'elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md) Ogni profilo avrà esattamente un elemento radice. **L'elemento WLANProfile** si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v1` .

Per visualizzare i profili WLAN di esempio, vedere [Esempi di profili wireless.](wireless-profile-samples.md)

-   [Elementi dello schema del profilo WLAN \_](wlan-profileschema-elements.md)
-   [Tipi semplici dello schema del profilo WLAN \_](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comandi Netsh per la rete locale wireless (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
