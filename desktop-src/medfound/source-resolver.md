---
description: Resolver di origine
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Resolver di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90ac92cc9d30c5dfb46be60812fbe3156e0f26e396ed1bb9006752ae9db47bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034739"
---
# <a name="source-resolver"></a>Resolver di origine

Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto. Il resolver dell'origine rappresenta il modo standard per la creazione di origini multimediali da parte delle applicazioni.

Internamente, il resolver di origine usa *oggetti gestore:*

-   *I gestori di schemi* accettano un URL e creano un'origine multimediale o un flusso di byte.
-   *I gestori di flussi di byte* accettano un flusso di byte e creano un'origine multimediale.

È possibile implementare un gestore personalizzato e aggiungerlo al registro. I gestori di schemi vengono registrati in base a uno schema URL e i gestori di flussi di byte vengono registrati in base all'estensione del nome file o al tipo MIME.

In questo argomento sono incluse le sezioni seguenti:

-   [Utilizzo del sistema di risoluzione di origine](using-the-source-resolver.md)
-   [Configurazione di un'origine multimediale](configuring-a-media-source.md)
-   [Gestori di schemi e Byte-Stream di schema](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini multimediali](media-sources.md)
</dt> </dl>

 

 



