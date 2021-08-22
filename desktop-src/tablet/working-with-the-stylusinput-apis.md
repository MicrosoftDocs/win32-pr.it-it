---
description: La classe RealTimeStylus consente di interagire con il flusso di dati dalla penna del tablet. Per interagire con il flusso di dati, aggiungere un oggetto RealTimeStylus all'applicazione e aggiungere plug-in all'oggetto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Uso delle API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143cb885cda16542a65aa096cdf95eb8a187b4f760a916a895887737ec63d7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842841"
---
# <a name="working-with-the-stylusinput-apis"></a>Uso delle API StylusInput

La [**classe RealTimeStylus**](realtimestylus-class.md) consente di interagire con il flusso di dati dalla penna del tablet. Per interagire con il flusso di dati, aggiungere un oggetto **RealTimeStylus** all'applicazione e aggiungere plug-in **all'oggetto RealTimeStylus.**

I plug-in possono modificare i dati associati a pacchetti in air, stilo verso il basso, pacchetti e metodi di notifica dello stilo up. I plug-in possono annullare i metodi di notifica dei pacchetti in ingresso e dei pacchetti. I plug-in possono anche aggiungere dati dell'applicazione al flusso sotto forma [di oggetti CustomStylusData.](/previous-versions/ms575208(v=vs.100)) L'elenco seguente offre idee per categorie comuni di plug-in che è possibile usare o creare.

-   Plug-in di filtro: oggetto che rimuove o annulla in modo selettivo i dati nel flusso di dati della penna del tablet.
-   Plug-in modificatore: oggetto che modifica in modo selettivo i dati nel flusso di dati della penna del tablet.
-   Plug-in renderer dinamico: oggetto che visualizza i dati della penna del tablet in tempo reale mentre vengono gestiti [**dall'oggetto RealTimeStylus.**](realtimestylus-class.md) In seguito, per eventi come l'aggiornamento di un modulo, il plug-in renderer dinamico o un plug-in di raccolta input penna potrebbe ridisegnare l'input penna.
-   Plug-in riconoscimento: oggetto che analizza il movimento della penna del tablet per individuare movimenti, grafia o altri glifi.
-   Plug-in dell'agente di raccolta input penna: oggetto che dal flusso di dati della penna del tablet crea e archivia l'input penna.
-   Plug-in wrapper: plug-in che funge da interfaccia tra l'oggetto [**RealTimeStylus**](realtimestylus-class.md) e un altro plug-in o oggetto come modo per modificare il comportamento dell'oggetto di cui è stato eseguito il wrapping.

È possibile creare plug-in dynamic-renderer e ink-collection per eseguire il rendering in vari contesti, ad esempio in un file, in un flusso o in un dispositivo di visualizzazione. L'input penna può anche essere archiviato in vari formati, ad esempio un oggetto [Ink,](/previous-versions/aa515768(v=msdn.10)) un file di Graphics Interchange Format (GIF), un file Ink Serialized Format (ISF) o altri formati.

Con le API StylusInput vengono forniti due plug-in: [**la classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e la [**classe GestureRecognizer.**](gesturerecognizer-class.md) La **classe DynamicRenderer** fornisce il rendering di base dei dati dell'input penna in tempo reale ed è semplificata per avere un impatto minimo sulle prestazioni. La **classe GestureRecognizer** fornisce il riconoscimento del movimento per [**la classe RealTimeStylus.**](realtimestylus-class.md)

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso della classe RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Plug-in e classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Note sull'implementazione per le API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Plug-in di raccolta input penna](ink-collection-plug-ins.md)
-   [Plug-in dynamic-renderer](dynamic-renderer-plug-ins.md)
-   [Plug-in di riconoscimento](recognizer-plug-ins.md)

 

 
