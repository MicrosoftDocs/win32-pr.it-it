---
title: Informazioni di riferimento sui metafile di Windows Media
description: Informazioni di riferimento sui metafile di Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Metafile di Windows Media, informazioni di riferimento
- Metafile, riferimento
- informazioni di riferimento sui metafile di Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044678"
---
# <a name="windows-media-metafile-reference"></a>Informazioni di riferimento sui metafile di Windows Media

Questa documentazione di riferimento illustra gli elementi e le estensioni di file per i file di Windows Media. Il riferimento è suddiviso nelle sezioni seguenti.



| Sezione                                                                                    | Descrizione                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Riferimento agli elementi metafile di Windows Media](windows-media-metafile-elements-reference.md) | Documenta gli elementi metafile, incluse le definizioni, gli attributi e i relativi valori, nonché le condizioni speciali correlate a ogni elemento. |
| [Estensioni di file](file-name-extensions.md)                                           | Documenta le estensioni dei nomi di file di metafile con regole e linee guida per l'utilizzo.                                                  |



 

I metafile di Windows Media sono file di testo che forniscono informazioni su un flusso di file e la relativa presentazione. I metafile sono basati sulla sintassi Extensible Markup Language (XML) e sono costituiti da vari elementi di tipo XML con i relativi tag e attributi. Ogni elemento definisce un'impostazione o un'azione per i flussi multimediali.

Sono disponibili due set di tag di elemento per i metafile. I metafile lato client hanno un set di elementi e i metafile del lato server hanno un altro set di elementi.

Se un tag di elemento non ha elementi figlio (quelli che modificano o sono contenuti all'interno di un altro elemento), è possibile usare una singola barra (/) alla fine del tag di apertura al posto di un tag di chiusura. Se gli elementi figlio non vengono visualizzati tra il tag di apertura e di chiusura per un elemento, non sono elementi figlio per quell'elemento e vengono ignorati o generano un errore nella sintassi del metafile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui metafile di Windows Media**](about-windows-media-metafiles.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Metafile di Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




