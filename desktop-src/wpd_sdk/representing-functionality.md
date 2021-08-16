---
description: Rappresentazione della funzionalità
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Rappresentazione della funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f969bcf6352cd4eef02c1580a93bebcbf769953e2ae658243b4499e6d1ca763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842703"
---
# <a name="representing-functionality"></a>Rappresentazione della funzionalità

Esistono oggetti funzionali per identificare o raggruppare logicamente le funzionalità di un dispositivo. Ad esempio, un'applicazione può vedere che un dispositivo supporta SMS cercando l'oggetto funzionale SMS. Analogamente, l'applicazione può verificare che un dispositivo abbia funzionalità di fotocamera cercando l'oggetto funzionale Still Image Capture.

Questa rappresentazione flessibile degli oggetti consente di supportare facilmente i dispositivi con funzionalità multi-funzione. I driver possono semplicemente esporre tutti gli oggetti funzionali che rappresentano il dispositivo, che è più granulare rispetto all'uso delle classi di dispositivo tradizionali. La rappresentazione dell'oggetto consente anche di isolare parti funzionali sovrapposte; ad esempio, alcuni telefoni possono avere due fotocamere o quattro archivi.

Nel sistema Windows 7, i servizi estendono gli oggetti funzionali fornendo query avanzate di funzionalità e un raggruppamento astratto di contenuto. Le applicazioni possono usare i servizi per individuare le funzionalità dei dispositivi e interagire con il contenuto in modo più efficiente. Ad esempio, un'applicazione può vedere che un dispositivo supporta le funzionalità di sincronizzazione dei contatti cercando un oggetto servizio Contatti e può trovare tutti i contatti come oggetti figlio dell'oggetto servizio, senza dover eseguire ricerche ricorsive nella gerarchia di archiviazione.

I servizi consentono anche alle applicazioni di individuare e richiamare il comportamento personalizzato in un dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> </dl>

 

 



