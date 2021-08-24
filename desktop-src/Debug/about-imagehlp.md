---
description: Le funzioni ImageHlp vengono usate principalmente da strumenti di programmazione, utilità di configurazione delle applicazioni e altri programmi che devono accedere ai dati contenuti in un'immagine PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Informazioni su ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aee63eba22293fe1fb56cb6608110f4343a0c6bc26a4be597bfbd884cdf87cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815651"
---
# <a name="about-imagehlp"></a>Informazioni su ImageHlp

Le funzioni ImageHlp vengono usate principalmente da strumenti di programmazione, utilità di configurazione delle applicazioni e altri programmi che devono accedere ai dati contenuti in un'immagine PE. Tutte le funzioni ImageHlp sono a thread singolo. Pertanto, le chiamate da più thread a questa funzione probabilmente comportano un comportamento imprevisto o un danneggiamento della memoria. Per evitare questo problema, è necessario sincronizzare tutte le chiamate simultanee da più thread a questa funzione.

Negli argomenti seguenti vengono descritte le immagini PE e le funzionalità fornite dalle funzioni ImageHlp.

-   [Formato PE](pe-format.md)
-   [Funzioni di accesso alle immagini](image-access-functions.md)
-   [Funzioni di integrità delle immagini](image-integrity-functions.md)
-   [Funzioni di modifica delle immagini](image-modification-functions.md)

 

 



