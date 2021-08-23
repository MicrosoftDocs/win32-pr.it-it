---
title: Aggiunta di driver all'interno di un'applicazione
description: Aggiunta di driver all'interno di un'applicazione
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- gestione compressione audio,aggiunta di driver
- ACM (Audio Compression Manager),aggiunta di driver
- Esempi di ACM, aggiunta di driver
- aggiunta di driver
- Funzione acmDriverAdd
- driver globali
- driver locali
- gestione compressione audio,driver globali
- ACM (Audio Compression Manager),driver globali
- gestione compressione audio,driver locali
- ACM (Gestione compressione audio),driver locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4cce1310a487e772ac6f65680221f065335951d7d1d6c6dd22c4178c0d985f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692331"
---
# <a name="adding-drivers-within-an-application"></a>Aggiunta di driver all'interno di un'applicazione

Se è necessario che l'applicazione implementi internamente le proprie routine di compressione, l'applicazione può aggiungere driver ad ACM chiamando la [**funzione acmDriverAdd.**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) L'applicazione implementa il driver fornendo una funzione conforme al prototipo [**acmDriverProc.**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) Dopo che l'applicazione ha aggiunto il driver, l'applicazione può usare il driver tramite ACM come qualsiasi altro driver.

ACM considera i driver come globali o locali. Un'applicazione specifica se un driver deve essere aggiunto come globale o locale quando chiama **acmDriverAdd.** Esistono due differenze tra driver globali e locali:

-   I driver aggiunti come driver globali non vengono condivisi con altre applicazioni.
-   Un'applicazione può modificare direttamente la priorità di un driver globale (ma non di un driver locale) chiamando la [**funzione acmDriverPriority.**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) ACM esegue una ricerca in ordine di priorità quando cerca un driver appropriato per fornire un'implementazione di una chiamata di funzione. ACM assegna sempre ai driver locali una priorità più alta rispetto ai driver globali. Il driver locale aggiunto più di recente ha la priorità più alta.

 

 




