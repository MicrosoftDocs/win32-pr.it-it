---
title: Proprietà e set di proprietà
description: Sebbene i tipi di proprietà di runtime che automazione e controlli ActiveX Microsoft offrano siano importanti, non risolvono direttamente la necessità di archiviare le informazioni con oggetti archiviati in modo permanente nel file system.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Archiviazione strutturata Strctd STG, nozioni fondamentali, proprietà e set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396967"
---
# <a name="properties-and-property-sets"></a>Proprietà e set di proprietà

Sebbene i tipi di proprietà di runtime che automazione e controlli ActiveX Microsoft offrano siano importanti, non risolvono direttamente la necessità di archiviare le informazioni con oggetti archiviati in modo permanente nel file system. Queste entità possono includere file (strutturati, composti e così via), directory e cataloghi riepilogativi. COM fornisce un formato serializzato standard per queste proprietà permanenti e un set di interfacce e funzioni che consentono di creare e modificare i set di proprietà e le relative proprietà.

Le proprietà permanenti vengono archiviate come set e uno o più set possono essere associati a un'entità file system. Questi set di proprietà permanenti devono essere usati per archiviare i dati adatti per essere rappresentati come una raccolta di valori con granularità fine. Non sono progettate per essere usate come base di dati di grandi dimensioni. Possono essere usati per archiviare informazioni di riepilogo su un oggetto nel sistema, a cui è possibile accedere da qualsiasi altro oggetto che comprenda come interpretare il set di proprietà.

Le versioni precedenti di COM specificavano molto poco rispetto alle proprietà e al loro utilizzo, ma definivano un formato serializzato che consentiva agli sviluppatori di archiviare proprietà e set di proprietà in un'istanza di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Sono stati definiti anche gli identificatori di proprietà e la semantica di un singolo set di proprietà, usati per ottenere informazioni di riepilogo su un documento. In quel momento, era necessario creare e modificare la struttura direttamente come flusso di dati. Vedere [formato di set di proprietà serializzato di archiviazione strutturato](structured-storage-serialized-property-set-format.md).

Ora, tuttavia, COM definisce due interfacce primarie per gestire i set di proprietà:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Non è più necessario gestire direttamente il formato serializzato quando queste interfacce sono implementate in un oggetto che supporta l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , ad esempio i file composti. La scrittura di proprietà tramite [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crea dati che sono esattamente conformi al formato del set di proprietà com, come visualizzato con i metodi **IStorage** . È anche vero il contrario: le proprietà scritte nel formato del set di proprietà COM usando **IStorage** sono visibili tramite **IPropertySetStorage** e **IPropertyStorage** (anche se non è possibile prevedere la scrittura in [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e le proprietà tramite **IPropertyStorage** immediatamente disponibile o viceversa).

L'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) definisce i metodi per la creazione e la gestione di set di proprietà. L'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) modifica direttamente le proprietà all'interno di un set di proprietà. Chiamando i metodi di queste interfacce, uno sviluppatore di applicazioni può gestire tutti i set di proprietà appropriati per una determinata entità file system. L'uso di queste interfacce fornisce un'implementazione ottimizzata per la lettura e la scrittura delle proprietà, anziché avere un'implementazione in ogni applicazione, in cui potrebbero verificarsi colli di bottiglia delle prestazioni, ad esempio la ricerca incessa. È possibile implementare le interfacce per migliorare le prestazioni, in modo che le proprietà possano essere lette e scritte più rapidamente da, ad esempio, un caching più efficiente. Inoltre, **IPropertyStorage** e **IPropertySetStorage** consentono di modificare le proprietà delle entità che non supportano [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), anche se in generale la maggior parte delle applicazioni non lo farà.

Questa sezione contiene i seguenti argomenti:

-   [Set di proprietà delle informazioni di riepilogo](the-summary-information-property-set.md)
-   [Identificatori di formato di set di proprietà predefiniti](predefined-property-set-format-identifiers.md)
-   [Set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazioni di set di proprietà in COM](property-set-implementations-in-com.md)
</dt> <dt>

[Considerazioni sui set di proprietà](property-set-considerations.md)
</dt> <dt>

[Gestione delle proprietà](managing-properties.md)
</dt> <dt>

[Gestione dei set di proprietà](managing-property-sets.md)
</dt> <dt>

[Archiviazione di set di proprietà](storing-property-sets.md)
</dt> <dt>

[Caratteristiche di prestazioni](performance-characteristics.md)
</dt> </dl>

 

 




