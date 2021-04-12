---
description: Resolver di origine
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: Resolver di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344381"
---
# <a name="source-resolver"></a>Resolver di origine

Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto. Il resolver dell'origine rappresenta il modo standard per la creazione di origini multimediali da parte delle applicazioni.

Internamente, il resolver di origine utilizza gli oggetti *gestore* :

-   I *gestori dello schema* accettano un URL e creano un'origine multimediale o un flusso di byte.
-   I *gestori del flusso di byte* accettano un flusso di byte e creano un'origine multimediale.

È possibile implementare un gestore personalizzato e aggiungerlo al registro di sistema. I gestori dello schema sono registrati dallo schema URL e i gestori del flusso di byte sono registrati dall'estensione del nome file o dal tipo MIME.

In questo argomento sono incluse le sezioni seguenti:

-   [Uso del resolver di origine](using-the-source-resolver.md)
-   [Configurazione di un'origine multimediale](configuring-a-media-source.md)
-   [Gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini supporti](media-sources.md)
</dt> </dl>

 

 



