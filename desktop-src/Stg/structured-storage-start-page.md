---
title: Archiviazione strutturata
description: L'archiviazione strutturata fornisce la persistenza di file e dati in COM gestendo un singolo file come una raccolta strutturata di oggetti noti come flussi e archivi.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Archiviazione strutturata Strctd STG
- Archivio strutturato Strctd STG, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338238"
---
# <a name="structured-storage"></a>Archiviazione strutturata

## <a name="purpose"></a>Scopo

L'archiviazione strutturata fornisce la persistenza di file e dati in COM gestendo un singolo file come una raccolta strutturata di oggetti noti come flussi e archivi.

Lo scopo dell'archiviazione strutturata consiste nel ridurre le sanzioni e il sovraccarico delle prestazioni associati all'archiviazione di oggetti distinti in un singolo file. L'archiviazione strutturata fornisce una soluzione definendo la modalità di gestione di una singola entità file come raccolta strutturata di due tipi di oggetti archiviazione e flussi tramite un'implementazione standard denominata file composti. Ciò consente all'utente di interagire con e gestire un file composto come se si trattasse di un singolo file piuttosto che di una gerarchia nidificata di oggetti separati.

## <a name="where-applicable"></a>Se applicabile

L'archiviazione strutturata può essere usata nei sistemi operativi Microsoft basati su COM.

## <a name="developer-audience"></a>Sviluppatori

La documentazione di archiviazione strutturata è destinata a programmatori C e C++ esperti e a sviluppatori di sistemi basati su COM.

L'archiviazione strutturata supporta principalmente i linguaggi di programmazione C e C++, tuttavia qualsiasi tecnologia basata su COM supporterà anche qualsiasi linguaggio di programmazione che utilizza i puntatori di interfaccia.

Una conoscenza approfondita delle tecnologie COM è un prerequisito per l'utilizzo dello sviluppo di un archivio strutturato.

## <a name="run-time-requirements"></a>Requisiti di runtime

Per ulteriori informazioni sui sistemi operativi necessari per utilizzare un particolare elemento API, vedere la sezione requisiti della documentazione relativa all'elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Overview](about-structured-storage.md)<br/>                 | Informazioni generali sull'archiviazione strutturata.<br/>                                                                                                                                                                                                                                                 |
| [Uso dell'archiviazione strutturata](using-structured-storage.md)<br/> | Uso delle informazioni per l'archiviazione strutturata.<br/>                                                                                                                                                                                                                                                     |
| [Riferimento](structured-storage-reference.md)<br/>            | Documentazione di interfacce, funzioni, strutture ed enumerazioni specifiche dell'archiviazione strutturata.<br/>                                                                                                                                                                                             |
| [Esempi](samples.md)<br/>                                   | Esempi di codice scritti in C++. Per ulteriori informazioni, vedere [nomi in IStorage](names-in-istorage.md), [intestazione set di proprietà](property-set-header.md), [sezione](section.md), archiviazione di [set di proprietà](storing-property-sets.md)e [utilizzo di archiviazione strutturata](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Component Object Model (COM)](../com/the-component-object-model.md)
</dt> </dl>

 

