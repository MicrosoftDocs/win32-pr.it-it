---
title: Rimozione degli attributi dei metadati
description: Rimozione degli attributi dei metadati
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, rimozione degli attributi dei metadati
- ASF (Advanced Systems Format), rimozione degli attributi dei metadati
- ASF (Advanced Systems Format), rimozione degli attributi dei metadati
- metadati, rimozione di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398756"
---
# <a name="removing-metadata-attributes"></a>Rimozione degli attributi dei metadati

È possibile rimuovere un attributo di metadati passandone l'indice e il numero di flusso al metodo [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) . L'ordine in cui gli attributi rimanenti vengono indicizzati dopo la rimozione di un attributo non cambia; tutti gli attributi rimanenti che originariamente avevano un valore di indice maggiore di quello rimosso hanno i valori di indice ridotti di uno. Quando si rimuovono più attributi, eseguire questa operazione in ordine decrescente in base all'indice per evitare di dover calcolare la regolazione nell'indicizzazione.

Per praticità nella rimozione dei valori, il metodo [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) restituisce i valori di indice in ordine decrescente.

> [!Note]  
> I valori di indice ottenuti utilizzando i metodi di [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) non sono compatibili con i valori di indice ottenuti utilizzando i metodi di [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). Se si utilizzano i metodi di un'interfaccia per modificare gli attributi in un file, è necessario presupporre che tutti i valori di indice recuperati in precedenza dall'altra interfaccia non siano più validi e che sia necessario ottenerli nuovamente. Se possibile, è consigliabile evitare di usare i metodi di **IWMHeaderInfo** .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




