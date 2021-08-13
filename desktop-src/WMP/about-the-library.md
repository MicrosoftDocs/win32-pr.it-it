---
title: Informazioni sulla libreria
description: Informazioni sulla libreria
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player,library
- Windows Media Player a oggetti, libreria
- modello a oggetti, libreria
- Windows Media Player ActiveX, libreria per il modello a oggetti
- ActiveX, libreria per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player libreria, informazioni su
- library,about
- metadati,Windows Media Player libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63fdaa19fc8be11de1886074a21b0cc1fb6d4be7dde73faa05c67e1f496ac17c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470351"
---
# <a name="about-the-library"></a>Informazioni sulla libreria

La libreria è un database di informazioni, o *metadati,* sul contenuto multimediale digitale disponibile per Windows Media Player. Alcune delle informazioni vengono visualizzate nel **riquadro Libreria** nel lettore. la maggior parte è disponibile tramite codice.

In Windows Media Player serie 9 e versioni precedenti, questa funzionalità è denominata **Catalogo multimediale.**

La libreria offre agli utenti un modo semplice per organizzare e accedere al contenuto multimediale digitale. Ad esempio, gli utenti possono visualizzare la musica organizzata per album, per artista, per genere o semplicemente come elenco di tutta la musica. È possibile usare il modello Windows Media Player a oggetti di SDK per accedere alla libreria per riprodurre contenuto, recuperare playlist, aggiungere contenuto, rimuovere contenuto e modificare i metadati associati. Windows Media Player la privacy degli utenti limitando la possibilità di accedere alla libreria dal codice in determinate condizioni. Per altre informazioni sui diritti di accesso, vedere [Accesso alla libreria](library-access.md).

La libreria archivia i metadati relativi a due tipi di base di contenuto multimediale digitale. Il primo tipo, gli elementi multimediali digitali, sono singoli file di contenuto, ad esempio una traccia musicale o una foto. Il secondo tipo, playlist, è un file che rappresenta un gruppo di elementi multimediali digitali, in genere destinati a essere riprodotti in un ordine specificato. I metadati associati al contenuto multimediale digitale vengono archiviati come coppie nome-valore. Ad esempio, i metadati che descrivono la persona che ha eseguito un brano sono denominati "Artista" e il valore associato è in genere una stringa di testo contenente il nome dell'esecutore. Ogni nome di metadati univoco è denominato *attributo*. Per un elenco degli attributi supportati, vedere Riferimento [agli attributi](attribute-reference.md). Per informazioni sull'uso degli attributi nel codice, vedere [Attributi degli elementi multimediali](media-item-attributes.md).

Le sezioni seguenti forniscono altre informazioni sull'uso della libreria:

-   [Accesso alla libreria a livello di codice](accessing-the-library-programmatically.md)
-   [Informazioni sui servizi di libreria](about-library-services.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




