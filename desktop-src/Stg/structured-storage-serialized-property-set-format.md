---
title: Structured Archiviazione Serialized Property Set Format
description: I set di proprietà persistenti offrono un'opzione per archiviare i dati file system entità. Per crearli e gestirli, è consigliabile usare le interfacce IPropertySetStorage e IPropertyStorage descritte in Proprietà e set di proprietà.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Structured Archiviazione Strctd Stg , fundamentals, serialized property set format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acbc5300c04b4fe5a9b2a9ce2610eefc8608b3921ef52968a7165c4362ff7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959775"
---
# <a name="structured-storage-serialized-property-set-format"></a>Structured Archiviazione Serialized Property Set Format

I set di proprietà persistenti offrono un'opzione per archiviare i dati file system entità. Per crearli e gestirli, è consigliabile usare le interfacce [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) descritte in [Proprietà e set di proprietà.](properties-and-property-sets.md)

I set di proprietà sono costituiti da una sezione con tag di valori, con la sezione identificata in modo univoco da un identificatore di formato (FMTID). Ogni proprietà è costituita da un identificatore di proprietà e da un indicatore di tipo che rappresenta un valore. Ogni valore archiviato in un set di proprietà ha un identificatore di proprietà univoco che distingue la proprietà. L'indicatore del tipo descrive la rappresentazione dei dati nel valore.

Quando si usano le [**interfacce IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) non è necessario gestire la struttura del formato del set di proprietà serializzato COM. Per altre informazioni, vedere gli argomenti elencati:

Tutti gli elementi dati all'interno di un set di proprietà vengono archiviati nella rappresentazione Intel, ovvero nell'ordine dei byte little endian.

COM definisce un formato dati standard serializzato per i set di proprietà. Quando si gestisce il formato serializzato e non con le interfacce, i set di proprietà hanno le caratteristiche seguenti:

-   I set di proprietà consentono ad applicazioni diverse di creare i propri set di proprietà indipendenti per gestire l'applicazione.
-   I set di proprietà possono essere archiviati in una singola [**istanza di IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o in [**un'istanza di IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) che contiene più flussi. I set di proprietà sono semplicemente un altro tipo di dati che può essere archiviato in molte forme diverse di archiviazione in memoria o su disco. Per altre informazioni e convenzioni consigliate per la creazione del nome di stringa per l'oggetto di archiviazione, vedere Archiviazione [Object Naming Conventions](storage-object-naming-conventions.md).
-   I set di proprietà consentono di includere un dizionario di nomi visualizzati che descrivono il contenuto. È consigliabile un set di convenzioni per la scelta dei nomi delle proprietà. Per altre informazioni su questo dizionario facoltativo, vedere [Identificatori di proprietà riservate,](reserved-property-identifiers.md)incluso [l'ID proprietà 0.](/windows/desktop/Stg/reserved-property-identifiers)

Il flusso del set di proprietà è suddiviso in tre parti principali:

-   Intestazione
-   Coppia FORMATID/offset
-   Sezione contenente i valori effettivi del set di proprietà

La lunghezza complessiva del flusso del set di proprietà deve essere minore o uguale a 256 KB. Le sezioni seguenti, Intestazione [set](property-set-header.md)di proprietà, Identificatore di [formato/Coppia](format-identifier-offset-pair.md)offset e Sezione [(inclusi](section.md) identificatori [di proprietà/coppie di offset),](property-identifiers-offset-pairs.md)con argomenti di supporto, descrivono i singoli componenti che compongono il formato dati del set di proprietà.

> [!Note]  
> Le versioni precedenti di questo documento descrivevano le estensioni al flusso del set di proprietà con più di una sezione consentita, ma che è stata modificata per fornire una sezione nel flusso di proprietà. L'unica eccezione è [documentSummaryInformation e i set di proprietà definiti dall'utente](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 