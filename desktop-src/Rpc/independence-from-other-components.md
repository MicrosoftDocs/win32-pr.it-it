---
title: Indipendenza da altri componenti
description: I dati degli errori estesi sono utili anche quando il server o l'applicazione attraverso cui la catena è passata non riconosce i dati di errore estesi o non ne sfrutta i vantaggi. Alla fine di questa sezione vengono forniti gli approcci consigliati per tali situazioni.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Indipendenza da altri componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955759"
---
# <a name="independence-from-other-components"></a>Indipendenza da altri componenti

I dati degli errori estesi sono utili anche quando il server o l'applicazione attraverso cui la catena è passata non riconosce i dati di errore estesi o non ne sfrutta i vantaggi. Alla fine di questa sezione vengono forniti gli approcci consigliati per tali situazioni.

I dati degli errori estesi sono particolarmente utili quando le applicazioni o i server che usano RPC sfruttano le informazioni estese sugli errori. Quando si analizza un codice di errore di RPC \_ \_ \* e i server o le applicazioni in cui si verificano i dati di errore estesi non sono disponibili, considerare gli approcci seguenti:

-   Prendere una sniffata.

    Riprodurre lo scenario durante l'esecuzione dell'analisi. L'analisi della rete conterrà i dati di errore estesi.

-   Esaminarlo dal debugger.

    Se l'analisi del problema non funziona perché la chiamata è locale o perché l'errore ha origine localmente, connettere un debugger al processo che restituisce l'errore e inserire un punto di interruzione immediatamente dopo la chiamata RPC che ha generato l'errore. RPC spesso indica errori generando eccezioni, pertanto se si sta cercando l'errore 1825 ( \_ errore pkg di RPC S \_ sec \_ \_ ), abilitare l'eccezione 1825 e quando il debugger interrompe tale eccezione, esaminare le informazioni estese sull'errore per il thread.

 

 




