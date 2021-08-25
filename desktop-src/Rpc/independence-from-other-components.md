---
title: Indipendenza da altri componenti
description: I dati degli errori estesi sono utili anche quando il server o l'applicazione tramite cui la catena passata non riconosce i dati degli errori estesi o non ne sfrutta i vantaggi. Gli approcci consigliati per tali situazioni sono disponibili alla fine di questa sezione.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Indipendenza da altri componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8174ffa0469550d3a7b274fb28f2f30dd807314e6bd596b75469f717f5924a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020451"
---
# <a name="independence-from-other-components"></a>Indipendenza da altri componenti

I dati degli errori estesi sono utili anche quando il server o l'applicazione tramite cui la catena passata non riconosce i dati degli errori estesi o non ne sfrutta i vantaggi. Gli approcci consigliati per tali situazioni sono disponibili alla fine di questa sezione.

I dati degli errori estesi sono particolarmente utili quando le applicazioni o i server che usano RPC sfruttano le informazioni sugli errori estesi. Quando si analizza un codice di errore RPC S e i server o le applicazioni coinvolte non rendono disponibili i dati degli errori estesi, prendere in considerazione \_ \_ \* gli approcci seguenti:

-   Eseguire un'analisi.

    Riprodurre lo scenario durante l'analisi. L'analisi della rete conterrà i dati degli errori estesi.

-   Esaminarlo dal debugger.

    Se l'analisi del problema non funziona perché la chiamata è locale o perché l'errore ha origine in locale, collegare un debugger al processo che restituisce l'errore e inserire un punto di interruzione immediatamente dopo la chiamata RPC che genera l'errore. RPC indica spesso errori generando eccezioni, quindi se si cerca l'errore 1825 (RPC S SEC PKG ERROR), abilitare l'eccezione \_ \_ \_ 1825 e quando il debugger si interrompe su tale eccezione, esaminare le informazioni sull'errore esteso per \_ il thread.

 

 




