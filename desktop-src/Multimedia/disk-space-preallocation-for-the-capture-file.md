---
title: Preallocazione dello spazio su disco per il file di acquisizione
description: Preallocazione dello spazio su disco per il file di acquisizione
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- Messaggio WM_CAP_FILE_ALLOCATE
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329628"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Preallocazione dello spazio su disco per il file di acquisizione

La preallocazione dello spazio su disco per il file di acquisizione compila un file di dimensioni specificate sul disco prima dell'avvio di un'operazione di acquisizione. La preallocazione di un file di acquisizione riduce l'elaborazione richiesta quando è in corso l'acquisizione e comporta un minor numero di frame eliminati. È possibile preallocare un file di acquisizione usando il messaggio di [**\_ \_ \_ allocazione file di WM Cap**](wm-cap-file-allocate.md) (o la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).

In genere, l'applicazione deve preallocare spazio su disco sufficiente per contenere il file di acquisizione più grande previsto. La preallocazione dello spazio su disco non limita le dimensioni del file acquisito. Le dimensioni del file vengono ingrandite automaticamente se i dati acquisiti superano lo spazio allocato. Le successive operazioni di scrittura nel file di acquisizione riutilizzeranno le parti dello spazio su disco allocate per il file, mantenendo le dimensioni e la frammentazione del file.

È inoltre possibile migliorare le prestazioni di acquisizione deframmentando il file di acquisizione. Per deframmentare il file, utilizzare un'utilità di deframmentazione, ad esempio utilità di deframmentazione dischi. Se si utilizza un file di acquisizione deframmentato e successivamente lo si ingrandisce, è necessario deframmentare il file ingrandito. L'ingrandimento di un file di acquisizione deframmentato può frammentare la parte espansa del file e ridurre le prestazioni nell'operazione di acquisizione.

È anche possibile migliorare le prestazioni usando un disco non compresso per l'acquisizione video. La compressione dei dati durante l'acquisizione può limitare la velocità effettiva di acquisizione sul disco.

Un'applicazione può riservare un file di acquisizione permanente per eliminare il tempo necessario per preallocare e deframmentare un file ogni volta che viene avviato. Poiché un file di acquisizione può richiedere una notevole quantità di spazio su disco e la preallocazione di un file di acquisizione rimuove tutti i dati da un file di acquisizione esistente, un'applicazione deve consentire all'utente di decidere se il file è permanente o temporaneo.

 

 




