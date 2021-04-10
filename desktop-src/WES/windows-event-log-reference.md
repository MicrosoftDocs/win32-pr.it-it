---
title: Riferimento al registro eventi di Windows
description: Di seguito sono riportati gli elementi di programmazione usati per creare un manifesto di strumentazione, creare risorse dal manifesto usato dal provider, ottenere i metadati di strumentazione in fase di esecuzione ed eseguire query sugli eventi da canali e file di log
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049121"
---
# <a name="windows-event-log-reference"></a>Riferimento al registro eventi di Windows

Di seguito sono riportati gli elementi di programmazione usati per creare un manifesto di strumentazione, creare risorse dal manifesto usato dal provider, ottenere i metadati di strumentazione in fase di esecuzione ed eseguire query sugli eventi da canali e file di log:

-   [Schema EventManifest](eventmanifestschema-schema.md)
-   [Schema dell'evento](eventschema-schema.md)
-   [Schema di query](queryschema-schema.md)
-   [Costanti registro eventi di Windows](windows-event-log-constants.md)
-   [Tipi di dati del registro eventi di Windows](windows-event-log-data-types.md)
-   [Enumerazioni del registro eventi di Windows](windows-event-log-enumerations.md)
-   [Funzioni del registro eventi di Windows](windows-event-log-functions.md)
-   [Strutture del registro eventi di Windows](windows-event-log-structures.md)
-   [Strumenti del registro eventi di Windows](windows-event-log-tools.md)

Per le applicazioni scritte con un linguaggio .NET, ad esempio C# o Visual Basic, vedere gli spazi dei nomi seguenti:

-   Per scrivere eventi, usare le classi e i metodi definiti nello spazio dei nomi [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   Per utilizzare eventi da un canale o da un registro eventi di Windows, utilizzare le classi e i metodi definiti nello spazio dei nomi [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

In alternativa all'utilizzo dello spazio dei nomi [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) per la scrittura di eventi, è possibile utilizzare l'argomento **-CS** o **-CSS** per fare in modo che il compilatore del messaggio generi il codice per la scrittura degli eventi. Per informazioni dettagliate, vedere [**compilatore di messaggi**](message-compiler--mc-exe-.md).
