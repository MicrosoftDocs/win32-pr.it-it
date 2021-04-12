---
description: Gli sviluppatori di database di installazione devono essere a conoscenza di due limitazioni sulla gestione dei flussi da parte dell'implementazione dell'archiviazione strutturata OLE Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitazioni OLE sui flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226446"
---
# <a name="ole-limitations-on-streams"></a>Limitazioni OLE sui flussi

Gli sviluppatori di database di installazione devono essere a conoscenza di due limitazioni sulla gestione dei flussi da parte dell'implementazione dell'archiviazione strutturata OLE Win32. Queste limitazioni possono influenzare indirettamente le funzioni del programma di installazione tramite trasformazioni e altri dati che possono essere archiviati nel database come flusso.

Esistono due limitazioni rilevanti:

-   I dati binari vengono archiviati con un nome di indice creato concatenando il nome della tabella e i valori delle chiavi primarie del record utilizzando un delimitatore di punto. OLE limita i nomi di flusso a 32 caratteri (31 + terminatore null). Windows Installer usa un algoritmo di compressione che può espandere il limite di 62 caratteri a seconda del carattere. Si noti che i caratteri a byte doppio vengono conteggiati come 2.
-   Sebbene sia possibile avere più flussi aperti contemporaneamente, non è possibile aprire un flusso una seconda volta fino a quando non viene chiuso il primo riferimento. Ciò significa che non è possibile selezionare lo stesso flusso di dati binario da aprire simultaneamente in più record. Il tentativo di leggere i dati binari dal secondo record ha esito negativo. Non è inoltre possibile rinominare le chiavi primarie di un record mentre un flusso di dati binari in tale record è aperto.

 

 



