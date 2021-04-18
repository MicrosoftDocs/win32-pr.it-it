---
title: Informazioni sulla libreria
description: Informazioni sulla libreria
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Library, informazioni
- libreria, informazioni
- metadati, Windows Media Player Library
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297753"
---
# <a name="about-the-library"></a>Informazioni sulla libreria

La libreria è un database di informazioni o *metadati* sul contenuto multimediale digitale disponibile per Windows Media Player. Alcune delle informazioni vengono visualizzate nel riquadro **libreria** del lettore; la maggior quantità è disponibile tramite codice.

(In Windows Media Player 9 serie e versioni precedenti questa funzionalità è denominata **libreria multimediale**).

La libreria offre agli utenti un modo semplice per organizzare e accedere al contenuto multimediale digitale. Ad esempio, gli utenti possono visualizzare musica organizzata in base all'album, dall'artista, dal genere o semplicemente come un elenco di tutti i brani musicali. È possibile utilizzare il modello a oggetti di Windows Media Player SDK per accedere alla libreria per riprodurre contenuto, recuperare playlist, aggiungere contenuto, rimuovere contenuto e modificare i metadati associati. Windows Media Player protegge la privacy degli utenti limitando la possibilità di accedere alla libreria dal codice in determinate condizioni. Per ulteriori informazioni sui diritti di accesso, vedere [Library Access](library-access.md).

La libreria archivia i metadati su due tipi di base di contenuto multimediale digitale. Il primo tipo, elementi multimediali digitali, è un singolo file di contenuto, ad esempio un brano musicale o una foto. Il secondo tipo, playlist, è costituito da file che rappresentano un gruppo di elementi multimediali digitali, in genere destinati a essere riprodotti in un ordine specificato. I metadati associati al contenuto multimediale digitale vengono archiviati come coppie nome-valore. I metadati che descrivono la persona che ha eseguito un brano, ad esempio, sono denominati "Artist" e il valore associato è in genere una stringa di testo contenente il nome dell'esecutore. Ogni nome di metadati univoco è denominato *attributo*. Per un elenco degli attributi supportati, vedere il [riferimento all'attributo](attribute-reference.md). Per informazioni sull'uso degli attributi nel codice, vedere [attributi degli elementi multimediali](media-item-attributes.md).

Nelle sezioni seguenti vengono fornite ulteriori informazioni sull'utilizzo della libreria:

-   [Accesso alla libreria a livello di codice](accessing-the-library-programmatically.md)
-   [Informazioni sui servizi di libreria](about-library-services.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




