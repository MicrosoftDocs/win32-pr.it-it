---
title: Recupero degli attributi dei metadati
description: Recupero degli attributi dei metadati
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK, recupero degli attributi dei metadati
- Formato di sistemi avanzati (ASF), recupero degli attributi dei metadati
- ASF (Advanced Systems Format), recupero degli attributi dei metadati
- metadati, recupero di attributi
- flussi, recupero di attributi di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046272"
---
# <a name="retrieving-metadata-attributes"></a>Recupero degli attributi dei metadati

Per recuperare un attributo da un'intestazione di file, è necessario conoscerne il numero di flusso e l'indice. È possibile usare il metodo [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) per ottenere gli indici per tutti gli attributi con lo stesso nome o tutti gli indici nella stessa lingua. Analogamente agli altri metodi di [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** gestisce un singolo flusso o con tutti gli attributi a livello di file che usano il flusso 0. È possibile usare 0xFFFF per il numero di flusso per ottenere gli indici globali che corrispondono ai criteri nell'intero file, indipendentemente dal numero di flusso.

Quando si conosce l'indice dell'attributo che si desidera recuperare, chiamare [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) per ottenere l'attributo. È necessario effettuare due chiamate a **GetAttributeByIndexEx** per ogni attributo recuperato. Alla prima chiamata, passare **null** per i puntatori al nome e al buffer dei dati per ottenere le dimensioni necessarie. Allocare quindi i buffer delle dimensioni indicate ed effettuare la seconda chiamata per recuperare il nome e i dati.

Per un esempio di codice che illustra come recuperare gli attributi di metadati, vedere [per recuperare tutti i metadati in un file](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




