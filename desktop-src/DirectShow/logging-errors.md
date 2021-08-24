---
description: Errori di registrazione
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Errori di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7402ade284f0d9a71b032f233276277dfdcd8c5e2844c85f03782caed101d095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685151"
---
# <a name="logging-errors"></a>Errori di registrazione

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

[DirectShow Editing Services](directshow-editing-services.md) (DES) fornisce un meccanismo predefinito per la registrazione degli errori che si verificano durante il caricamento, la costruzione o il rendering di un progetto DES. Questo articolo presenta un'applicazione console di esempio che carica un file di progetto XML e tenta di eseguirne il rendering. Se si verifica un errore, l'applicazione stampa un messaggio di errore nella finestra della console. Il codice di esempio presentato in questo articolo si basa sull'esempio fornito in Caricamento e anteprima di [un](loading-and-previewing-a-project.md)Project .

> [!Note]  
> L'applicazione non è necessaria per implementare la registrazione degli errori. DES non registra gli errori a meno che non venga richiesto in modo esplicito.

 

Questo articolo presuppone che si comprendi la programmazione client COM e il modello di sequenza temporale DES. È anche necessario comprendere le nozioni di base della programmazione a oggetti COM. Per informazioni sulle sequenze temporali in DES, vedere [Modello di sequenza temporale](the-timeline-model.md).

Questo articolo include le sezioni seguenti.

-   [Panoramica della registrazione degli errori](overview-of-error-logging.md)
-   [Creazione di una classe di registrazione degli errori](creating-an-error-logging-class.md)
-   [Implementazione di IAMErrorLog](implementing-iamerrorlog.md)
-   [Impostazione del log degli errori](setting-the-error-log.md)
-   [Registrazione degli errori DES: codice di esempio](des-error-logging--example-code.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei DirectShow di modifica](using-directshow-editing-services.md)
</dt> </dl>

 

 



