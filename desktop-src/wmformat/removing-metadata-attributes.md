---
title: Rimozione degli attributi dei metadati
description: Rimozione degli attributi dei metadati
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, rimozione degli attributi dei metadati
- Advanced Systems Format (ASF), rimozione degli attributi dei metadati
- ASF (Advanced Systems Format), rimozione degli attributi dei metadati
- metadati, rimozione di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e09e00fbba8ca5464ccec570a03bbd4e30935238bc531d36ce220a60150839e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110211"
---
# <a name="removing-metadata-attributes"></a>Rimozione degli attributi dei metadati

È possibile rimuovere un attributo di metadati passando l'indice e il numero di flusso al metodo [**IWMHeaderInfo3::D eleteAttribute.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) L'ordine in cui gli attributi rimanenti vengono indicizzati dopo la rimozione di un attributo non cambia; Tutti gli attributi rimanenti che originariamente avevano un valore di indice maggiore di quello rimosso hanno valori di indice ridotti di uno. Quando si rimuovono più attributi, eseguire questa operazione in ordine decrescente in base all'indice per evitare di dover calcolare la regolazione nell'indicizzazione.

Per praticità nella rimozione dei valori, il [**metodo IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) restituisce i valori di indice in ordine decrescente.

> [!Note]  
> I valori di indice ottenuti usando i metodi di [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) non sono compatibili con i valori di indice ottenuti usando i metodi di [**IWMHeaderInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) Se si usano i metodi di un'interfaccia per modificare gli attributi in un file, è necessario presupporre che tutti i valori di indice recuperati in precedenza dall'altra interfaccia non siano più validi e debbano essere ottenuti nuovamente. È consigliabile evitare di usare i metodi **di IWMHeaderInfo,** se possibile.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




