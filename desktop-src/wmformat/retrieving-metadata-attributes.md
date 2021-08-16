---
title: Recupero degli attributi dei metadati
description: Recupero degli attributi dei metadati
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK, recupero degli attributi dei metadati
- Advanced Systems Format (ASF), recupero degli attributi dei metadati
- ASF (Advanced Systems Format), recupero degli attributi dei metadati
- metadati, recupero di attributi
- flussi, recupero di attributi di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dc24f06779c12d40a109c1a8ef0fee9811370d3459f3811c0c870ee535d749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807881"
---
# <a name="retrieving-metadata-attributes"></a>Recupero degli attributi dei metadati

Per recuperare un attributo da un'intestazione di file, è necessario conoscere il numero di flusso e l'indice dell'attributo. È possibile usare il [**metodo IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) per ottenere gli indici per tutti gli attributi con lo stesso nome o tutti gli indici nella stessa lingua. Come gli altri metodi di [**IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) **GetAttributeIndices** gestisce un singolo flusso o con tutti gli attributi a livello di file che usano il flusso 0. È possibile usare 0xFFFF per il numero di flusso per ottenere indici globali corrispondenti ai criteri nell'intero file, indipendentemente dal numero di flusso.

Quando si conosce l'indice dell'attributo da recuperare, chiamare [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) per ottenere l'attributo. È necessario effettuare due chiamate a **GetAttributeByIndexEx** per ogni attributo recuperato. Nella prima chiamata, passare **NULL per i** puntatori del nome e del buffer di dati per ottenere le dimensioni necessarie. Allocare quindi i buffer delle dimensioni indicate ed eseguire la seconda chiamata per recuperare il nome e i dati.

Per un esempio di codice che illustra come recuperare gli attributi dei metadati, vedere [To Retrieve All Metadata in a File](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




