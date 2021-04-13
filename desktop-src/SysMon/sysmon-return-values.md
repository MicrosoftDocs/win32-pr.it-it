---
title: Valori restituiti SYSMON
description: Di seguito è riportato un elenco dei valori restituiti di monitoraggio di sistema definiti in Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399440"
---
# <a name="sysmon-return-values"></a>Valori restituiti SYSMON

Di seguito è riportato un elenco dei valori restituiti di monitoraggio di sistema definiti in Smonmsg. h.



| Valore restituito                                       | Descrizione                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Percorso contatore DUPL stato smon \_ \_ (0xC0001388)     | La raccolta di contatori contiene già il contatore specificato.                                                                                                                                                                               |
| \_Stato smon \_ nessun \_ \_ oggetto Sysmon (0xC0001389)      | Le impostazioni non contengono alcun oggetto HTML di monitoraggio di sistema completo.                                                                                                                                                                        |
| \_Stato smon \_ insufficiente per \_ alcuni \_ esempi (0xC000138A)       | Il file di log specificato contiene meno di due campioni di dati.                                                                                                                                                                                 |
| \_ \_ Limite dimensioni file di registro stato smon \_ \_ \_ (0xC000138B)  | Il file di log specificato supera i limiti di dimensioni del controllo di monitoraggio di sistema. Se è attualmente selezionato un file di log, selezionare l'attività corrente come origine dati per scaricare il file di log corrente, quindi selezionare nuovamente il file di log specificato. |
| \_ \_ Origine dati file di registro stato smon \_ \_ \_ (0xC000138C) | Per aggiungere un nuovo file di log all'origine dati, è necessario modificare il tipo di origine dati in un tipo diverso da sysmonLogFiles.                                                                                                                          |
| SMON \_ stato \_ DUPL \_ \_ percorso file di registro \_ (0xC000138D)   | La raccolta di file di log contiene già il file di log specificato.                                                                                                                                                                             |



 

Per una descrizione dei valori restituiti aggiuntivi restituiti da monitoraggio di sistema, vedere codici di errore di [sistema](/windows/desktop/Debug/system-error-codes) e codici di [errore dell'helper dati sulle prestazioni](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 