---
title: Funzionalità di lettura file
description: Funzionalità di lettura file
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK, funzionalità di lettura file
- Windows Media Format SDK, lettura asincrona dei file
- Windows Media Format SDK, lettura di file sincroni
- ASF (Advanced Systems Format), funzionalità di lettura dei file
- ASF (Advanced Systems Format), funzionalità di lettura dei file
- ASF (Advanced Systems Format), lettura asincrona dei file
- ASF (formato avanzato dei sistemi), lettura asincrona dei file
- ASF (Advanced Systems Format), lettura di file sincroni
- ASF (formato avanzato dei sistemi), lettura sincrona dei file
- lettura asincrona di file
- lettura di file sincroni
- lettori sincroni, funzionalità di lettura file
- lettura file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332319"
---
# <a name="file-reading-features"></a>Funzionalità di lettura file

La lettura dei file ASF è una delle funzionalità principali di Windows Media Format SDK. Sono supportati due tipi di lettura: asincrono e sincrono. La lettura asincrona dei file viene gestita dall'oggetto Reader. L'oggetto Reader sincrono viene utilizzato per leggere i file in modo sincrono. Per ulteriori informazioni sui diversi oggetti di lettura, vedere [oggetto Reader](reader-object.md) e [oggetto Reader sincrono](synchronous-reader-object.md).

Nello scenario di lettura del file asincrono più semplice, è necessario implementare un metodo di callback che l'oggetto Reader chiamerà quando gli esempi sono pronti. Una volta iniziata la lettura di un file, l'applicazione attende che gli esempi vengano recapitati al metodo di callback. La lettura asincrona è utile per le applicazioni del lettore e supporta le funzionalità non disponibili con la lettura sincrona. Se l'applicazione deve leggere i file da un percorso di rete o interagire con un server che esegue Servizi Windows Media, è necessario usare l'oggetto Reader. Lo svantaggio dell'oggetto Reader è che per ogni output fornito viene utilizzato un thread separato. Inoltre, l'oggetto Reader non è flessibile come il lettore sincrono in come può fornire esempi.

Con il lettore sincrono non è necessario utilizzare alcun metodo di callback. Al contrario, è possibile selezionare una parte del file per leggere e recuperare gli esempi uno alla volta con le chiamate al metodo. Il lettore sincrono è particolarmente adatto alle esigenze delle applicazioni di modifica del contenuto, in cui l'accesso rapido a specifici esempi è essenziale. Poiché nessun metodo di callback viene utilizzato dal lettore sincrono, è possibile creare applicazioni per leggere i file ASF con un sovraccarico di codifica minimo. Tuttavia, il lettore sincrono non è in grado di aprire un file da un percorso di rete o interagire con un server che esegue Servizi Windows Media oppure leggere file protetti con [*DRM*](wmformat-glossary.md).

Negli argomenti seguenti vengono illustrate le funzionalità del lettore e del lettore sincrono.



| Argomento                                                              | Descrizione                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Supporto di esempio allocato dall'utente](user-allocated-sample-support.md) | Viene descritta l'allocazione del buffer nel Reader e nel lettore sincrono e il modo in cui l'allocazione utente può migliorare le prestazioni |
| [Enumerazione del formato di output](output-format-enumeration.md)         | Descrive l'enumerazione del formato di output.                                                                               |



 

Inoltre, gli argomenti seguenti della sezione relativa alla scrittura di funzionalità si applicano anche alla lettura di file:

-   [Ridimensionamento video](video-resizing.md)
-   [Conversione dello spazio colore](color-space-conversion.md)
-   [Ricampionamento audio](audio-resampling.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità**](features.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




