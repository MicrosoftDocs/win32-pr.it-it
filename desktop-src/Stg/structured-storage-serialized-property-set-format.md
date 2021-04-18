---
title: Formato set di proprietà serializzato di archiviazione strutturata
description: I set di proprietà permanenti forniscono un'opzione per archiviare i dati all'interno di file system entità. Per crearli e gestirli, è consigliabile usare le interfacce IPropertySetStorage e IPropertyStorage descritte in proprietà e set di proprietà.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Archiviazione strutturata Strctd STG, nozioni fondamentali, formato set di proprietà serializzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea03d5ccab337897be801840080e83a6fa86880
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300072"
---
# <a name="structured-storage-serialized-property-set-format"></a>Formato set di proprietà serializzato di archiviazione strutturata

I set di proprietà permanenti forniscono un'opzione per archiviare i dati all'interno di file system entità. Per crearli e gestirli, è consigliabile usare le interfacce [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) descritte in [proprietà e set di proprietà](properties-and-property-sets.md).

I set di proprietà sono composti da una sezione con tag di valori, con la sezione identificata in modo univoco da un identificatore di formato (FMTID). Ogni proprietà è costituita da un identificatore di proprietà e da un indicatore di tipo che rappresenta un valore. Ogni valore archiviato in un set di proprietà ha un identificatore di proprietà univoco che distingue la proprietà. L'indicatore di tipo descrive la rappresentazione dei dati nel valore.

Quando si utilizzano le interfacce [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , non è necessario gestire la struttura del formato del set di proprietà serializzato com. Per ulteriori informazioni, vedere gli argomenti elencati di seguito:

Tutti gli elementi dati all'interno di un set di proprietà vengono archiviati in una rappresentazione Intel, ovvero in ordine di byte little-endian.

COM definisce un formato di dati serializzato standard per i set di proprietà. Quando si gestisce il formato serializzato e non con le interfacce, i set di proprietà hanno le caratteristiche seguenti:

-   I set di proprietà consentono a diverse applicazioni di creare set di proprietà indipendenti per gestire l'applicazione.
-   I set di proprietà possono essere archiviati in una singola istanza di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o in un'istanza di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) contenente più flussi. I set di proprietà sono semplicemente un altro tipo di dati che può essere archiviato in molte forme diverse di un'archiviazione in memoria o su disco. Per altre informazioni e le convenzioni consigliate per la creazione del nome di stringa per l'oggetto di archiviazione, vedere [convenzioni di denominazione degli oggetti di archiviazione](storage-object-naming-conventions.md).
-   I set di proprietà consentono di includere un dizionario di nomi visualizzati che descrivono il contenuto. È consigliabile un set di convenzioni per la scelta dei nomi di proprietà. Per altre informazioni su questo dizionario facoltativo, vedere [identificatori di proprietà riservati](reserved-property-identifiers.md), incluso [ID proprietà 0](/windows/desktop/Stg/reserved-property-identifiers).

Il flusso del set di proprietà è suddiviso in tre parti principali:

-   Intestazione
-   Coppia FORMATID/offset
-   Sezione che contiene i valori effettivi del set di proprietà

La lunghezza complessiva del flusso del set di proprietà deve essere minore o uguale a 256K. Le sezioni seguenti, l' [intestazione del set di proprietà](property-set-header.md), la [coppia identificatore/offset di formato](format-identifier-offset-pair.md)e la [sezione](section.md) (inclusi gli [identificatori di proprietà/coppie di offset](property-identifiers-offset-pairs.md)), con argomenti di supporto, descrivono i singoli componenti che compongono il formato dati del set di proprietà.

> [!Note]  
> Nelle versioni precedenti di questo documento sono descritte le estensioni al flusso del set di proprietà con più di una sezione consentita, ma che è stata riveduta per fornire una sezione nel flusso di proprietà. L'unica eccezione è rappresentata [dai set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 