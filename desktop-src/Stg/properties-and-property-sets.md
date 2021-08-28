---
title: Proprietà e set di proprietà
description: Anche se i tipi di proprietà di run-time offerti da Automazione e Microsoft ActiveX Controls sono importanti, non ricorrono direttamente alla necessità di archiviare le informazioni con gli oggetti archiviati in modo permanente nel file system.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Struttura Archiviazione Strctd Stg, nozioni fondamentali, proprietà e set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df2ef4b3e4d91cc908d82b58a0ec0156a60de23208cfd8dde2718fa62eaab60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662261"
---
# <a name="properties-and-property-sets"></a>Proprietà e set di proprietà

Anche se i tipi di proprietà di run-time offerti da Automazione e Microsoft ActiveX Controls sono importanti, non ricorrono direttamente alla necessità di archiviare le informazioni con gli oggetti archiviati in modo permanente nel file system. Queste entità possono includere file (strutturati, composti e così via), directory e cataloghi di riepilogo. COM fornisce sia un formato serializzato standard per queste proprietà persistenti sia un set di interfacce e funzioni che consentono di creare e modificare i set di proprietà e le relative proprietà.

Le proprietà persistenti vengono archiviate come set e uno o più set possono essere associati a un'file system entità. Questi set di proprietà persistenti devono essere usati per archiviare dati adatti a essere rappresentati come una raccolta di valori con granularità fine. Non sono destinate a essere usate come data base di grandi dimensioni. Possono essere usati per archiviare informazioni di riepilogo su un oggetto nel sistema, a cui può accedere qualsiasi altro oggetto che comprende come interpretare il set di proprietà.

Le versioni precedenti di COM specificavano molto poco in relazione alle proprietà e al relativo utilizzo, ma definivano un formato serializzato che consentiva agli sviluppatori di archiviare proprietà e set di proprietà in [**un'istanza di IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Sono stati definiti anche gli identificatori di proprietà e la semantica di un singolo set di proprietà, usati per informazioni di riepilogo su un documento. In quel momento era necessario creare e modificare tale struttura direttamente come flusso di dati. Vedere [Structured Archiviazione Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

A questo punto, tuttavia, COM definisce due interfacce principali per gestire i set di proprietà:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Non è più necessario gestire direttamente il formato serializzato quando queste interfacce vengono implementate in un oggetto che supporta [**l'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , ad esempio i file composti. La scrittura di proprietà [**tramite IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crea dati esattamente conformi al formato del set di proprietà COM, come visualizzato tramite **i metodi IStorage.** Il contrario è anche vero: le proprietà scritte nel formato del set di proprietà COM usando **IStorage** sono visibili tramite **IPropertySetStorage** e **IPropertyStorage** (anche se non è possibile prevedere di scrivere in [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e avere le proprietà tramite **IPropertyStorage** immediatamente disponibili o viceversa).

[**L'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) definisce i metodi che creano e gestiscono i set di proprietà. [**L'interfaccia IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) modifica direttamente le proprietà all'interno di un set di proprietà. Chiamando i metodi di queste interfacce, uno sviluppatore di applicazioni può gestire tutti i set di proprietà appropriati per una determinata file system entità. L'uso di queste interfacce offre un'implementazione ottimizzata di lettura e scrittura per le proprietà, anziché disporre di un'implementazione in ogni applicazione, in cui potrebbero verificarsi colli di bottiglia delle prestazioni, ad esempio la ricerca continua. È possibile implementare le interfacce per migliorare le prestazioni, in modo che le proprietà possano essere lette e scritte più rapidamente, ad esempio con una memorizzazione nella cache più efficiente. Inoltre, **IPropertyStorage** e **IPropertySetStorage** consentono di modificare le proprietà nelle entità che non supportano [**IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage)anche se in generale la maggior parte delle applicazioni non lo farà.

Questa sezione contiene i seguenti argomenti:

-   [Set di proprietà Summary Information](the-summary-information-property-set.md)
-   [Identificatori di formato dei set di proprietà predefiniti](predefined-property-set-format-identifiers.md)
-   [Set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazioni di set di proprietà in COM](property-set-implementations-in-com.md)
</dt> <dt>

[Considerazioni sui set di proprietà](property-set-considerations.md)
</dt> <dt>

[Gestione delle proprietà](managing-properties.md)
</dt> <dt>

[Gestione di set di proprietà](managing-property-sets.md)
</dt> <dt>

[Archiviazione di set di proprietà](storing-property-sets.md)
</dt> <dt>

[Caratteristiche di prestazioni](performance-characteristics.md)
</dt> </dl>

 

 




