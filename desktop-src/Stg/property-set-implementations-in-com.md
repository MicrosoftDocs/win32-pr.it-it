---
title: Implementazioni di set di proprietà in COM
description: Implementazioni di set di proprietà in COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Archiviazione strutturata Strctd STG, uso, uso di set di proprietà in COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963185"
---
# <a name="property-set-implementations-in-com"></a>Implementazioni di set di proprietà in COM

Sebbene il potenziale utilizzo di set di proprietà permanenti non sia completamente sfruttato, esistono attualmente due utilizzi principali:

-   Archiviazione di informazioni di riepilogo con un oggetto, ad esempio un documento
-   Trasferimento di dati di proprietà tra oggetti

I set di proprietà COM sono stati progettati per archiviare i dati adatti alla rappresentazione come una raccolta con dimensioni moderate di valori con granularità fine. I set di dati troppo grandi per questa operazione devono essere suddivisi in flussi, archivi e/o set di proprietà distinti. Il formato dei dati del set di proprietà COM non è stato progettato per fornire un sostituto per un database di molti oggetti di piccole dimensioni.

COM fornisce implementazioni delle interfacce dei set di proprietà per vari oggetti, insieme a tre funzioni di supporto. Nella sezione seguente vengono descritte alcune caratteristiche delle prestazioni di queste implementazioni. Per ulteriori informazioni su interfacce specifiche e su come ottenere un puntatore a tali interfacce, fare riferimento alla sezione seguente nella sezione di riferimento COM:

-   [IPropertySetStorage: implementazione del file composto](ipropertysetstorage-compound-file-implementation.md)

    L'implementazione del file composto, che fornisce le interfacce [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , fornisce anche le interfacce [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Data un'implementazione di file composito di **IStorage**, l'interfaccia **IPropertySetStorage** può essere ottenuta chiamando [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [IPropertySetStorage: implementazione del file system NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    Le interfacce [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) possono essere ottenute anche per i file NTFS che non sono file composti. Pertanto, è possibile ottenere queste interfacce per tutti i file in un volume NTFS.

-   [IPropertySetStorage: implementazione autonoma](ipropertysetstorage-stand-alone-implementation.md)

    Quando viene creata un'istanza di questa implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , viene assegnato un puntatore a un oggetto che supporta l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Modifica quindi le archiviazioni del set di proprietà all'interno dell'oggetto di archiviazione. Pertanto, è possibile accedere e modificare i set di proprietà su qualsiasi oggetto supportato da.

-   [Considerazioni sull'implementazione di IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Esistono diversi aspetti da considerare per fornire un'implementazione dell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Per informazioni sulle *considerazioni sull'implementazione* , vedere la sezione riferimenti com.

Sono inoltre disponibili quattro funzioni di supporto, progettate per facilitare la gestione di proprietà che sono state lette da una proprietà impostata in memoria (in una struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ):

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

Le sezioni seguenti illustrano in modo più dettagliato le implementazioni dei set di proprietà in COM:

-   [Gestione dei set di proprietà](managing-property-sets.md)
-   [Considerazioni sui set di proprietà](property-set-considerations.md)
-   [Archiviazione di set di proprietà](storing-property-sets.md)
-   [Caratteristiche di prestazioni](performance-characteristics.md)
-   [Implementazione del set di proprietà informazioni di riepilogo](implementing-the-summary-information-property-set.md)
-   [Considerazioni sull'implementazione di IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 