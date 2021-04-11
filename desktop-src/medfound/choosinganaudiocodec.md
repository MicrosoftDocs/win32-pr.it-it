---
description: Scelta di un codec audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Scelta di un codec audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225834"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Scelta di un codec audio (Microsoft Media Foundation)

Il [**codificatore Windows Media Audio**](windowsmediaaudioencoder.md) fornisce tre categorie di codifica audio, come illustrato nella tabella seguente.



| Category                         | Scopo                                                    |
|----------------------------------|------------------------------------------------------------|
| Windows Media Audio standard     | Compressione di utilizzo generico dell'audio.                      |
| Windows Media Audio Professional | Compressione di audio multicanale e ad alta definizione.       |
| Windows Media Audio senza perdita di perdite     | Compressione audio senza perdita di dati originali. |



 

La categoria standard fornisce la codifica audio per utilizzo generico adatta per diversi scenari di riproduzione. Ad esempio, può comprimere l'audio a una velocità in bit ridotta per lo streaming in una rete con larghezza di banda limitata o per il rendering su dispositivi portatili. All'altra estremità della scala, può produrre contenuto audio compresso per la riproduzione di alta qualità. L'enfasi degli algoritmi di codifica standard è la musica, ma sono adatti anche ad altri contenuti audio complessi. La categoria standard deve essere l'impostazione predefinita per il contenuto audio. Le categorie Professional e lossless devono essere usate per soddisfare esigenze specifiche.

Un codificatore separato, [**Windows Media Voice encoder**](windowsmediaaudiovoiceencoder.md), fornisce la compressione del parlato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> </dl>

 

 



