---
title: Funzionalità dei metadati
description: I metadati vengono utilizzati nei file ASF per descrivere il contenuto e le proprietà del file.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK, funzionalità dei metadati
- Windows Media Format SDK, funzionalità
- ASF (Advanced Systems Format), funzionalità dei metadati
- ASF (Advanced Systems Format), funzionalità dei metadati
- ASF (Advanced Systems Format), funzionalità
- ASF (Advanced Systems Format), funzionalità
- metadati, funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398762"
---
# <a name="metadata-features"></a>Funzionalità dei metadati

I metadati vengono utilizzati nei file ASF per descrivere il contenuto e le proprietà del file. Tutti i file ASF creati devono includere i metadati appropriati. Per una panoramica, vedere [metadati](metadata.md). Windows Media Format SDK include il supporto per la modifica dei metadati tramite l'oggetto writer, l'oggetto editor dei metadati e gli oggetti Reader e Reader sincroni. È incluso il supporto nativo per un'ampia gamma di attributi di metadati. Vedere [attributi](attributes.md) per un elenco degli attributi predefiniti.

Il supporto dei metadati fornito dai vari oggetti di Windows Media Format SDK è flessibile e potente. Le funzionalità principali dei metadati sono riepilogate nell'elenco seguente:

-   Dimensioni degli attributi flessibili. Le dimensioni degli attributi dei metadati non sono limitate.
-   Attributi a livello di flusso. I metadati nei file ASF possono essere assegnati al file nel suo complesso o a un determinato flusso.
-   Attributi duplicati. Un attributo denominato può essere utilizzato più volte nello stesso file. Questa funzionalità viene usata in particolare quando si assegnano attributi descrittivi del contenuto. Ad esempio, un brano può avere più autori, ognuno dei quali richiede un attributo **Author** separato nel file.
-   Più lingue. A ogni attributo è associata una lingua. È possibile impostare le lingue supportate e assegnarne una a ogni attributo che si scrive. Poiché è possibile duplicare gli attributi, è possibile fornire gli attributi più importanti in diversi linguaggi per raggiungere un numero maggiore di destinatari. Se non si specifica una lingua, verrà usata la lingua predefinita, ottenuta dal sistema operativo del computer che esegue l'applicazione.
-   Attributi complessi. Alcuni degli attributi predefiniti supportano i dati strutturati. Per questi attributi, il tipo di dati è binario, ma il valore è una struttura definita in questo SDK.

Negli argomenti seguenti vengono illustrate le altre funzionalità di metadati supportate.



| Argomento                                  | Descrizione                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [Supporto ID3](id3.md)                 | Viene illustrato il supporto per i frame ID3 utilizzando gli oggetti di Windows Media Format SDK. |
| [Metadati personalizzati](custom-metadata.md) | Vengono illustrate le implicazioni dell'utilizzo di metadati personalizzati.                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità**](features.md)
</dt> <dt>

[**Interfaccia IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interfaccia IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**Interfaccia IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Metadati**](metadata.md)
</dt> </dl>

 

 




