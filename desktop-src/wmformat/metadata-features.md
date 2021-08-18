---
title: Funzionalità dei metadati
description: I metadati vengono usati nei file ASF per descrivere il contenuto e le proprietà dei file.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK, funzionalità dei metadati
- Windows Media Format SDK, funzionalità
- Advanced Systems Format (ASF), funzionalità dei metadati
- ASF (Advanced Systems Format), funzionalità dei metadati
- Advanced Systems Format (ASF), funzionalità
- ASF (Advanced Systems Format), funzionalità
- metadati, funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6865e54f2eeabcb96dd88df27aba578a9169ed84857d17af5602848041f24118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700453"
---
# <a name="metadata-features"></a>Funzionalità dei metadati

I metadati vengono usati nei file ASF per descrivere il contenuto e le proprietà dei file. Tutti i file ASF creati devono includere i metadati appropriati. Per una panoramica, vedere [Metadati.](metadata.md) L Windows Media Format SDK include il supporto per la modifica dei metadati tramite l'oggetto writer, l'oggetto editor di metadati e gli oggetti reader e reader sincroni. È incluso il supporto nativo per un'ampia gamma di attributi di metadati. Per [un](attributes.md) elenco degli attributi predefiniti, vedere Attributi.

Il supporto dei metadati fornito dai vari oggetti di Windows Media Format SDK è flessibile e potente. Le principali funzionalità dei metadati sono riepilogate nell'elenco seguente:

-   Dimensioni flessibili dell'attributo. Le dimensioni degli attributi dei metadati non sono limitate.
-   Attributi a livello di flusso. I metadati nei file ASF possono essere assegnati al file nel suo complesso o a un flusso specifico.
-   Attributi duplicati. Un attributo denominato può essere usato più volte nello stesso file. Questa funzionalità è particolarmente utile quando si assegnano attributi descrittivi del contenuto. Ad esempio, un brano può avere diversi autori, ognuno dei quali richiede un **attributo Author** separato nel file.
-   Più lingue. A ogni attributo è associata una lingua. È possibile impostare le lingue supportate e quindi assegnarle a ogni attributo scritto. Poiché è possibile duplicare gli attributi, è possibile fornire gli attributi più importanti in diverse lingue per raggiungere un pubblico più ampio. Se non si specifica una lingua, verrà usata la lingua predefinita (ottenuta dal sistema operativo del computer che esegue l'applicazione).
-   Attributi complessi. Alcuni degli attributi predefiniti supportano i dati strutturati. Per questi attributi, il tipo di dati è binario, ma il valore è una struttura definita in questo SDK.

Negli argomenti seguenti vengono illustrate le altre funzionalità dei metadati supportate.



| Argomento                                  | Descrizione                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [Supporto ID3](id3.md)                 | Illustra il supporto per i fotogrammi ID3 usando gli oggetti di Windows Media Format SDK. |
| [Metadati personalizzati](custom-metadata.md) | Vengono illustrate le implicazioni dell'uso di metadati personalizzati.                                    |



 

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

 

 




