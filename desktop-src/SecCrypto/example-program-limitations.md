---
description: Limitazioni del programma di esempio
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: Limitazioni del programma di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315388"
---
# <a name="example-program-limitations"></a>Limitazioni del programma di esempio

I principi delle procedure di programmazione valide non sono sempre seguiti in questi programmi di esempio per fornire codice più conciso e leggibile. In particolare:

-   Vengono visualizzate solo le risposte di errore limitate. I programmi di lavoro devono sempre controllare i codici di errore restituiti ed eseguire le azioni appropriate quando viene rilevato un errore.
-   Viene eseguita solo la memoria limitata e la gestione delle risorse. Nei programmi in esecuzione, tutti gli [*hash*](../secgloss/h-gly.md) e le chiavi devono essere eliminati, è necessario liberare tutta la memoria allocata, tutti i file devono essere chiusi e tutti gli handle devono essere rilasciati. Questi programmi di esempio forniscono solo dimostrazioni limitate dell'utilizzo di funzioni che eseguono queste attività. Questi programmi di esempio non eseguono attività di memoria o di gestione delle risorse in caso di interruzione del programma a causa di errori.

 

 
