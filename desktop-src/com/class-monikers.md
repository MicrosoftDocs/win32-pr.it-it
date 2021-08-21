---
title: Moniker di classe
description: Anche se le classi vengono in genere identificate direttamente con i CLSID in funzioni come CoCreateInstance o CoGetClassObject, le classi possono ora essere identificate anche con un moniker denominato moniker di classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499a117372cd7364fc52b3503b30175a4be11afb9e28e3dd32adbf1007185f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048694"
---
# <a name="class-monikers"></a>Moniker di classe

Anche se le classi vengono in genere identificate direttamente con i CLSID a funzioni come [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)le classi possono ora anche essere identificate con un moniker denominato *moniker di classe*. I moniker di classe vengono associati all'oggetto classe della classe per cui vengono creati.

La possibilità di identificare le classi con un moniker supporta operazioni utili che altrimenti non sono ingombranti. Ad esempio, i moniker di file supportavano in genere l'associazione rich solo alla classe associata alla classe di file a cui fanno riferimento; Un moniker a un file Excel verrebbe associato a un'istanza di un oggetto Excel e un moniker a un'immagine GIF verrebbe associato a un'istanza del gestore GIF attualmente registrato. Un moniker di classe consente di indicare la classe che si vuole usare per modificare un file tramite la composizione con un moniker di file. Un moniker di classe per una classe di grafici 3D composto da un moniker in un file Excel restituisce un moniker associato a un'istanza dell'oggetto grafico 3D e inizializza l'oggetto con il contenuto del file Excel.

I moniker di classe sono quindi più utili nella composizione con altri tipi di moniker, ad esempio moniker di file o moniker di elementi.

I moniker di classe possono anche essere composti a destra dei moniker che supportano l'associazione [**all'interfaccia IClassActivator.**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) Se composto in questo modo, **IClassActivator** concede semplicemente l'accesso all'oggetto classe e alle istanze della classe tramite [**IClassActivator::GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). I moniker di classe possono essere identificati tramite [**IMoniker::IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), che restituisce MKSYS \_ CLASSMONIKER in *pdwMksys*.

I programmatori creano in genere moniker di classe [**usando la funzione CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) o [**tramite MkParseDisplayName.**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) Per informazioni [**dettagliate, vedere IMoniker::P arseDisplayName.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker file](file-monikers.md)
</dt> <dt>

[Moniker degli elementi](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




