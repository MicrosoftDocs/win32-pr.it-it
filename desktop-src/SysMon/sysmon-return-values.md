---
title: Valori restituiti SYSMON
description: Di seguito è riportato un elenco dei valori restituiti di Monitoraggio di sistema definiti in Smonmsg.h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce526a64132cef51338a83b387aa8e9bfd58ce0ef0b99a1fb7db0dce4c15ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956447"
---
# <a name="sysmon-return-values"></a>Valori restituiti SYSMON

Di seguito è riportato un elenco dei valori restituiti di Monitoraggio di sistema definiti in Smonmsg.h.



| Valore restituito                                       | Descrizione                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SMON \_ STATUS \_ DUPL COUNTER PATH \_ \_ (0xC0001388)     | L'insieme di contatori contiene già il contatore specificato.                                                                                                                                                                               |
| STATO SMON \_ \_ NESSUN OGGETTO \_ \_ SYSMON (0xC0001389)      | Le impostazioni non contengono oggetti HTML completi di Monitoraggio di sistema.                                                                                                                                                                        |
| SMON \_ STATUS TOO FEW SAMPLES \_ \_ \_ (0XC000138A)       | Il file di log specificato contiene meno di due esempi di dati.                                                                                                                                                                                 |
| LIMITE DIMENSIONI FILE DI LOG DI STATO SMON \_ \_ \_ \_ \_ (0xC000138B)  | Il file di log specificato supera i limiti di dimensione del controllo Monitoraggio di sistema. Se è attualmente selezionato un file di log, selezionare l'attività corrente come origine dati per scaricare il file di log corrente, quindi selezionare nuovamente il file di log specificato. |
| ORIGINE DATI DEL FILE DI LOG DI STATO SMON \_ \_ \_ \_ \_ (0xC000138C) | Per aggiungere un nuovo file di log all'origine dati, il tipo di origine dati deve essere modificato in un tipo diverso da sysmonLogFiles.                                                                                                                          |
| SMON \_ STATUS \_ DUPL LOG FILE PATH \_ \_ \_ (0xC000138D)   | La raccolta di file di log contiene già il file di log specificato.                                                                                                                                                                             |



 

Per una descrizione dei valori restituiti aggiuntivi restituiti da Monitoraggio di sistema, vedere [Codici di](/windows/desktop/Debug/system-error-codes) errore di sistema e Codici di [errore dell'helper dati sulle prestazioni](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 