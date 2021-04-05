---
title: Moniker compositi
description: Una delle funzionalità più utili dei moniker è che è possibile concatenare o comporre i moniker.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5375bb505ff3737fb4e0cdea894790d93c0051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714275"
---
# <a name="composite-monikers"></a>Moniker compositi

Una delle funzionalità più utili dei moniker è che è possibile concatenare o comporre i moniker. Un *moniker composito* è un moniker che è una composizione di altri moniker ed è in grado di determinare la relazione tra le parti. Ciò consente di assemblare il percorso completo di un oggetto in base a due o più moniker equivalenti a percorsi parziali. È possibile comporre moniker della stessa classe (ad esempio due moniker di file) o di classi diverse, ad esempio un moniker di file e un moniker di elemento. Se fosse necessario scrivere una classe moniker personalizzata, è anche possibile comporre i moniker con moniker di file o di elemento. Il vantaggio di base di un composito è il fatto che fornisce una porzione di codice per implementare ogni possibile moniker, ovvero una combinazione di moniker più semplici. Che riduce significativamente la necessità di specifiche classi del moniker personalizzato.

Poiché i moniker di classi diverse possono essere composti tra loro, i moniker consentono di creare un join di più spazi dei nomi. Il file system definisce uno spazio dei nomi comune per gli oggetti archiviati come file perché tutte le applicazioni comprendono un nome di percorso file system. Analogamente, un oggetto contenitore definisce anche uno spazio dei nomi privato per gli oggetti in esso contenuti, poiché nessun contenitore riconosce i nomi generati da un altro contenitore. I moniker consentono di unire questi spazi dei nomi perché è possibile comporre moniker di file e moniker di elemento. Un client moniker può eseguire ricerche nello spazio dei nomi per tutti gli oggetti usando un unico meccanismo. Il client chiama semplicemente [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sul moniker e il codice del moniker gestisce il resto. Una chiamata a [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) in un oggetto composito crea un nome usando la concatenazione di tutti i nomi visualizzati dei singoli moniker.

Poiché è possibile scrivere una classe moniker personalizzata, la composizione del moniker consente inoltre di aggiungere estensioni personalizzate allo spazio dei nomi per gli oggetti.

In alcuni casi è possibile combinare due moniker di classi specifiche in modo particolare. Ad esempio, un moniker di file che rappresenta un percorso incompleto e un altro moniker di file che rappresenta un percorso relativo possono essere combinati per formare un moniker di file singolo che rappresenta il percorso completo. Ad esempio, i moniker del file "c: \\ Work \\ Art" possono essere composti con il moniker del file relativo ". \\ backup \\myfile.doc "è uguale a" c: \\ work \\ backup \\myfile.doc ". Questo è un esempio di *composizione non generica*.

La *composizione generica*, d'altra parte, consente la connessione di due moniker qualsiasi, indipendentemente dalle classi. È possibile, ad esempio, comporre un moniker di elemento in un moniker di file, sebbene non sia ovviamente l'altro.

Poiché una composizione non generica dipende dalla classe dei moniker interessati, i relativi dettagli vengono definiti dall'implementazione di una particolare classe moniker. È possibile definire nuovi tipi di composizioni non generiche se si scrive una nuova classe moniker. Al contrario, le composizioni generiche sono definite da OLE. I moniker creati in seguito alla composizione generica sono denominati moniker compositi generici.

Queste tre classi, moniker di file, moniker di elementi e moniker compositi generici, interagiscono tra loro e sono le classi di moniker utilizzate più di frequente.

I client moniker devono chiamare [**IMoniker:: ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) per creare un oggetto composito su moniker con un altro. Il moniker su cui viene chiamato internamente stabilisce se può eseguire una composizione generica o non generica. Se l'implementazione del moniker determina che una composizione generica è utilizzabile, OLE fornisce la funzione [**CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) per semplificare questa operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker della classe](class-monikers.md)
</dt> <dt>

[Moniker di file](file-monikers.md)
</dt> <dt>

[Moniker elemento](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




