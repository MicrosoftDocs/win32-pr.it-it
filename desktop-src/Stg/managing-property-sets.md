---
title: Gestione di set di proprietà
description: Un set di proprietà persistenti contiene dati correlati come proprietà.
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- Gestione di set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b6b81c466232d4fd325d53a3cfe67ebb1cbc60c757a6dfe135a021ab7892a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960885"
---
# <a name="managing-property-sets"></a>Gestione di set di proprietà

Un set di proprietà persistenti contiene dati correlati come proprietà. Ogni set di proprietà viene identificato con un FMTID e un identificatore univoco globale (GUID) che consente alle applicazioni, che accedono al set di proprietà, di identificare il set di proprietà. Tramite questa identificazione, l'applicazione interpreta le proprietà contenute nel set.

Ad esempio, le proprietà di formattazione dei caratteri in un elaboratore di testi o gli attributi di rendering di un elemento in un programma di disegno sono set di proprietà.

COM definisce [**l'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per facilitare la gestione dei set di proprietà. Tramite i metodi di questa interfaccia è possibile creare un nuovo set di proprietà oppure aprire o eliminare un set di proprietà esistente. Fornisce inoltre un metodo che crea un enumeratore e fornisce un puntatore alla relativa [**interfaccia IEnumSTATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) È possibile chiamare i metodi di questa interfaccia per enumerare le strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) nell'oggetto, che fornirà informazioni su tutti i set di proprietà nell'oggetto.

Quando si crea o si apre un'istanza di [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)è simile all'apertura di un oggetto che supporta [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), perché è necessario specificare la modalità di archiviazione in cui si apre l'interfaccia. Per **IStorage**, questi includono la modalità transazione, la modalità di lettura/scrittura e la modalità di condivisione.

Quando si crea un set di proprietà con una chiamata a [**IPropertySetStorage::Create,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)specificare se il set di proprietà deve essere semplice o non semplice. Un set di proprietà semplice contiene tipi che possono essere scritti completamente all'interno del flusso del set di proprietà, che ha dimensioni limitate e non può essere superiore a 256 KB in Windows NT 4.0 e versioni precedenti o 1 MB in Windows 2000, Windows XP e Windows Server 2003. Tuttavia, quando è necessario archiviare una maggiore quantità di informazioni nel set di proprietà, è possibile specificare che il set di proprietà sia non semplice. In questo modo è possibile usare uno o più tipi che specificano solo un puntatore a un oggetto di archiviazione o flusso. Questi tipi sono VT \_ STREAM, VT \_ STREAMED OBJECT, VT \_ STORAGE e VT \_ STORED \_ OBJECT.

I dati archiviati in queste proprietà non vengono conteggiati in base al limite di dimensioni del set di proprietà di 256 KB in Windows NT 4.0 o versioni precedenti o al limite di 1 MB in Windows 2000, Windows XP e Windows Server 2003. Tuttavia, i dati sulla proprietà, ad esempio il nome, si applicano. Inoltre, se è necessario un aggiornamento transazionato, il set di proprietà deve essere non semplice. Si verifica ovviamente una certa penalizzazione delle prestazioni per l'apertura di questi tipi, perché richiede l'apertura del flusso o dell'oggetto di archiviazione a cui si ha il puntatore.

Se l'applicazione usa file compositi, è possibile usare l'implementazione fornita da COM di queste interfacce, implementate nell'oggetto di archiviazione di file compositi COM.

Ogni set di proprietà è costituito principalmente da un gruppo di proprietà connesso logicamente, come descritto in [Gestione delle proprietà](managing-properties.md).

Per altre informazioni sui set di proprietà in COM, vedere:

-   [Implementazioni di set di proprietà in COM](property-set-implementations-in-com.md)
-   [Considerazioni sui set di proprietà](property-set-considerations.md)
-   [Considerazioni sull'implementazione di IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Archiviazione di set di proprietà](storing-property-sets.md)
-   [Caratteristiche di prestazioni](performance-characteristics.md)
-   [Implementazione del set di proprietà Summary Information](implementing-the-summary-information-property-set.md)

 

 