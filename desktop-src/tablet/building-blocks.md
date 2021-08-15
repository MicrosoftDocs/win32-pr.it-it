---
description: La piattaforma Tablet PC genera diversi formati di persistenza utili come blocchi predefiniti per i formati elencati in precedenza. I formati seguenti vengono tutti generati e utilizzati usando i metodi Load e Save dell'oggetto Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Blocchi predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dbf34cc0159bdf2efe9b68255292a8b644ab10e684f44c11fa60d484bd45516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714291"
---
# <a name="building-blocks"></a>Blocchi predefiniti

La piattaforma Tablet PC genera diversi formati di persistenza utili come blocchi predefiniti per i formati elencati in precedenza. I formati seguenti vengono tutti generati e utilizzati usando i [**metodi**](/previous-versions/ms583670(v=vs.100)) [**Load**](/previous-versions/ms569609(v=vs.100)) e Save [**dell'oggetto**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) Ink.

-   Formato serializzato input penna (ISF): Ink Serialized Format (ISF) è la rappresentazione persistente più compatta dell'input penna. È possibile incorporare ISF in un formato di documento binario o spostarlo direttamente negli Appunti. L'input penna archiviato in ISF deve usare il sistema di coordinate predefinito, hiMETRIC, con l'asse verticale invertito.
-   ISF con codifica Base 64: è possibile usare isf con codifica Base 64 per codificare l'input penna direttamente in un file Extensible Markup Language (XML) o HTML.
-   Immagini Graphics Interchange Format (GIF) : l'immagine GIF fortificata è un file GIF che contiene ISF come metadati incorporati nel file. L'input penna generato come GIF unificata può essere visualizzato nelle applicazioni che non riconoscono l'input penna e tutti i dati dell'input penna vengono mantenuti se l'input penna torna a un'applicazione che riconosce l'input penna. Questo formato è ideale per il trasporto di contenuto input penna all'interno di un file HTML. L'input penna è disponibile per qualsiasi applicazione, indipendentemente dal fatto che l'applicazione riconosca o meno l'input penna.
-   CODIFICA BASE 64- GIF codificata: questo formato viene fornito agli sviluppatori che vogliono codificare l'input penna direttamente in un file XML o HTML e quindi convertire il file in un'immagine in un secondo momento. È possibile usarlo quando si vuole che un file XML generato contenga tutte le informazioni sull'input penna e che possa essere usato per generare codice HTML tramite Extensible Stylesheet Language Transformations (XSLT).
    > [!Note]  
    > La tecnologia di compressione e decompressione LZW è coperta da US Patent No. 4.558.302 e i suoi patenti correlati ed estere (collettivamente, i patenti LZW) di proprietà di Unisys Corporation. Microsoft Corporation ha ottenuto una licenza da Unisys in base ai patenti LZW per usare la tecnologia GIF e LZW in determinati prodotti Microsoft. Questa licenza, tuttavia, non si estende agli sviluppatori di terze parti che usano prodotti di sviluppo Microsoft, ad esempio microsoft toolkit e prodotti per lo sviluppo di linguaggi, per fornire gif in lettura/scrittura o qualsiasi altra funzionalità LZW nei propri prodotti. Gli sviluppatori di terze parti devono decidere se hanno bisogno di una licenza di Unisys per i propri prodotti.

     

Un'applicazione può generare uno di questi formati persistenti usando [Microsoft.Ink.Stroke.HitTest](/previous-versions/ms828460(v=msdn.10)) o il [metodo Microsoft.Ink.Ink.HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) per generare una raccolta di tratti e:

-   Aggiunta di questi tratti a un nuovo [**oggetto Ink**](/previous-versions/ms583670(v=vs.100)) usando il [metodo AddStrokesAtRectangle.](/previous-versions/ms569548(v=vs.100))
-   Generazione di un nuovo [**oggetto Ink**](/previous-versions/ms583670(v=vs.100)) tramite il [metodo ExtractStrokes.](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90))

Il primo converte il rettangolo di selezione nell'origine, mentre il secondo no. L'applicazione usa quindi [**il metodo Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto [**Ink.**](/previous-versions/ms583670(v=vs.100))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti sInk e tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
