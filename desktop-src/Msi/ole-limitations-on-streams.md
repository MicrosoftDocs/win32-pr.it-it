---
description: Gli sviluppatori di database di installazione devono essere a conoscenza di due limitazioni relative alla gestione dei flussi da parte dell'implementazione dell'archiviazione strutturata OLE Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitazioni OLE in Flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a3a1c606a4446129d9e6592c9b352dd0b3e06ae5c77bb378c2430a32cbc568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754251"
---
# <a name="ole-limitations-on-streams"></a>Limitazioni OLE in Flussi

Gli sviluppatori di database di installazione devono essere a conoscenza di due limitazioni relative alla gestione dei flussi da parte dell'implementazione dell'archiviazione strutturata OLE Win32. Queste limitazioni possono influire indirettamente sulle funzioni del programma di installazione tramite trasformazioni e altri dati che possono essere archiviati nel database come flusso.

Esistono due limitazioni rilevanti:

-   I dati binari vengono archiviati con un nome di indice creato concatenando il nome della tabella e i valori delle chiavi primarie del record usando un delimitatore punto. OLE limita i nomi dei flussi a 32 caratteri (31 + carattere di terminazione Null). Windows Il programma di installazione usa un algoritmo di compressione in grado di espandere il limite a 62 caratteri a seconda del carattere. Si noti che i caratteri a byte doppio vengono conteggiati come 2.
-   Anche se è possibile avere più flussi aperti contemporaneamente, non è possibile aprire un flusso una seconda volta fino a quando il primo riferimento non viene chiuso. Ciò significa che non è possibile selezionare lo stesso flusso di dati binari da aprire contemporaneamente in più record. I tentativi di lettura dei dati binari dal secondo record hanno esito negativo. Non è inoltre possibile rinominare le chiavi primarie di un record mentre è aperto un flusso di dati binari in tale record.

 

 



