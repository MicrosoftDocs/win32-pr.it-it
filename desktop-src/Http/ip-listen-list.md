---
title: Elenco di ascolto IP
description: Le API del server HTTP non vengono associate ad alcuna coppia di indirizzi IP e porte TCP finché un utente non registra un UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dfc3f1763a9372911923cf24e50959bc6ac15e030c1b04daf3f81b45bff7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340521"
---
# <a name="ip-listen-list"></a>Elenco di ascolto IP

Le API del server HTTP non vengono associate ad alcuna coppia di indirizzi IP e porte TCP finché un utente non registra un UrlPrefix. Per impostazione predefinita, una volta immessa una registrazione nella coda delle richieste, l'API del server HTTP viene associata alla porta specificata in UrlPrefix (ad esempio la porta 80) per tutti gli indirizzi IP (INADDR ANY o \_ INADDR6 ANY) disponibili \_ nel computer. I problemi si verificano quando le applicazioni di terze parti (che non usano le API del server HTTP) si associano a coppie di indirizzo IP e porta 80 nel computer. L'API server HTTP consente di configurare l'elenco di indirizzi IP associati e risolve questo problema di coesistenza. L'amministratore di sistema chiama [**la funzione HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato sul valore HttpServiceConfigIPListenList per specificare l'elenco di ascolto IP. È possibile aggiungere all'elenco sia indirizzi IPv4 che indirizzi IPv6. Gli indirizzi IP immessi si applicano a tutte le applicazioni nel computer che usano l'API server HTTP e vengono mantenuti tra i riavvii del computer. Tuttavia, le modifiche alla configurazione dell'elenco di ascolto IP non vengono apportate in modo dinamico. Nella maggior parte dei casi può essere necessario un riavvio del sistema.

 

 




