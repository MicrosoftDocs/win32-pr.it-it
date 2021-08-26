---
title: Funzionalità di lettura file
description: Funzionalità di lettura file
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK, funzionalità di lettura file
- Windows Media Format SDK, lettura asincrona dei file
- Windows Media Format SDK, lettura sincrona di file
- Advanced Systems Format (ASF), funzionalità di lettura file
- ASF (Advanced Systems Format), funzionalità di lettura file
- Advanced Systems Format (ASF), lettura asincrona dei file
- ASF (Advanced Systems Format), lettura asincrona dei file
- Advanced Systems Format (ASF), lettura sincrona di file
- ASF (Advanced Systems Format), lettura sincrona di file
- lettura asincrona di file
- lettura sincrona di file
- lettori sincroni, funzionalità di lettura file
- lettura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8efb7bc0fca898c1a63db586b158b39b4bb9daa9ad051e7a61fe8c4a5d6b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930531"
---
# <a name="file-reading-features"></a>Funzionalità di lettura file

La lettura dei file ASF è una delle funzionalità principali di Windows Media Format SDK. Sono supportati due tipi di lettura: asincrona e sincrona. La lettura asincrona dei file viene gestita dall'oggetto reader. L'oggetto lettore sincrono viene usato per leggere i file in modo sincrono. Per altre informazioni sui diversi oggetti di lettura, vedere [Oggetto Lettore](reader-object.md) e [Oggetto lettore sincrono](synchronous-reader-object.md).

Nello scenario di lettura asincrona dei file più semplice, è necessario implementare un metodo di callback che l'oggetto lettore chiamerà quando gli esempi sono pronti. Dopo aver iniziato a leggere un file, l'applicazione attende che gli esempi siano recapitati al metodo di callback. La lettura asincrona è utile per le applicazioni lettore e supporta funzionalità non disponibili con la lettura sincrona. Se l'applicazione deve leggere i file da un percorso di rete o interagire con un server che esegue Servizi Windows Media, è necessario usare l'oggetto lettore. Lo svantaggio dell'oggetto lettore è che viene usato un thread separato per ogni output recapitato. Inoltre, l'oggetto lettore non è flessibile come il lettore sincrono nel modo in cui può distribuire gli esempi.

Con il lettore sincrono non è necessario usare alcun metodo di callback. Al contrario, si seleziona una parte del file da leggere e recuperare gli esempi uno alla volta con le chiamate al metodo . Il lettore sincrono è adatto alle esigenze delle applicazioni di modifica del contenuto, in cui è essenziale l'accesso rapido a esempi specifici. Poiché il lettore sincrono non usa metodi di callback, è possibile creare applicazioni per leggere i file ASF con un sovraccarico minimo per la scrittura del codice. Tuttavia, il lettore sincrono non può aprire un file da un percorso di rete o interagire con un server che esegue Servizi Windows Media o leggere i file protetti con [*DRM*](wmformat-glossary.md).

Negli argomenti seguenti vengono illustrate le funzionalità del lettore e del lettore sincrono.



| Argomento                                                              | Descrizione                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Supporto di esempio allocato dall'utente](user-allocated-sample-support.md) | Viene illustrata l'allocazione del buffer nel lettore e nel lettore sincrono e viene illustrato come l'allocazione utente può migliorare le prestazioni. |
| [Enumerazione del formato di output](output-format-enumeration.md)         | Viene illustrata l'enumerazione del formato di output.                                                                               |



 

Inoltre, gli argomenti seguenti della sezione relativa alle funzionalità di scrittura si applicano anche alla lettura di file:

-   [Ridimensionamento video](video-resizing.md)
-   [Conversione dello spazio colori](color-space-conversion.md)
-   [Ricampionamento audio](audio-resampling.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità**](features.md)
</dt> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




