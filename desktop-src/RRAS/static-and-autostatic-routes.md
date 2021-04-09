---
title: Route statiche e autostatiche
description: In genere, le route alle reti remote vengono ottenute in modo dinamico tramite protocolli di routing.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955751"
---
# <a name="static-and-autostatic-routes"></a>Route statiche e autostatiche

In genere, le route alle reti remote vengono ottenute in modo dinamico tramite protocolli di routing. Tuttavia, l'amministratore può anche eseguire il *seeding* della tabella di routing fornendo le route manualmente. Queste route sono denominate *static*. Una route statica è associata a un'interfaccia che rappresenta la rete remota. Diversamente dalle route dinamiche, le route statiche vengono mantenute anche se il router viene riavviato o l'interfaccia è disabilitata.

Una route *autostatic* viene ottenuta tramite un protocollo di routing, ma una volta ottenuta si comporta come una route statica. Il processo per ottenere le route autostatiche è il seguente: la gestione router IP o IPX invia una richiesta di aggiornamento delle informazioni di routing per un'interfaccia specifica da parte di un protocollo di routing. I risultati dell'aggiornamento vengono quindi convertiti in route statiche. Si noti che solo alcuni protocolli di routing supportano le richieste di aggiornamenti della route autostatic.

 

 




