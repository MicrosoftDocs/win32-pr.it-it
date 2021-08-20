---
title: Implementazioni di set di proprietà in COM
description: Implementazioni di set di proprietà in COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Struttura Archiviazione Strctd Stg , using, set di proprietà usa in COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d582699d398a69a0f24bee18ede362569f529de098fe49310fb93254314b1feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960730"
---
# <a name="property-set-implementations-in-com"></a>Implementazioni di set di proprietà in COM

Sebbene il potenziale utilizzo di set di proprietà persistenti non sia completamente toccato, esistono attualmente due usi principali:

-   Archiviazione di informazioni di riepilogo con un oggetto, ad esempio un documento
-   Trasferimento dei dati delle proprietà tra oggetti

I set di proprietà COM sono stati progettati per archiviare dati adatti alla rappresentazione come una raccolta di valori con granularità fine di dimensioni moderate. I set di dati troppo grandi per essere fattibili devono essere suddivisi in flussi, archivi e/o set di proprietà separati. Il formato dei dati del set di proprietà COM non era destinato a fornire un sostituto per un database di molti oggetti di piccole dimensioni.

COM fornisce implementazioni delle interfacce del set di proprietà per vari oggetti, insieme a tre funzioni helper. La sezione seguente descrive alcune caratteristiche delle prestazioni di queste implementazioni. Per altre informazioni su interfacce specifiche e su come ottenere un puntatore a queste interfacce, vedere quanto segue nella sezione di riferimento COM:

-   [Implementazione di IPropertySetStorage-Compound File](ipropertysetstorage-compound-file-implementation.md)

    L'implementazione del file composto, che fornisce [**le interfacce IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream,**](/windows/desktop/api/Objidl/nn-objidl-istream) fornisce anche [**le interfacce IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Data l'implementazione di un file composto **di IStorage,** **l'interfaccia IPropertySetStorage** può essere ottenuta chiamando [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [Implementazione del file system IPropertySetStorage-NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    Le [**interfacce IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) possono essere ottenute anche per i file NTFS che non sono file composti. Pertanto, è possibile ottenere queste interfacce per tutti i file in un volume NTFS.

-   [Implementazione autonoma di IPropertySetStorage-Stand-alone](ipropertysetstorage-stand-alone-implementation.md)

    Quando viene creata un'istanza di questa implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) viene assegnato un puntatore a un oggetto che supporta l'interfaccia [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Modifica quindi le risorse di archiviazione dei set di proprietà all'interno di tale oggetto di archiviazione. Di conseguenza, è possibile accedere e modificare i set di proprietà in qualsiasi oggetto che supporta .

-   [Considerazioni sull'implementazione di IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Esistono diversi problemi da considerare nel fornire un'implementazione [**dell'interfaccia IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Fare riferimento a queste *considerazioni sull'implementazione* nella sezione Com Reference (Considerazioni sull'implementazione) nella sezione Com Reference (Informazioni di riferimento su COM).

Sono inoltre disponibili quattro funzioni helper, progettate per facilitare la gestione delle proprietà lette da un set di proprietà in memoria (in una [**struttura PROPVARIANT):**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

Le sezioni seguenti illustrano in modo più dettagliato le implementazioni dei set di proprietà in COM:

-   [Gestione di set di proprietà](managing-property-sets.md)
-   [Considerazioni sui set di proprietà](property-set-considerations.md)
-   [Archiviazione di set di proprietà](storing-property-sets.md)
-   [Caratteristiche di prestazioni](performance-characteristics.md)
-   [Implementazione del set di proprietà Summary Information](implementing-the-summary-information-property-set.md)
-   [Considerazioni sull'implementazione di IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 