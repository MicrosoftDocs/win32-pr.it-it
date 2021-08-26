---
title: Uso dei metadati
description: Uso dei metadati
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows MEDIA Format SDK, panoramica dei metadati
- Advanced Systems Format (ASF), panoramica dei metadati
- ASF (Advanced Systems Format), panoramica dei metadati
- metadati, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c001eed5330d3d90cdbf42cc52cfef3f048a25f7d8f72fe4402a48ccbb42480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109881"
---
# <a name="working-with-metadata"></a>Uso dei metadati

Il supporto dei metadati viene fornito dall'oggetto writer, dal lettore e dagli oggetti lettore sincroni e dall'oggetto editor di metadati. Per informazioni generali sui metadati, vedere [Metadati](metadata.md). Per informazioni sulle funzionalità che supportano i metadati in Windows Media Format SDK, vedere [Funzionalità dei metadati](metadata-features.md).

L'interfaccia per la modifica dei metadati [**è IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)che è possibile ottenere chiamando il **metodo QueryInterface** di qualsiasi interfaccia in uno degli oggetti elencati in precedenza. **IWMHeaderInfo3** eredita i metodi di [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) I metodi di **IWMHeaderInfo3** che si occupano degli attributi dei metadati rappresentano un approccio diverso all'accesso ai metadati rispetto a quello usato dai metodi di **IWMHeaderInfo.** È consigliabile usare sempre i metodi più nuovi.

I metadati in un file ASF sono identificati da un indice e da un numero di flusso. Agli attributi a livello di file viene assegnato un numero di flusso 0. Nelle versioni precedenti di Windows Media Format SDK, gli attributi potevano essere identificati in base al nome. Tuttavia, poiché è ora possibile duplicare i nomi degli attributi all'interno di un flusso, questo non è più possibile. È invece possibile recuperare tutti gli indici corrispondenti a un nome. Per altre informazioni, vedere [Recupero di attributi di metadati.](retrieving-metadata-attributes.md)

Per facilitare la ricerca rapida degli attributi, è possibile usare un numero di flusso speciale, 0xFFFF. Usare questo numero di flusso per identificare il file nel suo complesso, anziché un flusso specifico o gli attributi a livello di file. Gli oggetti dell'SDK Windows Media Format mantengono indici separati per ogni flusso e per gli attributi a livello di file. Quando si usano 0xFFFF flusso, gli indici sono diversi da quelli utilizzati quando si specifica un flusso specifico. Ad esempio, l'attributo con indice 0 per il flusso 0 non corrisponde all'attributo che corrisponde all'indice 0 per il flusso 0xFFFF.

Le sezioni seguenti descrivono l'uso dei metadati in modo più dettagliato.



| Sezione                                                                    | Descrizione                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Recupero degli attributi dei metadati](retrieving-metadata-attributes.md)       | Viene descritto come leggere gli attributi dei metadati da un'intestazione di file.                     |
| [Impostazione degli attributi dei metadati](setting-metadata-attributes.md)             | Viene descritto come aggiungere nuovi attributi di metadati a un'intestazione di file.                    |
| [Modifica degli attributi dei metadati](editing-metadata-attributes.md)             | Viene descritto come modificare gli attributi di metadati esistenti.                               |
| [Rimozione degli attributi dei metadati](removing-metadata-attributes.md)           | Viene descritto come rimuovere gli attributi di metadati esistenti.                             |
| [Uso di attributi di metadati complessi](using-complex-metadata-attributes.md) | Viene descritto come utilizzare gli attributi i cui valori sono rappresentati da strutture . |



 

Diverse applicazioni di esempio illustrano come recuperare e modificare i metadati. In particolare, vedere l'esempio MetadataEdit, disponibile sia nelle versioni C++ che in C#.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> <dt>

[**Applicazioni di esempio**](sample-applications.md)
</dt> </dl>

 

 




