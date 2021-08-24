---
title: Tipi percepiti (funzionalità dell Windows legacy)
description: PerceivedType è una proprietà che classifica un elemento nell'indice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de2baa37a46a9bd78e6e8a7ad94806dffe3a918046253bb09d4dab6090838b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610831"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Tipi percepiti (funzionalità dell Windows legacy)

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

`PerceivedType` è una proprietà che classifica un elemento nell'indice. Questa classificazione è diversa dalla classificazione "tipo" usata dalla sintassi di [query avanzata,](-search-2x-wds-aqsreference.md) ma allo stesso modo consente agli utenti di perfezionare i risultati della ricerca. Il tipo AQS consente agli utenti di limitare la query di ricerca, mentre la proprietà PerceivedType consente agli utenti di filtrare il set di risultati.

## <a name="types"></a>Tipi

Usare la proprietà PerceivedType per classificare il tipo di file in modo che gli utenti possano filtrare i risultati della ricerca in base al tipo. L'output deve essere una delle stringhe seguenti:

-   contact
-   (DIP) interno
-   comunicazioni/posta elettronica
-   comunicazioni/calendario
-   communications/task
-   communications/im
-   documento
-   documento/nota
-   documento/testo
-   documento/foglio di calcolo
-   documento/presentazione
-   music
-   images
-   immagini/immagine
-   immagini/video
-   folder
-   programma

Ad esempio, quando si vuole creare un componente aggiuntivo filtro per un nuovo tipo di file di immagine, è necessario implementare quanto segue [**nell'interfaccia IFilter:**](/windows/desktop/api/filter/nn-filter-ifilter)

-   **GetChunk** per restituire un oggetto FULLPROPSPEC che include: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** per restituire un oggetto PROPVARIANT che include: VT \_ LPWSTR = "images/picture"

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Sviluppo di componenti aggiuntivi IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintassi di ricerca avanzata](-search-2x-wds-aqsreference.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
