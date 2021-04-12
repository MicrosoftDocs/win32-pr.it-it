---
title: Moniker della classe
description: Sebbene le classi siano in genere identificate direttamente con CLSID per funzioni quali CoCreateInstance o CoGetClassObject, le classi possono ora essere identificate anche con un moniker denominato moniker della classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80886ce49ea25d2fb5acbf4dddf550c9d2c3ae29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332196"
---
# <a name="class-monikers"></a>Moniker della classe

Sebbene le classi siano in genere identificate direttamente con CLSID per funzioni quali [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), le classi possono ora essere identificate anche con un moniker denominato *moniker della classe*. I moniker della classe sono associati all'oggetto classe della classe per cui sono stati creati.

La possibilità di identificare le classi con un moniker supporta operazioni utili che non sono altrimenti ingombranti. I moniker di file, ad esempio, supportavano tradizionalmente l'associazione completa solo alla classe associata alla classe del file a cui fa riferimento. un moniker di un file di Excel viene associato a un'istanza di un oggetto di Excel e un moniker a un'immagine GIF viene associato a un'istanza del gestore GIF attualmente registrato. Un moniker della classe consente di indicare la classe che si vuole usare per modificare un file tramite la composizione con un moniker del file. Un moniker della classe per una classe di grafici 3D costituito da un moniker a un file di Excel produce un moniker associato a un'istanza dell'oggetto grafico 3D e Inizializza l'oggetto con il contenuto del file di Excel.

I moniker della classe sono pertanto molto utili in composizione con altri tipi di moniker, ad esempio moniker di file o moniker di elemento.

I moniker della classe possono anche essere composti a destra dei moniker che supportano l'associazione all'interfaccia [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Quando è composto in questo modo, **IClassActivator** fornisce semplicemente l'accesso all'oggetto della classe e alle istanze della classe tramite [**IClassActivator:: GetClassObject**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). I moniker della classe possono essere identificati tramite [**IMoniker:: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), che restituisce MKSYS \_ CLASSMONIKER in *pdwMksys*.

I programmatori in genere creano moniker di classe usando la funzione [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) o [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname). Per informazioni dettagliate, vedere [**IMoniker::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Moniker compositi](composite-monikers.md)
</dt> <dt>

[Moniker di file](file-monikers.md)
</dt> <dt>

[Moniker elemento](item-monikers.md)
</dt> <dt>

[Moniker puntatore](pointer-monikers.md)
</dt> </dl>

 

 




