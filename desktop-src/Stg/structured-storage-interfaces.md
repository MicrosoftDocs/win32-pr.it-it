---
title: Interfacce Archiviazione strutturate
description: I Archiviazione strutturati sono organizzati in tre categorie di interfacce.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Interfacce Archiviazione strutturate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345c7b10ae4f73a80b3a263b9a9487c2172382b176404871b363aff336441a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661721"
---
# <a name="structured-storage-interfaces"></a>Interfacce Archiviazione strutturate

I Archiviazione strutturati sono organizzati in tre categorie [di interfacce](interfaces.md). Ogni set rappresenta un livello successivo di riferimento indiretto o astrazione tra un file composto, gli oggetti in esso contenuti e i supporti fisici in cui sono archiviati i singoli componenti.

La prima categoria di interfacce è costituita [**da IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage). Le prime due interfacce definiscono la modalità di archiviazione degli oggetti all'interno di un file composto. Queste interfacce forniscono metodi per l'apertura di elementi di archiviazione, il commit e il ripristino delle modifiche, la copia e lo spostamento di elementi, la lettura e la scrittura di flussi. Queste interfacce non riconoscono i formati di dati nativi dei singoli oggetti e pertanto non dispongono di metodi per salvare tali oggetti in un archivio permanente. **L'interfaccia IRootStorage** ha un singolo metodo per associare un documento composto a un nome file system sottostante. I client devono implementare queste interfacce per i file composti.

La seconda categoria di interfacce è costituita dalle [**interfacce IPersist,**](/windows/win32/api/objidl/nn-objidl-ipersist) che gli oggetti implementano per gestire i dati persistenti. Queste interfacce forniscono metodi per leggere i formati di dati dei singoli oggetti e quindi sapere come archiviarli. Gli oggetti sono responsabili dell'implementazione di queste interfacce perché i client non conoscono i formati di dati nativi dei relativi oggetti annidati. Queste interfacce, tuttavia, non hanno alcuna conoscenza di supporti di archiviazione fisici specifici.

Una terza categoria è costituita da una singola interfaccia, [**ILockBytes,**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)che fornisce metodi per la scrittura di file in supporti fisici specifici, ad esempio un disco rigido o un'unità nastro. Tuttavia, la maggior parte delle applicazioni non implementerà l'interfaccia **ILockBytes** perché COM fornisce già implementazioni per le due situazioni più comuni, ovvero l'implementazione basata su file e l'implementazione basata sulla memoria. L'oggetto di archiviazione file composto chiama **i metodi ILockBytes** che non vengono chiamate direttamente nell'implementazione.

## <a name="compound-file-implementation-limits"></a>Limiti di implementazione di file composti

L'implementazione COM dell'architettura Archiviazione strutturata è denominata *file composti.* Archiviazione oggetti, implementati in file composti, includono un'implementazione delle [**interfacce IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) [**e IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

I puntatori all'implementazione di file composti di queste interfacce vengono acquisiti chiamando la funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) per creare un nuovo oggetto file composto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) per aprire un file composto creato in precedenza.

Un metodo alternativo per acquisire un puntatore all'implementazione di file composta di queste interfacce consiste nel chiamare la funzione [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) precedente e più limitata. Tutte e quattro le funzioni vengono trattate come implementazioni di file composti.

L'implementazione del file composto può essere configurata per l'uso di settori a 512 o 4096 byte, come definito nella [**struttura STGOPTIONS.**](/windows/win32/api/coml2api/ns-coml2api-stgoptions)

L'implementazione di file composti di file composti è soggetta ai vincoli di implementazione seguenti.



| Limite                                           | File composto                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Limiti delle dimensioni dei file:                               | 512: 2 gigabyte (GB) 4096: fino a file system limite<br/>                                                                                                                    |
| Dimensioni massime dell'heap necessarie per gli elementi aperti:   | 512: 4 megabyte (MB) 4096: fino ai limiti di memoria virtuale<br/>                                                                                                                 |
| Si apre la radice simultanea (apre lo stesso file): | Se vengono specificati STGM \_ READ e STGM SHARE DENY WRITE, i limiti \_ sono \_ \_ dettati dai limiti del file system. In caso contrario, è previsto un limite di 20 apre radice simultanee dello stesso file. |
| Numero di elementi in un file:                   | 512: Illimitato, ma le prestazioni possono peggiorare se gli elementi sono numerici nelle migliaia 4096: Illimitato<br/>                                                                         |



 

A causa del limite di dimensioni heap di 4 MB, il numero di elementi aperti in modalità transazione è in genere limitato a diverse migliaia di elementi.

 

