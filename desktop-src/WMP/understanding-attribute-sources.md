---
title: Informazioni sulle origini degli attributi
description: Informazioni sulle origini degli attributi
ms.assetid: 83274fea-233d-40dc-b587-99e99ddcd92b
keywords:
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, origini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b7266b75f8f506b1f06e822fbbb40a85d8f2dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713777"
---
# <a name="understanding-attribute-sources"></a>Informazioni sulle origini degli attributi

Gli attributi, o i metadati, che è possibile utilizzare provengono da diverse origini. In questo argomento vengono descritte tali origini, che passano da scenari con un minor numero di attributi potenziali a quelli con attributi più potenziali.

Mentre l'utente riproduce un CD o un DVD, è possibile accedere a metadati molto piccoli sul disco stesso o sul contenuto multimediale del disco. I dischi commerciali, in genere, non includono i metadati dell'attributo.

Se l'utente ha eseguito un CD o un DVD mentre era connesso a Internet, potrebbe essere possibile accedere a più attributi quando tale disco si trova nell'unità CD o DVD. Mentre Windows Media Player è connesso a Internet e riproduce un CD o DVD, il lettore recupera i metadati per tale disco da un database online. Il lettore Visualizza queste informazioni nell' **ora di riproduzione** e in un nodo separato della libreria. Gli attributi non vengono archiviati nel database di libreria, ma vengono memorizzati nella cache. Se la cache non è ancora stata svuotata, l'applicazione avrà accesso agli attributi mentre il disco si trova nell'unità.

> [!Note]  
> Gli utenti possono scegliere di non consentire il recupero di informazioni multimediali da un database online. In tal caso, gli unici attributi disponibili saranno quelli di un file multimediale digitale, quelli che l'utente ha immesso manualmente nella libreria e quelli generati dal lettore stesso, ad esempio gli attributi correlati alla frequenza con cui un elemento è stato riprodotto.

 

Se l'utente riproduce un file multimediale digitale che non viene aggiunto alla libreria, sarà possibile accedere agli attributi inclusi nel file.

Se l'utente riproduce un file multimediale digitale che è stato aggiunto alla libreria, è possibile accedere agli attributi archiviati solo nella libreria, gli attributi archiviati solo nel file e gli attributi archiviati sia nella libreria sia in quello del file.

Gli attributi disponibili per gli elementi multimediali aggiunti alla libreria variano in base alla modalità di creazione del file multimediale digitale di origine e alle azioni eseguite dall'utente dall'aggiunta.

-   Il creatore del contenuto può inserire informazioni sugli attributi nel file quando viene creato per la prima volta. Se, ad esempio, si crea e si distribuisce un file multimediale digitale con l'applicazione, si avrà il controllo sugli attributi inseriti originariamente nel file.
-   Se l'utente modifica i dati degli attributi per un elemento multimediale che è stato aggiunto alla libreria, utilizzando Advanced Tag Editor o l'interfaccia utente della libreria, Windows Media Player aggiunge tali dati al database di libreria. Il giocatore aggiunge alcuni attributi direttamente al file perché sono archiviati solo nel file. In alcuni casi, gli attributi di lettura/scrittura vengono sincronizzati con il file in modo che gli attributi archiviati sia nella libreria che nel file abbiano lo stesso valore.
-   Se l'utente copia un brano da un CD utilizzando Windows Media Player mentre è connesso a Internet, l'effetto è quasi identico a quello che si verifica se l'utente ha modificato gli attributi utilizzando Windows Media Player. Gli attributi vengono aggiunti al database di libreria, estratti dal file stesso e da un database online. Alcuni attributi vengono archiviati solo nel file. A un certo tempo indeterminato, il database di libreria viene sincronizzato con il file.
-   Se si scrive codice usando il controllo Windows Media Player per modificare il valore di un attributo di lettura/scrittura esistente in un elemento multimediale aggiunto alla libreria, l'effetto è quasi identico a quello in cui l'utente ha modificato l'attributo usando Windows Media Player. Il valore viene scritto nel database di libreria e, in un determinato momento, il database viene sincronizzato con il file.
-   [!Note]  
    > Se si incorpora il controllo nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player. Se si usa il controllo in un'applicazione remota scritta in C++, gli attributi di file che vengono modificati verranno scritti nel file multimediale digitale subito dopo aver apportato le modifiche. In entrambi i casi, le modifiche sono immediatamente disponibili tramite la libreria.

     

-   Se si scrive codice usando il controllo Media Player di Windows per inserire un attributo personalizzato in un elemento multimediale, l'attributo e il relativo valore vengono mantenuti solo se l'applicazione contiene un riferimento all'oggetto **multimediale** . L'attributo e il relativo valore non verranno archiviati nel database di libreria o nel file multimediale digitale, se presente.

La situazione più semplice è quando si lavora con i file multimediali digitali forniti. In questo scenario si è certi che gli attributi specifici si trovino nel file. Quando si aggiunge l'elemento multimediale alla raccolta, è possibile utilizzare tali attributi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi elemento multimediale**](media-item-attributes.md)
</dt> </dl>

 

 




