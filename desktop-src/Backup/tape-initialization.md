---
title: Inizializzazione del nastro
description: Un'applicazione deve usare la funzione CreateFile per creare un handle di un dispositivo nastro. Questo handle viene usato nelle operazioni successive sul nastro nel dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Backup inizializzazione nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aeba729feb9351b5af15d26f6366b455c5ce74a9cc6300c9ab8d25047b4760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835404"
---
# <a name="tape-initialization"></a>Inizializzazione del nastro

Un'applicazione deve usare [**la funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per creare un handle di un dispositivo nastro. Questo handle viene usato nelle operazioni successive sul nastro nel dispositivo.

Prima che un'applicazione scrive su un nastro, il nastro deve essere formattato in base alle esigenze dell'applicazione e alle funzionalità dell'unità nastro in uso. La [**funzione CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) riformatta un nastro, creando su di esso un determinato numero di partizioni di una dimensione specificata.

La [**funzione PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara un nastro per l'accesso o la rimozione. Questa funzione può caricare, scaricare, bloccare o sbloccare un nastro. Questa funzione può anche tensionere il nastro spostando il nastro alla fine del nastro e tornando all'inizio.

Per recuperare e impostare informazioni su un nastro e un'unità nastro, un'applicazione usa le [**funzioni GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)e [**GetTapeStatus.**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera informazioni che descrivono un nastro o un'unità nastro. Le informazioni sul nastro includono il tipo, la densità e le dimensioni del blocco del nastro; il numero di partizioni sul nastro; la quantità di nastro rimanente; E così via. Le informazioni sull'unità nastro includono le dimensioni predefinite del blocco dell'unità, il numero massimo di partizioni e le funzionalità supportate.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) imposta le dimensioni del blocco nastro o imposta i flag dell'unità nastro che indicano se l'unità supporta la correzione degli errori hardware, la compressione dei dati, la spaziatura interna dei dati o qualsiasi combinazione dei tre.

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica se l'unità nastro è pronta per elaborare i comandi del nastro.

 

 