---
description: La tabella DisplayToID correla la stringa descrittiva visualizzata da monitoraggio di sistema al GUID archiviato nelle altre tabelle.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312171"
---
# <a name="displaytoid"></a>DisplayToID

La tabella **DisplayToID** correla la stringa descrittiva visualizzata da monitoraggio di sistema al GUID archiviato nelle altre tabelle.

La tabella **DisplayToID** definisce i campi seguenti:

-   **GUID:** Identificatore univoco generato per un log. Questo campo è la chiave primaria della tabella.
-   **RunId:** Riservato per uso interno.
-   **DisplayString:** Nome del file di log visualizzato in Monitor di sistema.
-   **LogStartTime:** Ora di inizio del processo di registrazione nel formato aaaa-mm-gg hh: mm: SS: nnn.
-   **LogStopTime:** Ora di arresto del processo di registrazione nel formato aaaa-mm-gg hh: mm: SS: nnn. È possibile differenziare più file di log con lo stesso valore **displayString** usando il valore in questo e i campi **LogStartTime** . I valori nei campi **LogStartTime** e **LogStopTime** consentono inoltre di accedere rapidamente al tempo totale di raccolta.
-   **NumberOfRecords:** Numero di campioni archiviati nella tabella per ogni raccolta di log.
-   **MinutesToUTC:** Valore utilizzato per convertire i dati della riga archiviati nell'ora UTC nell'ora locale.
-   **TimeZoneName:** Nome del fuso orario in cui sono stati raccolti i dati. Se si raccolgono o si riregistrano dati da un file raccolto nei sistemi nel proprio fuso orario, questo campo dimostrerà il percorso.

**Nota**  Prima di Windows Vista, gli insiemi agenti di raccolta dati venivano archiviati nel registro di sistema

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ log queries**

. I campi elencati sopra non corrispondono ai valori nel registro di sistema. Per Windows Vista, gli insiemi agenti di raccolta dati non vengono archiviati nel registro di sistema.

 

 



