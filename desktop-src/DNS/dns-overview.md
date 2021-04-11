---
title: Panoramica di DNS
description: DNS è un servizio standard del settore usato per individuare i computer in una rete basata su IP (Internet Protocol).
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470807a5775b022834a3ca2f0ee3f91db8bdd5de
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234917"
---
# <a name="dns-overview"></a>Panoramica di DNS

DNS è un servizio standard del settore usato per individuare i computer in una rete basata su IP (Internet Protocol). Le reti IP, ad esempio le reti Internet e Windows 2000, si basano su indirizzi numerici, ad esempio 207.46.131.137, per trasferire le informazioni in tutta la rete. Gli utenti di rete utilizzano nomi basati su caratteri, ad esempio `www.microsoft.com` . Pertanto, è necessario convertire gli indirizzi di tipo carattere o intuitivo ( `www.microsoft.com` ) negli indirizzi basati su numeri (207.46.131.137) che la rete è in grado di riconoscere. DNS è il servizio da scegliere in Windows 2000 per individuare le risorse e convertirle negli indirizzi IP corrispondenti.

DNS usa un database specializzato di record di risorse, comunemente noto semplicemente come RRs, per rispondere alle query di risoluzione dei nomi dei client. Prima del DNS, la risoluzione dei nomi su Internet è stata realizzata con il [*file hosts*](h-gly.md), che sono file creati manualmente che hanno associato nomi host con indirizzi IP.

Quando un nuovo client è stato aggiunto alla rete, un amministratore deve aggiornare manualmente il file host e quindi copiare (replicare) il file in tutti gli altri computer della rete, in modo che il nuovo host possa essere raggiunto da tutti. Con la crescita di Internet, questo tipo di risoluzione dei nomi era chiaramente insufficiente. la gestione era troppo complessa e non era [*scalabile*](s-gly.md). Il file degli host è diventato più grande e poiché ha usato uno [*spazio dei nomi flat*](f-gly.md) (vedere anche [spazio dei nomi](name-space.md)), non è stato possibile partizionarlo e deve essere distribuito interamente. La soluzione era DNS.

-   DNS ha sostituito lo spazio del nome flat del file host con uno [*spazio dei nomi gerarchico*](h-gly.md). Con uno spazio dei nomi gerarchico, le informazioni sui nomi host e gli indirizzi IP possono essere partizionate e distribuite. viene quindi realizzata la scalabilità. Ad esempio, nel dominio widgets.products.microsoft.com fittizio, la responsabilità della risoluzione dei nomi può essere partizionata in modo che vari server possano gestire la risoluzione dei nomi per diverse parti dello spazio dei nomi:
    -   Un server può essere responsabile della risoluzione della prima parte (microsoft.com) ed è quindi in grado di inviare la richiesta di risoluzione dei nomi al server DNS successivo nella gerarchia.
    -   Il server DNS successivo può essere responsabile della risoluzione della parte successiva dello spazio dei nomi (prodotti).
    -   Infine, la richiesta può essere trasmessa a un terzo server DNS responsabile della risoluzione dell'ultima parte del nome (widget).

I server DNS in ogni parte dello spazio dei nomi gerarchico devono mantenere un database di record di risorse per gli host, ma solo nella loro parte della gerarchia. In questo modo, il server (o i server) nella parte Products di widgets.products.microsoft.com gestisce RRs solo per i prodotti inclusi nello spazio dei nomi gerarchico, non per la parte microsoft.com o la parte widget dello spazio dei nomi.

 

 




