---
title: Amministrazione della peer cache
description: Nota A partire Windows 7, il modello di peer caching Servizio trasferimento intelligente in background (BITS) 3.0 è deprecato.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3821cc0894754b8dbc2ee9f9a189381ac69030d39938c8f6cb4bc52625ef03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588751"
---
# <a name="administering-the-peer-cache"></a>Amministrazione della peer cache

> [!Note]  
> A partire Windows 7, il modello di peer caching Servizio trasferimento intelligente in background (BITS) 3.0 è deprecato. Se BITS 4.0 è installato, il modello di peer caching BITS 3.0 non è disponibile.

 

Per migliorare le prestazioni di download, BITS consente di scaricare contenuto da computer peer. Per abilitare questa funzionalità, l'amministratore deve abilitare l'impostazione di Criteri di gruppo EnablePeerCaching. Se abilitata, il peer può scaricare il contenuto dai peer e fornire contenuto ai peer. L'amministratore può anche usare le impostazioni dei criteri DisablePeerCachingClient e DisablePeerCachingServer per impedire rispettivamente il download di contenuto da un peer o la gestione del contenuto ai peer.

Se le impostazioni di Criteri di gruppo non sono configurate, un'applicazione può chiamare il metodo [**IBitsPeerCacheAdministration::SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) per impostare la preferenza di peer caching per il computer. Si noti che queste preferenze vengono sostituite dalle impostazioni di Criteri di gruppo se vengono impostate in un secondo momento. Per determinare se il computer abilita il peer caching, chiamare il metodo [**IBitsPeerCacheAdministration::GetConfigurationFlags.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags)

Se la peer caching è abilitata, BITS memorizza nella cache il contenuto di un processo solo se il processo consente in modo esplicito la memorizzazione nella cache del contenuto. BITS scarica anche il contenuto da un peer solo se il processo lo consente in modo esplicito. Per abilitare il peer caching per un processo, chiamare il [**metodo IBackgroundCopyJob4::SetPeerCachingFlags.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags)

Oltre a usare Criteri di gruppo o l'interfaccia [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) per abilitare il peer caching, è anche possibile usare uno dei due metodi per modificare le dimensioni predefinite della cache e l'intervallo di tempo per cui un file non accessibile rimane nella cache. Per modificare le impostazioni predefinite usando **l'interfaccia IBitsPeerCacheAdministration,** chiamare i [**metodi SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) e [**SetMaximumContentAge.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) Poiché questi metodi impostano le impostazioni delle preferenze, vengono sostituiti dalle impostazioni di Criteri di gruppo.

Per elencare i peer da cui BITS tenterà di scaricare il contenuto, chiamare il [**metodo IBitsPeerCacheAdministration::EnumPeers.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers)

Per elencare i file nella cache che BITS servirà ai peer, chiamare il [**metodo IBitsPeerCacheAdministration::EnumRecords.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords)

Non è mai necessario gestire la peer cache per quanto riguarda l'individuazione di peer o l'eliminazione dei record della cache. Questa funzionalità è stata inclusa [**nell'interfaccia IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) per completezza.

 

 




