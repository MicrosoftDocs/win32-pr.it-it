---
title: Operazioni di eventi timer
description: Operazioni di eventi timer
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- timer multimediali, eventi
- timer, eventi
- Funzione timeSetEvent (funzione)
- timeKillEvent (funzione)
- avvio di eventi timer
- eventi timer singolo
- eventi timer periodici
- annullamento degli eventi del timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724799"
---
# <a name="timer-event-operations"></a>Operazioni di eventi timer

Dopo aver stabilito la risoluzione del timer dell'applicazione, è possibile avviare gli eventi del timer usando la funzione [**funzione timeSetEvent**](/previous-versions//dd757634(v=vs.85)) . Questa funzione restituisce un identificatore del timer che può essere utilizzato per arrestare o identificare gli eventi del timer. Uno dei parametri della funzione è l'indirizzo di una funzione di callback [**TimeProc**](/previous-versions//dd757631(v=vs.85)) che viene chiamata quando si verifica l'evento del timer.

Esistono due tipi di eventi del timer: *singolo* e *periodico*. Un singolo evento del timer si verifica una sola volta, dopo un numero specificato di millisecondi. Un evento timer periodico si verifica ogni volta che trascorre un numero specificato di millisecondi. L'intervallo tra gli eventi periodici è denominato *ritardo evento*. Gli eventi timer periodici con un ritardo evento di 10 millisecondi o meno utilizzano una parte significativa delle risorse della CPU.

La relazione tra la risoluzione di un evento timer e la lunghezza del ritardo dell'evento è importante negli eventi del timer. Se ad esempio si specifica una risoluzione di 5 e un ritardo evento 100, i servizi timer inviano una notifica alla funzione di callback dopo un intervallo compreso tra 95 e 105 millisecondi.

È possibile annullare un evento del timer attivo in qualsiasi momento tramite la funzione [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) . Assicurarsi di annullare tutti i timer in attesa prima di liberare la memoria che contiene la funzione di callback.

> [!Note]  
> Il timer multimediale viene eseguito nel proprio thread.

 

 

 