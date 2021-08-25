---
title: Operazioni degli eventi timer
description: Operazioni degli eventi timer
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- timer multimediali, eventi
- timer, eventi
- Funzione timeSetEvent
- Funzione timeKillEvent
- avvio di eventi timer
- eventi timer singoli
- eventi timer periodici
- annullamento di eventi timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3869015cdde4afe5bd77bb65d39d5ee43aeb4eab65b1f54e7bfd3dadca1a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370821"
---
# <a name="timer-event-operations"></a>Operazioni degli eventi timer

Dopo aver stabilito la risoluzione del timer dell'applicazione, è possibile avviare gli eventi timer usando la [**funzione timeSetEvent.**](/previous-versions//dd757634(v=vs.85)) Questa funzione restituisce un identificatore timer che può essere usato per arrestare o identificare gli eventi timer. Uno dei parametri della funzione è l'indirizzo di una funzione di callback [**TimeProc**](/previous-versions//dd757631(v=vs.85)) chiamata quando si verifica l'evento timer.

Esistono due tipi di eventi timer: *singolo* e *periodico.* Un singolo evento timer si verifica una volta, dopo un numero specificato di millisecondi. Ogni volta che è trascorso un numero specificato di millisecondi, si verifica un evento timer periodico. L'intervallo tra eventi periodici è detto ritardo *dell'evento*. Gli eventi timer periodici con un ritardo di 10 millisecondi o inferiore utilizzano una parte significativa delle risorse della CPU.

La relazione tra la risoluzione di un evento timer e la lunghezza del ritardo dell'evento è importante negli eventi timer. Ad esempio, se si specifica una risoluzione di 5 e un ritardo dell'evento di 100, i servizi timer inviano una notifica alla funzione di callback dopo un intervallo compreso tra 95 e 105 millisecondi.

È possibile annullare un evento timer attivo in qualsiasi momento usando la [**funzione timeKillEvent.**](/previous-versions//dd757630(v=vs.85)) Assicurarsi di annullare tutti i timer in sospeso prima di liberare la memoria contenente la funzione di callback.

> [!Note]  
> Il timer multimediale viene eseguito nel proprio thread.

 

 

 