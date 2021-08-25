---
title: Windows Informazioni di riferimento sui metafile multimediali
description: Windows Informazioni di riferimento sui metafile multimediali
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows metafile multimediali, informazioni di riferimento
- metafile, informazioni di riferimento
- informazioni di riferimento Windows metafile multimediali
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b00cd604ec94c42ef90f08a8875edb4fda92ba8267c7e4a7d7b5505c2fb57932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862261"
---
# <a name="windows-media-metafile-reference"></a>Windows Informazioni di riferimento sui metafile multimediali

Questo riferimento documenta gli elementi e le estensioni di file Windows metafile multimediali. Il riferimento è suddiviso nelle sezioni seguenti.



| Sezione                                                                                    | Descrizione                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Windows Informazioni di riferimento per gli elementi metafile multimediali](windows-media-metafile-elements-reference.md) | Documenta gli elementi metafile, incluse le definizioni, gli attributi e i relativi valori, e le condizioni speciali correlate a ogni elemento. |
| [Estensioni di file](file-name-extensions.md)                                           | Documenta le estensioni di file metafile con regole e linee guida sul loro uso.                                                  |



 

Windows I metafile multimediali sono file di testo che forniscono informazioni su un flusso di file e la relativa presentazione. I metafile sono basati sulla sintassi Extensible Markup Language (XML) e sono formati da vari elementi di tipo XML con tag e attributi. Ogni elemento definisce un'impostazione o un'azione per il flusso multimediale.

Per i metafile sono disponibili due set di tag di elemento. I metafile lato client hanno un set di elementi e i metafile sul lato server hanno un altro set di elementi.

Se un tag di elemento non ha elementi figlio (quelli che modificano o sono contenuti in un altro elemento), è possibile usare un singolo carattere barra (/) alla fine del tag di apertura al posto di un tag di chiusura. Se gli elementi figlio non vengono visualizzati tra il tag di apertura e quello di chiusura di un elemento, non sono elementi figlio per tale elemento e vengono ignorati o causano un errore nella sintassi del metafile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni Windows metafile multimediali**](about-windows-media-metafiles.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Metafile multimediali**](windows-media-metafiles.md)
</dt> </dl>

 

 




