---
title: Route statiche e autostatiche
description: In genere, le route alle reti remote vengono ottenute dinamicamente tramite protocolli di routing.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0206190c86c75e4e50ce390cf3f084db956671de6efebe21022151879362ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127831"
---
# <a name="static-and-autostatic-routes"></a>Route statiche e autostatiche

In genere, le route alle reti remote vengono ottenute dinamicamente tramite protocolli di routing. Tuttavia, l'amministratore può anche *eseguire il seed della* tabella di routing fornendo manualmente le route. Queste route sono denominate *statici*. Una route statica è associata a un'interfaccia che rappresenta la rete remota. A differenza delle route dinamiche, le route statiche vengono mantenute anche se il router viene riavviato o l'interfaccia è disabilitata.

Una *route autostatica* viene ottenuta tramite un protocollo di routing, ma una volta ottenuta si comporta come una route statica. Il processo per ottenere route autostatiche è il seguente: il gestore router IP o IPX esegua una richiesta di aggiornamento delle informazioni di routing per un'interfaccia specifica da parte di un protocollo di routing. I risultati dell'aggiornamento vengono quindi convertiti in route statiche. Si noti che solo determinati protocolli di routing supportano le richieste di aggiornamenti di route autostatici.

 

 




