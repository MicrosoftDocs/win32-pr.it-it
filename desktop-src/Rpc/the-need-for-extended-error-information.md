---
title: Necessità di informazioni estese sugli errori
description: Una delle principali difficoltà associate alla risoluzione dei problemi RPC consiste nel mapping di un codice di errore RPC al problema sottostante.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82fbbcaf0fac427b2bf64fbacbf1e85aeb4d06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044452"
---
# <a name="the-need-for-extended-error-information"></a>Necessità di informazioni estese sugli errori

Una delle principali difficoltà associate alla risoluzione dei problemi RPC consiste nel mapping di un codice di errore RPC al problema sottostante. Un problema di configurazione o di rete può comportare la ricezione di errori RPC da parte di una o più workstation \_ \_ \* , ma la workstation può solo visualizzare l'errore, parafrasarla o salvarla in un file di log. Indipendentemente dall'approccio usato, la persona che risolve il problema è priva di informazioni essenziali:

-   Dove si è verificato l'errore. Potrebbe essersi verificata nel computer locale, in un computer remoto chiamato dal computer locale o in un computer remoto chiamato da un altro computer remoto.
-   Codice di errore originale che ha causato il problema. Per essere conforme allo standard OSF, MS RPC esegue il mapping dei codici di errore ai \_ \_ \* codici RPC. \_ \_ \* Tuttavia, i codici RPC sono troppo generici e offrono poche informazioni utili per la risoluzione dei problemi.
-   Informazioni di contesto relative all'occorrenza del problema. Con gli errori non RPC, i debugger possono arrestare il processo ed esaminare il contesto in cui si è verificato l'errore. Gli errori RPC vengono spesso generati da un processo remoto o da un computer, che continua l'elaborazione dopo la restituzione dell'errore e sovrascrive qualsiasi contesto relativo all'errore.

 

 




