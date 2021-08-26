---
description: La tabella DisplayToID mette in relazione la stringa descrittiva visualizzata da Monitoraggio di sistema con il GUID archiviato nelle altre tabelle.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485eab24a2c758b36e190e035a9442a032ebd683f3f5ea052bd37992ad14c85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033911"
---
# <a name="displaytoid"></a>DisplayToID

La **tabella DisplayToID** mette in relazione la stringa descrittiva visualizzata da Monitoraggio di sistema con il GUID archiviato nelle altre tabelle.

La **tabella DisplayToID** definisce i campi seguenti:

-   **GUID:** Identificatore univoco generato per un log. Questo campo è la chiave primaria di questa tabella.
-   **RunID:** Riservato per uso interno.
-   **DisplayString:** Nome del file di log visualizzato in Monitoraggio di sistema.
-   **LogStartTime:** Ora di inizio del processo di registrazione nel formato aaaa-mm-gg hh:mm:ss:nnn.
-   **LogStopTime:** Ora di arresto del processo di registrazione nel formato aaaa-mm-gg hh:mm:ss:nnn. È possibile differenziare più file di log con lo stesso valore **DisplayString** usando il valore in questo campo e nei **campi LogStartTime.** I valori nei campi **LogStartTime** e **LogStopTime** consentono anche di accedere rapidamente al tempo totale di raccolta.
-   **NumberOfRecords:** Numero di esempi archiviati nella tabella per ogni raccolta di log.
-   **MinutesToUTC:** Valore utilizzato per convertire i dati di riga archiviati nell'ora UTC nell'ora locale.
-   **TimeZoneName:** Nome del fuso orario in cui sono stati raccolti i dati. Se si raccolgono o si dispone di dati di un file raccolto nei sistemi nel proprio fuso orario, questo campo indica la posizione.

**Nota**  Prima di Windows Vista, gli insiemi agenti di raccolta dati venivano archiviati nel Registro di sistema in

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services \\ SysmonLog \\ Log Queries**

. I campi elencati in precedenza non corrispondono ai valori nel Registro di sistema. Per Windows Vista, gli insiemi agenti di raccolta dati non vengono archiviati nel Registro di sistema.

 

 



