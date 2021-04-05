---
title: Amministrazione della peer cache
description: Nota a partire da Windows 7, il modello di memorizzazione nella cache di peer Servizio trasferimento intelligente in background (BITS) 3,0 è deprecato.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b3ea1dd19c9aca855ffd73e174dcb3b588a54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708374"
---
# <a name="administering-the-peer-cache"></a>Amministrazione della peer cache

> [!Note]  
> A partire da Windows 7, il modello di memorizzazione nella cache di peer Servizio trasferimento intelligente in background (BITS) 3,0 è deprecato. Se è installato BITS 4,0, il modello di memorizzazione nella cache dei peer 3,0 BITS non è disponibile.

 

Per migliorare le prestazioni di download, BITS consente di scaricare il contenuto da computer peer. Per abilitare questa funzionalità, l'amministratore deve abilitare l'impostazione di criteri di gruppo EnablePeerCaching. Se abilitata, il peer può scaricare il contenuto dai peer e distribuire il contenuto ai peer. L'amministratore può anche usare le impostazioni dei criteri DisablePeerCachingClient e DisablePeerCachingServer per impedire il download di contenuto da un peer o il contenuto a peer, rispettivamente.

Se le impostazioni di criteri di gruppo non sono configurate, un'applicazione può chiamare il metodo [**IBitsPeerCacheAdministration:: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) per impostare la preferenza per la memorizzazione nella cache del peer per il computer. Si noti che queste preferenze vengono sostituite dalle impostazioni di criteri di gruppo se vengono impostate in un secondo momento. Per determinare se il computer consente la memorizzazione nella cache peer, chiamare il metodo [**IBitsPeerCacheAdministration:: GetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) .

Se la memorizzazione nella cache peer è abilitata, BITS memorizza nella cache solo il contenuto di un processo se il processo ne consente la memorizzazione nella cache in modo esplicito. BITS consente inoltre di scaricare il contenuto da un peer solo se il processo lo consente in modo esplicito. Per abilitare la memorizzazione nella cache peer per un processo, chiamare il metodo [**IBackgroundCopyJob4:: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) .

Oltre a usare Criteri di gruppo o l'interfaccia [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) per abilitare la memorizzazione nella cache peer, è anche possibile usare uno dei due metodi per modificare la dimensione della cache predefinita e il periodo di tempo in cui un file non accessibile rimane nella cache. Per modificare le impostazioni predefinite usando l'interfaccia **IBitsPeerCacheAdministration** , chiamare i metodi [**SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) e [**SetMaximumContentAge**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) . Poiché questi metodi impostano le impostazioni preferenza, vengono sostituiti dalle impostazioni di criteri di gruppo.

Per elencare i peer da cui BITS tenterà di scaricare il contenuto, chiamare il metodo [**IBitsPeerCacheAdministration:: EnumPeers**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) .

Per elencare i file nella cache che i bit serviranno ai peer, chiamare il metodo [**IBitsPeerCacheAdministration:: EnumRecords**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) .

Non è mai necessario gestire la peer cache per quanto riguarda l'individuazione di peer o l'eliminazione di record della cache. Questa funzionalità è stata inclusa nell'interfaccia [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) per completezza.

 

 




