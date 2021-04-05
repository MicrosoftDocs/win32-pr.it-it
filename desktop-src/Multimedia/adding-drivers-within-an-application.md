---
title: Aggiunta di driver all'interno di un'applicazione
description: Aggiunta di driver all'interno di un'applicazione
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Gestione compressione audio (ACM), aggiunta di driver
- ACM (Gestione compressione audio), aggiunta di driver
- Esempi di ACM, aggiunta di driver
- Aggiunta di driver
- acmDriverAdd (funzione)
- driver globali
- driver locali
- Gestione compressione audio (ACM), driver globali
- ACM (Gestione compressione audio), driver globali
- Gestione compressione audio (ACM), driver locali
- ACM (Gestione compressione audio), driver locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044730"
---
# <a name="adding-drivers-within-an-application"></a>Aggiunta di driver all'interno di un'applicazione

Se è necessario che l'applicazione implementi le proprie routine di compressione internamente, l'applicazione può aggiungere driver all'ACM chiamando la funzione [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) . L'applicazione implementa il driver fornendo una funzione conforme al prototipo [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) . Dopo che l'applicazione ha aggiunto il driver, l'applicazione può utilizzare il driver tramite l'ACM, perché utilizzerebbe qualsiasi altro driver.

L'ACM considera i driver come globali o locali. Un'applicazione specifica se un driver deve essere aggiunto come globale o locale quando chiama **acmDriverAdd**. Esistono due differenze tra i driver globali e locali:

-   I driver aggiunti come driver globali non sono condivisi con altre applicazioni.
-   Un'applicazione può modificare direttamente la priorità di un driver globale, ma non di un driver locale, chiamando la funzione [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) . L'ACM esegue una ricerca con priorità durante la ricerca di un driver appropriato per fornire un'implementazione di una chiamata di funzione. L'ACM assegna sempre ai driver locali una priorità più alta rispetto ai driver globali. Il driver locale aggiunto più di recente ha la priorità più alta.

 

 




