---
title: Panoramica di DNS
description: DNS è un servizio standard del settore usato per individuare i computer in una rete basata su IP (Internet Protocol).
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a47874606491c1baf5c52ca7934d7e0c3156a6ab99f9726e6c000d9eb3cb65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967471"
---
# <a name="dns-overview"></a>Panoramica di DNS

DNS è un servizio standard del settore usato per individuare i computer in una rete basata su IP (Internet Protocol). Le reti IP, ad esempio Internet e le reti Windows 2000, si basano su indirizzi basati su numeri, ad esempio 207.46.131.137, per ottenere informazioni sui collegamenti in tutta la rete. Gli utenti di rete si basano su nomi basati su caratteri, ad esempio `www.microsoft.com` . Pertanto, è necessario convertire gli indirizzi di caratteri o descrittivi ( ) negli indirizzi basati su numeri `www.microsoft.com` (207.46.131.137) che la rete è in grado di riconoscere. DNS è il servizio preferito in Windows 2000 per individuare le risorse e convertirle nei rispettivi indirizzi IP corrispondenti.

DNS usa un database specializzato di record di risorse, comunemente definiti semplicemente RR, per rispondere alle query di risoluzione dei nomi dei client. Prima di DNS, la risoluzione dei nomi su Internet era ottenuta con il [*file hosts*](h-gly.md), che sono file creati manualmente che hanno associato i nomi host agli indirizzi IP.

Quando è stato aggiunto un nuovo client alla rete, un amministratore doveva aggiornare manualmente il file hosts e quindi copiare (replicare) il file in tutti gli altri computer della rete in modo che il nuovo host fosse raggiungibile da tutti. Con la crescita di Internet, questa forma di risoluzione dei nomi era chiaramente insufficiente; era troppo a elevato utilizzo di gestione e non ha [*ridimensionato*](s-gly.md). Il file hosts si è appena ingrandito e, poiché usava uno spazio dei nomi flat [*(vedere*](f-gly.md) anche Spazio dei [nomi),](name-space.md)non era possibile partizionarlo ed era necessario distribuirlo completamente. La soluzione era DNS.

-   DNS ha sostituito lo spazio dei nomi flat del file hosts con uno [*spazio dei nomi gerarchico*](h-gly.md). Con uno spazio dei nomi gerarchico, le informazioni sui nomi host e sugli indirizzi IP possono essere partizionate e distribuite; viene quindi ottenuta la scalabilità. Ad esempio, nel dominio fittizio widgets.products.microsoft.com, la responsabilità della risoluzione dei nomi può essere partizionata in modo che vari server possano gestire la risoluzione dei nomi per parti diverse dello spazio dei nomi:
    -   Un server può essere responsabile della risoluzione della prima parte (microsoft.com) e quindi può inoltrare la richiesta di risoluzione dei nomi al server DNS successivo nella gerarchia.
    -   Il server DNS successivo può essere responsabile della risoluzione della parte successiva dello spazio dei nomi (prodotti).
    -   Infine, la richiesta può essere inoltrata a un terzo server DNS responsabile della risoluzione dell'ultima parte del nome (widget).

I server DNS in ogni parte dello spazio dei nomi gerarchico devono mantenere un database di record di risorse per gli host, ma solo nella parte della gerarchia. Di conseguenza, il server (o i server) nella parte dei prodotti di widgets.products.microsoft.com gestisce le richieste r solo per i prodotti che fanno parte dello spazio dei nomi gerarchico, non per la parte microsoft.com o i widget dello spazio dei nomi.

 

 




