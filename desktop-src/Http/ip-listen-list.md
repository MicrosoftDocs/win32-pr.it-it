---
title: Elenco di ascolto IP
description: Le API del server HTTP non vengono associate ad alcuna coppia di indirizzi IP e porte TCP fino a quando un utente non registra un UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955794"
---
# <a name="ip-listen-list"></a>Elenco di ascolto IP

Le API del server HTTP non vengono associate ad alcuna coppia di indirizzi IP e porte TCP fino a quando un utente non registra un UrlPrefix. Per impostazione predefinita, dopo aver immesso una registrazione nella coda di richieste, l'API del server HTTP viene associata alla porta specificata in UrlPrefix (ad esempio, la porta 80) per tutti gli indirizzi IP (tutti i \_ o INADDR6 \_ ) disponibili nel computer. I problemi si verificano quando le applicazioni di terze parti (che non usano le API del server HTTP) si associano alle coppie di indirizzi IP e porte 80 nel computer. L'API server HTTP consente di configurare l'elenco di indirizzi IP che associa e risolve questo problema di coesistenza. L'amministratore di sistema chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato sul valore HttpServiceConfigIPListenList per specificare l'elenco di ascolto IP. Gli indirizzi IPv4 e IPv6 possono essere aggiunti all'elenco. Gli indirizzi IP immessi si applicano a tutte le applicazioni nel computer che usano l'API del server HTTP e vengono mantenuti tra i riavvii del computer. Tuttavia, qualsiasi modifica alla configurazione dell'elenco di ascolto IP non viene eseguita in modo dinamico; nella maggior parte dei casi, potrebbe essere necessario un riavvio del sistema.

 

 




