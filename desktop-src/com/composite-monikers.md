---
title: Moniker compositi
description: Una delle funzionalità più utili dei moniker è che è possibile concatenare o comporre moniker insieme.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad815cdb89dda7f58fe1507d43a07a14d24875309668297e20ec51114dd65d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737027"
---
# <a name="composite-monikers"></a>Moniker compositi

Una delle funzionalità più utili dei moniker è che è possibile concatenare o comporre moniker insieme. Un *moniker composito* è un moniker che è una composizione di altri moniker e può determinare la relazione tra le parti. In questo modo è possibile assemblare il percorso completo di un oggetto in base a due o più moniker equivalenti ai percorsi parziali. È possibile comporre moniker della stessa classe (ad esempio due moniker di file) o di classi diverse (ad esempio un moniker di file e un moniker di elemento). Se si scrive una classe moniker personalizzata, è anche possibile comporre i moniker con moniker di file o elementi. Il vantaggio di base di un composito è che offre un frammento di codice per implementare ogni moniker possibile, che è una combinazione di moniker più semplici. In questo modo si riduce significativamente la necessità di classi di moniker personalizzate specifiche.

Poiché i moniker di classi diverse possono essere composti tra loro, i moniker offrono la possibilità di unire più spazi dei nomi. Il file system definisce uno spazio dei nomi comune per gli oggetti archiviati come file perché tutte le applicazioni comprendono un nome file system percorso. Analogamente, un oggetto contenitore definisce anche uno spazio dei nomi privato per gli oggetti in esso contenuti perché nessun contenitore comprende i nomi generati da un altro contenitore. I moniker consentono di unire questi spazi dei nomi perché è possibile creare moniker di file e moniker di elementi. Un client moniker può cercare tutti gli oggetti nello spazio dei nomi usando un unico meccanismo. Il client chiama [**semplicemente IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sul moniker e il codice del moniker gestisce il resto. Una chiamata a [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) su un oggetto composito crea un nome usando la concatenazione dei nomi visualizzati di tutti i moniker singoli.

Inoltre, poiché è possibile scrivere una classe moniker personalizzata, la composizione del moniker consente di aggiungere estensioni personalizzate allo spazio dei nomi per gli oggetti .

A volte due moniker di classi specifiche possono essere combinati in modo speciale. Ad esempio, un moniker di file che rappresenta un percorso incompleto e un altro moniker di file che rappresenta un percorso relativo possono essere combinati per formare un singolo moniker di file che rappresenta il percorso completo. Ad esempio, i moniker di file "c: work art" possono essere composti con il \\ \\ moniker file relativo ".. \\ backup \\myfile.doc" uguale a "c: \\ work backup \\ \\myfile.doc". Questo è un esempio di *composizione nongenerica*.

*La composizione* generica, d'altra parte, consente la connessione di due moniker qualsiasi, indipendentemente dalle relative classi. Ad esempio, è possibile comporre un moniker di elemento in un moniker di file, anche se non, naturalmente, al contrario.

Poiché una composizione non generale dipende dalla classe dei moniker coinvolti, i relativi dettagli sono definiti dall'implementazione di una particolare classe moniker. È possibile definire nuovi tipi di composizione nongenerica se si scrive una nuova classe moniker. Al contrario, le composizione generiche sono definite da OLE. I moniker creati come risultato della composizione generica sono detti moniker compositi generici.

Queste tre classi, moniker di file, moniker di elementi e moniker compositi generici, lavorano tutte insieme e sono le classi di moniker più comunemente usate.

I client moniker devono chiamare [**IMoniker::ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) per creare un composito nel moniker con un altro. Il moniker su cui viene chiamato internamente decide se può eseguire una composizione generica o non generica. Se l'implementazione del moniker determina che una composizione generica è utilizzabile, OLE fornisce la [**funzione CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) per semplificare questa operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker di classe](class-monikers.md)
</dt> <dt>

[Moniker file](file-monikers.md)
</dt> <dt>

[Moniker degli elementi](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




