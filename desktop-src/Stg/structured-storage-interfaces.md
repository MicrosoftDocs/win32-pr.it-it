---
title: Interfacce di archiviazione strutturate
description: I servizi di archiviazione strutturati sono organizzati in tre categorie di interfacce.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Interfacce di archiviazione strutturate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0010a0d4dec4908111c8a5bb939f795f0a2b2eb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300073"
---
# <a name="structured-storage-interfaces"></a>Interfacce di archiviazione strutturate

I servizi di archiviazione strutturati sono organizzati in tre categorie di [interfacce](interfaces.md). Ogni set rappresenta un livello di riferimento indiretto o di astrazione successivo tra un file composto, gli oggetti in esso contenuti e il supporto fisico in cui sono archiviati questi singoli componenti.

La prima categoria di interfacce è costituita da [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage). Le prime due interfacce definiscono la modalità di archiviazione degli oggetti all'interno di un file composto. Queste interfacce forniscono metodi per l'apertura di elementi di archiviazione, il commit e il ripristino di modifiche, la copia e lo sviluppo di elementi, la lettura e la scrittura di flussi. Queste interfacce non riconoscono i formati di dati nativi dei singoli oggetti e pertanto non dispongono di metodi per salvare tali oggetti nell'archivio permanente. L'interfaccia **IRootStorage** ha un singolo metodo per associare un documento composto con un nome di file system sottostante. I client devono implementare queste interfacce per i file composti.

La seconda categoria di interfacce è costituita dalle interfacce [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) , che gli oggetti implementano per gestire i dati persistenti. Queste interfacce forniscono metodi per leggere i formati di dati dei singoli oggetti e pertanto sono in grado di archiviarli. Gli oggetti sono responsabili dell'implementazione di queste interfacce perché i client non conoscono i formati di dati nativi degli oggetti annidati. Queste interfacce, tuttavia, non conoscono supporti di archiviazione fisici specifici.

Una terza categoria è costituita da una singola interfaccia, [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), che fornisce metodi per la scrittura di file in supporti fisici specifici, ad esempio un disco rigido o un'unità nastro. Tuttavia, la maggior parte delle applicazioni non implementa l'interfaccia **ILockBytes** poiché com fornisce già implementazioni per le due situazioni più comuni, ovvero l'implementazione basata su file e l'implementazione basata sulla memoria. L'oggetto di archiviazione file composto chiama i metodi **ILockBytes** che non vengono chiamati direttamente nell'implementazione.

## <a name="compound-file-implementation-limits"></a>Limiti di implementazione dei file composti

L'implementazione COM di architettura di archiviazione strutturata è denominata *file composti*. Gli oggetti di archiviazione, come implementato nei file composti, includono un'implementazione delle interfacce [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

I puntatori all'implementazione del file composto di queste interfacce vengono acquisiti chiamando la funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) per creare un nuovo oggetto file composto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) per aprire un file composto creato in precedenza.

Un metodo alternativo per l'acquisizione di un puntatore all'implementazione del file composto di queste interfacce consiste nel chiamare la funzione [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) meno recente e più limitata. Tutte e quattro le funzioni vengono considerate come implementazioni di file composte.

L'implementazione del file composto può essere configurata in modo da usare i settori 512 o 4096 byte, come definito nella struttura [**STGOPTIONS**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) .

L'implementazione del file composto dei file composti è soggetta ai vincoli di implementazione seguenti.



| Limite                                           | File composto                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Limiti per le dimensioni dei file:                               | 512:2 gigabyte (GB) 4096: limiti fino a file system<br/>                                                                                                                    |
| Dimensioni massime heap richieste per gli elementi aperti:   | 512:4 megabyte (MB) 4096: fino a limiti di memoria virtuale<br/>                                                                                                                 |
| Si apre la radice simultanea (si apre lo stesso file): | Se \_ vengono specificati STGM Read e STGM \_ share \_ Deny \_ Write, i limiti sono determinati dai limiti del file System. In caso contrario, è previsto un limite di 20 aperture radice simultanee dello stesso file. |
| Numero di elementi in un file:                   | 512: illimitato, ma le prestazioni possono peggiorare se il numero di elementi nelle migliaia 4096: illimitato<br/>                                                                         |



 

A causa del limite delle dimensioni dell'heap di 4 MB, il numero di elementi aperti in modalità transazionale è in genere limitato a diverse migliaia di elementi.

 

