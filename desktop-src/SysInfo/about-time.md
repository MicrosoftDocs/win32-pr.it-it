---
description: Le funzioni correlate al tempo restituiscono il tempo in uno dei diversi formati. È possibile usare le funzioni temporali per eseguire la conversione tra alcuni formati di tempo per semplificare il confronto e la visualizzazione. Nella tabella seguente vengono riepilogati i formati di ora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Informazioni sul tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050134"
---
# <a name="about-time"></a>Informazioni sul tempo

Le funzioni correlate al tempo restituiscono il tempo in uno dei diversi formati. È possibile usare le funzioni temporali per eseguire la conversione tra alcuni formati di tempo per semplificare il confronto e la visualizzazione. Nella tabella seguente vengono riepilogati i formati di ora.



| Formato          | Tipo                                                                     | Descrizione                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Sistema          | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Anno, mese, giorno, ora, secondo e millisecondo, tratto dal clock hardware interno.                                            |
| Locale           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) o [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Ora di sistema o di file convertito nel fuso orario locale del sistema.                                                               |
| File            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Una parola compressa per la data, un'altra per l'ora.                                                                                   |
| Windows         | **DWORD** o **ULONGLONG**                                               | Numero di millisecondi trascorsi dall'ultimo avvio del sistema. Quando viene recuperato come valore DWORD, l'ora di Windows viene ciclica ogni 49,7 giorni. |
| Numero di interrupt | **ULONGLONG**                                                            | Numero di intervalli di 100-nanosecondi dall'ultimo avvio del sistema.                                                           |



 

Per altre informazioni, vedere i seguenti argomenti:

-   [Ora di sistema](system-time.md)
-   [Ora locale](local-time.md)
-   [Orari file](file-times.md)
-   [Data e ora di MS-DOS](ms-dos-date-and-time.md)
-   [Ora di Windows](windows-time.md)
-   [Tempo di interrupt](interrupt-time.md)

 

 
