---
description: Errori di registrazione
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Errori di registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745970"
---
# <a name="logging-errors"></a>Errori di registrazione

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

[DirectShow editing Services](directshow-editing-services.md) (des) fornisce un meccanismo incorporato per la registrazione degli errori che si verificano durante il caricamento, la costruzione o il rendering di un progetto des. Questo articolo presenta un'applicazione console di esempio che carica un file di progetto XML e tenta di eseguirne il rendering. Se si verifica un errore, l'applicazione stampa un messaggio di errore nella finestra della console. Il codice di esempio presentato in questo articolo si basa sull'esempio fornito in [caricamento e anteprima di un progetto](loading-and-previewing-a-project.md).

> [!Note]  
> L'applicazione non è necessaria per implementare la registrazione degli errori. Il DES non registra gli errori a meno che non venga richiesto in modo esplicito.

 

Questo articolo presuppone che si conosca la programmazione dei client COM e il modello di sequenza temporale DES. Inoltre, è necessario comprendere le nozioni di base della programmazione di oggetti COM. Per informazioni sulle sequenze temporali in DES, vedere [il modello di sequenza temporale](the-timeline-model.md).

Questo articolo include le sezioni seguenti.

-   [Panoramica della registrazione degli errori](overview-of-error-logging.md)
-   [Creazione di una classe di registrazione degli errori](creating-an-error-logging-class.md)
-   [Implementazione di IAMErrorLog](implementing-iamerrorlog.md)
-   [Impostazione del log degli errori](setting-the-error-log.md)
-   [Registrazione degli errori DES: codice di esempio](des-error-logging--example-code.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



