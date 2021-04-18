---
title: Tipi percepiti (funzionalità legacy dell'ambiente Windows)
description: PerceivedType è una proprietà che classifica un elemento nell'indice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300898"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Tipi percepiti (funzionalità legacy dell'ambiente Windows)

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

`PerceivedType` è una proprietà che classifica un elemento nell'indice. Questa classificazione è diversa dalla classificazione "Kind" usata dalla sintassi di [query avanzata](-search-2x-wds-aqsreference.md) ma consente agli utenti di affinare i risultati della ricerca. Il tipo AQS consente agli utenti di limitare la query di ricerca mentre la proprietà PerceivedType consente agli utenti di filtrare il set di risultati.

## <a name="types"></a>Tipi

Utilizzare la proprietà PerceivedType per classificare il tipo di file in modo che gli utenti possano filtrare i risultati della ricerca in base al tipo. L'output deve essere una delle stringhe seguenti:

-   contact
-   (DIP) interno
-   comunicazioni/posta elettronica
-   comunicazioni/calendario
-   comunicazioni/attività
-   comunicazioni/messaggistica immediata
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

Ad esempio, quando si desidera creare un componente aggiuntivo filtro per un nuovo tipo di file immagine, è necessario implementare quanto segue nell'interfaccia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):

-   **GetChunk** per restituire un FULLPROPSPEC che include: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** per restituire un PROPVARIANT che include: VT \_ LPWSTR = "immagini/immagine"

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

 

 
