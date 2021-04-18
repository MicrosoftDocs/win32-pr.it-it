---
title: Gestori COM
description: Lo scopo dei gestori COM è fornire alcuni \ 0034; Smart \ 0034; codice nello spazio degli indirizzi del client che può ottimizzare le chiamate tra un client e un server. I gestori possono eseguire l'override di alcune interfacce e delegare gli altri direttamente al server (tramite il proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297751"
---
# <a name="com-handlers"></a>Gestori COM

Lo scopo dei gestori COM è fornire codice "intelligente" nello spazio degli indirizzi del client in grado di ottimizzare le chiamate tra un client e un server. I gestori possono eseguire l'override di alcune interfacce e delegare gli altri direttamente al server (tramite il proxy).

Esistono due tipi di gestori COM:

-   [Il gestore OLE](the-ole-handler.md) è una DLL dei pesi massimi che fornisce importanti servizi per il collegamento e l'incorporamento. Viene in genere creato prima dell'avvio del server e viene inizializzato in modo che il server venga attivato quando l'oggetto incorporato entra nello stato in esecuzione.
-   [Il gestore leggero lato client](the-lightweight-client-side-handler.md) può essere creato per qualsiasi scopo, può essere molto piccolo e non può essere creato prima del server.

 

 




