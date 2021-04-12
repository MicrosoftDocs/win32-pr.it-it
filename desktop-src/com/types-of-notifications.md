---
title: Tipi di notifiche
description: Tipi di notifiche
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396530"
---
# <a name="types-of-notifications"></a>Tipi di notifiche

Le notifiche rientrano in tre gruppi: documento composto, dati e visualizzazione. Un oggetto invia notifiche di documenti composti in risposta alla ridenominazione, al salvataggio, alla chiusura o, nel caso di un collegamento, con la ridenominazione dell'origine del collegamento. Come ci si aspetterebbe, gli oggetti inviano notifiche dati in risposta alle modifiche nei dati e inviano notifiche di visualizzazione in risposta alle modifiche nella presentazione. Le applicazioni contenitore devono essere registrate separatamente per ognuno di questi tipi di notifica, ma tutte possono essere gestite da un singolo sink consultivo.

Tutti i contenitori, il gestore dell'oggetto e il registro oggetti collegati per le notifiche dei documenti composti. Il contenitore tipico viene registrato anche per le notifiche di visualizzazione. Le notifiche dei dati vengono in genere inviate sia all'oggetto collegato che al gestore dell'oggetto. Un contenitore per scopi specifici, ad esempio quello che esegue il rendering dei dati, potrebbe trarre vantaggio dalla ricezione di notifiche di dati anziché da notifiche di visualizzazione. Ad esempio, un contenitore del grafico incorporato con un collegamento a una tabella può registrarsi per le notifiche dei dati. Poiché una modifica alla tabella influiscono sul grafico, la ricezione di una notifica dati indicherà al contenitore di ottenere i nuovi dati tabulari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Notifications](notifications.md)
</dt> </dl>

 

 




