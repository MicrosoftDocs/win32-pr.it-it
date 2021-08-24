---
title: Preallocazione dello spazio su disco per il file di acquisizione
description: Preallocazione dello spazio su disco per il file di acquisizione
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE messaggio
- Macro capFileAlloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a14fa0f3a01a65ad2cb90062fcd4e237eb3e94ef99460d77883bd26df9213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678762"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Preallocazione dello spazio su disco per il file di acquisizione

La preallocazione dello spazio su disco per il file di acquisizione compila un file di una dimensione specificata sul disco prima dell'inizio di un'operazione di acquisizione. La preallocazione di un file di acquisizione riduce l'elaborazione necessaria mentre è in corso l'acquisizione e comporta un minor numero di frame eliminati. È possibile preallocare un file di acquisizione usando il messaggio [**WM \_ CAP FILE \_ \_ ALLOCATE**](wm-cap-file-allocate.md) (o la macro [**capFileAlloc).**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc)

In genere, l'applicazione deve preallocare spazio su disco sufficiente per contenere il file di acquisizione più grande previsto. La preallocazione dello spazio su disco non limita le dimensioni del file acquisito. Le dimensioni del file vengono aumentate automaticamente se i dati acquisiti superano lo spazio allocato. Le successive operazioni di scrittura nel file di acquisizione riutilizzano le parti di spazio su disco allocate per il file, mantenendo le dimensioni e la frammentazione del file.

È anche possibile migliorare le prestazioni di acquisizione deframmentando il file di acquisizione. Per deframmentare il file, usare un'utilità di deframmentazione, ad esempio Utilità di deframmentazione dischi. Se si usa un file di acquisizione deframmentato e in seguito lo si ingrandisce, è necessario deframmentare il file ingrandito. L'espansione di un file di acquisizione deframmentato può frammentare la parte espansa del file e ridurre le prestazioni nell'operazione di acquisizione.

È anche possibile migliorare le prestazioni usando un disco non compresso per l'acquisizione video. La compressione dei dati durante l'acquisizione può limitare la velocità effettiva di acquisizione sul disco.

Un'applicazione può riservare un file di acquisizione permanente per eliminare il tempo necessario per preallocare e deframmentare un file ogni volta che viene avviato. Poiché un file di acquisizione può richiedere una notevole quantità di spazio su disco e la preallocazione di un file di acquisizione rimuove tutti i dati da un file di acquisizione esistente, un'applicazione deve consentire all'utente di decidere se il file è permanente o temporaneo.

 

 




