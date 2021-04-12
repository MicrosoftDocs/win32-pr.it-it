---
title: Utilizzo dei metadati
description: Utilizzo dei metadati
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK, panoramica dei metadati
- Advanced Systems Format (ASF), panoramica dei metadati
- ASF (Advanced Systems Format), panoramica dei metadati
- metadati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398770"
---
# <a name="working-with-metadata"></a>Utilizzo dei metadati

Il supporto dei metadati è fornito dall'oggetto writer, dagli oggetti Reader e Reader sincroni e dall'oggetto editor dei metadati. Per informazioni generali sui metadati, vedere [metadati](metadata.md). Per informazioni sulle funzionalità che supportano i metadati in Windows Media Format SDK, vedere [funzionalità dei metadati](metadata-features.md).

L'interfaccia per la modifica dei metadati è [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), che è possibile ottenere chiamando il metodo **QueryInterface** di qualsiasi interfaccia in uno degli oggetti elencati in precedenza. **IWMHeaderInfo3** eredita i metodi di [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2). I metodi di **IWMHeaderInfo3** che gestiscono gli attributi di metadati rappresentano un approccio diverso per accedere ai metadati rispetto a quello usato dai metodi di **IWMHeaderInfo**. Usare sempre i metodi più recenti.

I metadati in un file ASF sono identificati da un indice e da un numero di flusso. Agli attributi a livello di file viene assegnato un numero di flusso pari a 0. Nelle versioni precedenti di Windows Media Format SDK, gli attributi possono essere identificati in base al nome. Tuttavia, poiché è ora possibile duplicare i nomi di attributo all'interno di un flusso, questa operazione non è più possibile. È invece possibile recuperare tutti gli indici che corrispondono a un nome. Per altre informazioni, vedere [recupero di attributi di metadati](retrieving-metadata-attributes.md).

Per semplificare la ricerca rapida degli attributi, è possibile usare un numero di flusso speciale, 0xFFFF. Usare questo numero di flusso per identificare il file nel suo complesso, anziché uno specifico flusso o gli attributi a livello di file. Gli oggetti di Windows Media Format SDK mantengono indici distinti per ogni flusso e per gli attributi a livello di file. Quando si usa Stream 0xFFFF, gli indici sono diversi da quelli usati quando si specifica un flusso specifico. Ad esempio, l'attributo che è index 0 per stream 0 non corrisponderà all'attributo index 0 per Stream 0xFFFF.

Le sezioni seguenti descrivono in modo più dettagliato l'uso dei metadati.



| Sezione                                                                    | Descrizione                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Recupero degli attributi dei metadati](retrieving-metadata-attributes.md)       | Viene descritto come leggere gli attributi dei metadati da un'intestazione di file.                     |
| [Impostazione degli attributi dei metadati](setting-metadata-attributes.md)             | Viene descritto come aggiungere nuovi attributi di metadati a un'intestazione di file.                    |
| [Modifica degli attributi dei metadati](editing-metadata-attributes.md)             | Viene descritto come modificare gli attributi di metadati esistenti.                               |
| [Rimozione degli attributi dei metadati](removing-metadata-attributes.md)           | Viene descritto come rimuovere gli attributi di metadati esistenti.                             |
| [Uso di attributi di metadati complessi](using-complex-metadata-attributes.md) | Viene descritto come utilizzare gli attributi i cui valori sono rappresentati da strutture. |



 

Diverse applicazioni di esempio illustrano come recuperare e modificare i metadati. In particolare, vedere l'esempio MetadataEdit, disponibile in entrambe le versioni di C++ e C#.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> <dt>

[**Applicazioni di esempio**](sample-applications.md)
</dt> </dl>

 

 




