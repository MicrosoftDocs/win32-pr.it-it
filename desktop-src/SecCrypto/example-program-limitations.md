---
description: Limitazioni del programma di esempio
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitazioni del programma di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0244f373264ed6886632979f00ace873949c1ab7e781262b4ef30dab2072f8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007439"
---
# <a name="example-program-limitations"></a>Limitazioni del programma di esempio

I principi di buona programmazione non vengono sempre seguiti in questi programmi di esempio per fornire codice più conciso e leggibile. In particolare:

-   Vengono visualizzate solo risposte di errore limitate. I programmi di lavoro devono sempre controllare i codici di errore restituiti ed eseguire le azioni appropriate quando viene rilevato un errore.
-   Viene eseguita solo la gestione limitata della memoria e delle risorse. Nei programmi funzionanti tutte le chiavi e [*gli hash*](../secgloss/h-gly.md) devono essere distrutti, tutta la memoria allocata deve essere liberata, tutti i file devono essere chiusi e tutti gli handle devono essere rilasciati. Questi programmi di esempio forniscono solo dimostrazioni limitate dell'uso di funzioni che eseguono queste attività. Questi programmi di esempio non eseguono attività di gestione della memoria o delle risorse in caso di chiusura del programma a causa di errori.

 

 
