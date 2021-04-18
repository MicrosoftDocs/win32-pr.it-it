---
description: Sono disponibili diversi formati di persistenza generati dalla piattaforma Tablet PC che risultano utili come blocchi predefiniti per i formati elencati in precedenza. I formati seguenti vengono generati e utilizzati usando i metodi di caricamento e salvataggio dell'oggetto Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Blocchi predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305352"
---
# <a name="building-blocks"></a>Blocchi predefiniti

Sono disponibili diversi formati di persistenza generati dalla piattaforma Tablet PC che risultano utili come blocchi predefiniti per i formati elencati in precedenza. I formati seguenti vengono generati e utilizzati usando i metodi di [**caricamento**](/previous-versions/ms569609(v=vs.100)) e [**salvataggio**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto [**Ink**](/previous-versions/ms583670(v=vs.100)) .

-   Formato ISF (Ink Serialized Format): il formato ISF (Ink Serialized Format) è la rappresentazione permanente più compatta dell'input penna. È possibile incorporare ISF in un formato di documento binario o spostarlo direttamente negli Appunti. L'input penna archiviato in ISF deve usare il sistema di coordinate predefinito, ovvero HIMETRIC, con l'asse verticale invertito.
-   Base-64 con codifica ISF: è possibile usare l'ISF codificato in base 64 per codificare l'input penna direttamente in un file di Extensible Markup Language (XML) o HTML.
-   Fortificated Graphics Interchange Format (GIF): il GIF fortificato è un file GIF che contiene ISF come metadati incorporati all'interno del file. L'input penna generato come GIF fortificato può essere visualizzato in applicazioni che non riconoscono l'input penna e tutti i dati di input penna vengono conservati se l'input penna viene restituito a un'applicazione che riconosce l'input penna. Questo formato è ideale per il trasporto di contenuto input penna in un file HTML. L'input penna è disponibile per qualsiasi applicazione, indipendentemente dal fatto che l'applicazione riconosca l'input penna.
-   GIF fortificato con codifica base 64: questo formato viene fornito per gli sviluppatori che desiderano codificare l'input penna direttamente in un file XML o HTML e quindi convertire il file in un'immagine in un secondo momento. Questa operazione può essere utilizzata quando si desidera che un file XML generato contenga tutte le informazioni sull'input penna e venga utilizzato come metodo per generare codice HTML utilizzando Extensible Stylesheet Language Transformations (XSLT).
    > [!Note]  
    > La tecnologia di compressione e decompressione LZW è presumibilmente coperta dal brevetto US no. 4.558.302 e i brevetti correlati e le controparti straniere (collettivamente, i brevetti LZW) di proprietà di Unisys Corporation. Microsoft Corporation ha ottenuto una licenza da Unisys con i brevetti LZW per l'uso del GIF e della tecnologia LZW in alcuni prodotti Microsoft. Questa licenza, tuttavia, non si estende a sviluppatori di terze parti che utilizzano prodotti di sviluppo Microsoft, come Microsoft Toolkit e prodotti per lo sviluppo di linguaggi, per fornire in lettura/scrittura GIF o qualsiasi altra funzionalità LZW nei propri prodotti. Gli sviluppatori di terze parti devono stabilire la propria determinazione per la necessità di una licenza di Unisys per i propri prodotti.

     

Un'applicazione può generare uno di questi formati permanenti usando [Microsoft. Ink. Stroke. HitTest](/previous-versions/ms828460(v=msdn.10)) o il metodo [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) per generare una raccolta Strokes e uno dei seguenti:

-   Aggiunta di questi tratti a un nuovo oggetto [**Ink**](/previous-versions/ms583670(v=vs.100)) usando il metodo [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100)) .
-   Generazione di un nuovo oggetto [**Ink**](/previous-versions/ms583670(v=vs.100)) usando il metodo [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90)) .

Il primo converte il rettangolo di selezione nell'origine, mentre il secondo no. L'applicazione usa quindi il metodo [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) dell'oggetto [**Ink**](/previous-versions/ms583670(v=vs.100)) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti sInk e tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
