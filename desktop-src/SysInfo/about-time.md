---
description: Le funzioni correlate al tempo restituiscono l'ora in uno dei diversi formati. È possibile usare le funzioni di ora per eseguire la conversione tra alcuni formati di ora per semplificare il confronto e la visualizzazione. Nella tabella seguente sono riepilogati i formati di ora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Sarebbe ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cb2cd140ada7033ebe7bf672e654dbf7227385509c676176ee8e936ff590ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765032"
---
# <a name="about-time"></a>Sarebbe ora

Le funzioni correlate al tempo restituiscono l'ora in uno dei diversi formati. È possibile usare le funzioni di ora per eseguire la conversione tra alcuni formati di ora per semplificare il confronto e la visualizzazione. Nella tabella seguente sono riepilogati i formati di ora.



| Formato          | Tipo                                                                     | Descrizione                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Sistema          | [**Systemtime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Anno, mese, giorno, ora, secondo e millisecondo, tratto dall'orologio hardware interno.                                            |
| Locale           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) o [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Ora di sistema o ora del file convertita nel fuso orario locale del sistema.                                                               |
| File            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Numero di intervalli di 100 nanosecondi dal 1° gennaio 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Parola imballata per la data, un'altra per l'ora.                                                                                   |
| Windows         | **DWORD** o **ULONGLONG**                                               | Numero di millisecondi dall'ultimo avvio del sistema. Quando viene recuperato come valore DWORD, Windows cicli di tempo ogni 49,7 giorni. |
| Conteggio interrupt | **Ulonglong**                                                            | Numero di intervalli di 100 nanosecondi dall'ultimo avvio del sistema.                                                           |



 

Per altre informazioni, vedere i seguenti argomenti:

-   [Ora di sistema](system-time.md)
-   [Ora locale](local-time.md)
-   [Orari dei file](file-times.md)
-   [Data e ora di MS-DOS](ms-dos-date-and-time.md)
-   [Ora di Windows](windows-time.md)
-   [Tempo di interrupt](interrupt-time.md)

 

 
