---
title: Windows Informazioni di riferimento sul registro eventi
description: Di seguito sono riportati gli elementi di programmazione utilizzati per creare un manifesto di strumentazione, creare risorse dal manifesto utilizzato dal provider, ottenere metadati di strumentazione in fase di esecuzione ed eseguire query sugli eventi dai canali e dai file di log
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957791"
---
# <a name="windows-event-log-reference"></a>Windows Informazioni di riferimento sul registro eventi

Di seguito sono riportati gli elementi di programmazione utilizzati per creare un manifesto di strumentazione, creare risorse dal manifesto utilizzato dal provider, ottenere metadati di strumentazione in fase di esecuzione ed eseguire query sugli eventi dai canali e dai file di log:

-   [EventManifest Schema](eventmanifestschema-schema.md)
-   [Schema di eventi](eventschema-schema.md)
-   [Query Schema](queryschema-schema.md)
-   [Windows Costanti del registro eventi](windows-event-log-constants.md)
-   [Windows Tipi di dati del log eventi](windows-event-log-data-types.md)
-   [Windows Enumerazioni del log eventi](windows-event-log-enumerations.md)
-   [Windows Funzioni del registro eventi](windows-event-log-functions.md)
-   [Windows Strutture del log eventi](windows-event-log-structures.md)
-   [Windows Strumenti del registro eventi](windows-event-log-tools.md)

Per le applicazioni scritte con un linguaggio .NET, ad esempio C# o Visual Basic, vedere gli spazi dei nomi seguenti:

-   Per scrivere eventi, usare le classi e i metodi definiti nello spazio dei nomi [System.Diagnostics.Eventing.](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8)
-   Per utilizzare gli eventi da Windows canale o log del log eventi, usare le classi e i metodi definiti nello spazio dei nomi [System.Diagnostics.Eventing.Reader.](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true)

In alternativa all'uso dello spazio dei nomi [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) per scrivere eventi, è possibile usare l'argomento **-cs** o **-css** per fare in modo che il compilatore di messaggi generi il codice per scrivere gli eventi. Per informazioni dettagliate, vedere [**Compilatore di messaggi**](message-compiler--mc-exe-.md).
