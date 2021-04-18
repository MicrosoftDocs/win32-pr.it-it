---
description: Le funzioni ImageHlp sono utilizzate principalmente da strumenti di programmazione, utilità di installazione dell'applicazione e altri programmi che richiedono l'accesso ai dati contenuti in un'immagine PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Informazioni su ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304570"
---
# <a name="about-imagehlp"></a>Informazioni su ImageHlp

Le funzioni ImageHlp sono utilizzate principalmente da strumenti di programmazione, utilità di installazione dell'applicazione e altri programmi che richiedono l'accesso ai dati contenuti in un'immagine PE. Tutte le funzioni ImageHlp sono a thread singolo. Pertanto, le chiamate da più thread a questa funzione potrebbero causare un comportamento imprevisto o un danneggiamento della memoria. Per evitare questo problema, è necessario sincronizzare tutte le chiamate simultanee da più di un thread a questa funzione.

Negli argomenti seguenti vengono descritte le immagini PE e la funzionalità fornita dalle funzioni ImageHlp.

-   [Formato PE](pe-format.md)
-   [Funzioni di accesso alle immagini](image-access-functions.md)
-   [Funzioni di integrità immagini](image-integrity-functions.md)
-   [Funzioni di modifica delle immagini](image-modification-functions.md)

 

 



