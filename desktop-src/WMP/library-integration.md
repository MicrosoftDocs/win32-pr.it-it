---
title: Integrazione della libreria
description: Integrazione della libreria
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Windows Media Player Online Stores, integrazione libreria
- negozi online, integrazione di librerie
- digitare 1 negozi online, integrazione con la libreria
- Windows Media Player Online Stores, riquadri attività
- archivi online, riquadri attività
- digitare 1 archivi online, riquadri attività
- Media Player di Windows, riquadri attività
- Windows Media Player Library, integrazione
- libreria, integrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398595"
---
# <a name="library-integration"></a>Integrazione della libreria

L'interfaccia utente di Windows Media Player è organizzata in aree funzionali, denominate *riquadri attività*, che incapsulano le varie funzionalità di alto livello del programma. Sono inclusi i riquadri delle attività **libreria**, **Sincronizza** e **Burn** (tra gli altri). Il riquadro attività **libreria** consente agli utenti di utilizzare la libreria. il riquadro attività **sincronizzazione** consente agli utenti di sincronizzare i file multimediali digitali in un dispositivo portatile; il riquadro attività di **masterizzazione** consente agli utenti di masterizzare i file multimediali digitali in un CD o DVD.

> [!Note]  
> Il riquadro attività **libreria** viene talvolta denominato riquadro attività **Sfoglia** .

 

Ognuno di questi riquadri attività ha un certo livello di integrazione con la libreria. Se, ad esempio, l'utente desidera masterizzare musica su un CD, è opportuno consentire all'utente di scegliere la musica da masterizzare esplorando la libreria e semplicemente trascinando gli elementi multimediali in un elenco. Questo significa che gli utenti possono visualizzare e usare un catalogo di negozi online integrato completamente nella libreria quando si lavora nei riquadri delle attività **libreria**, **Sincronizza** e **Masterizza** . L'enumerazione [WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) contiene valori che rappresentano questi tre riquadri attività, in modo che possano essere identificati a livello di codice.

Ognuno di questi tre riquadri attività è organizzato in tre parti principali. La prima parte è il controllo di visualizzazione ad albero della libreria. Questo controllo consente all'utente di visualizzare gerarchicamente la libreria Media Player di Windows, incluse le funzionalità di categorizzazione per brano, artista, album e così via. La seconda parte del riquadro attività è il riquadro dettagli. Questo riquadro fornisce informazioni dettagliate organizzate in base alla categoria attualmente selezionata nel controllo di visualizzazione albero della libreria. Se, ad esempio, l'utente ha fatto clic su **canzoni** nella visualizzazione albero, nel riquadro dei dettagli vengono visualizzati i titoli delle canzoni attualmente presenti nella libreria, insieme ad altre informazioni, ad esempio la lunghezza e il titolo dell'album. La terza parte è il riquadro elenco o il *carrello*. Gli utenti possono trascinare gli elementi multimediali nel cestino per compilare elenchi, ad esempio playlist, elenchi di sincronizzazione ed elenchi di masterizzazioni.

Quando un catalogo di Store online è integrato con la libreria, l'archivio online viene visualizzato come categoria di primo livello, o *nodo*, nel controllo di visualizzazione albero della libreria. (Un solo catalogo di Store online è visibile all'utente alla volta). Quando un utente sceglie di visualizzare il catalogo dei negozi online facendo clic sul nodo, nel riquadro dei dettagli vengono visualizzate le informazioni relative alla musica nel catalogo del negozio online. Sono incluse le musiche acquistate o affittate dall'utente, nonché la musica non ancora acquisita dall'utente.

Il nodo di archivio online di primo livello include un set di nodi figlio forniti da Windows Media Player. Ad esempio, il nodo di archivio online di primo livello include nodi figlio Radio, artista e album, tra gli altri. Il nodo di archivio online di primo livello può anche avere fino a otto nodi figlio personalizzati forniti dal negozio online. Windows Media Player crea un nodo figlio personalizzato per qualsiasi elenco con un identificatore elenco compreso tra 0 e 7. Nell'archivio online viene specificato l'identificatore di un elenco nel file [list.csv](list-csv.md) che fa parte del catalogo del negozio.

Windows Media Player recupera un'icona per ogni nodo dell'albero personalizzato del negozio online chiamando [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando CPListIDIcon nel parametro *bstrInfoName* .

Quando l'utente si sposta nel catalogo, Windows Media Player effettua chiamate a **IWMPContentPartner:: GetItemInfo** per recuperare i metadati dal plug-in del partner di contenuti sugli elementi musicali selezionati dall'utente. Questi metadati forniscono informazioni al lettore, in modo che il lettore possa visualizzare i dettagli sugli elementi del catalogo. Se, ad esempio, l'utente seleziona un album, Windows Media Player recupera l'URL dell'immagine dell'album in modo che l'utente possa visualizzare l'album di copertina.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




