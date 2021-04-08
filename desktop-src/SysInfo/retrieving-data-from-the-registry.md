---
description: Per recuperare dati dal registro di sistema, un'applicazione in genere enumera le sottochiavi di una chiave fino a trovare una particolare e quindi recupera i dati dal valore o dai valori associati.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Recupero di dati dal registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8dd6f6e4d667cf2760c7cba441200755fb6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058178"
---
# <a name="retrieving-data-from-the-registry"></a>Recupero di dati dal registro di sistema

Per recuperare dati dal registro di sistema, un'applicazione in genere enumera le sottochiavi di una chiave fino a trovare una particolare e quindi recupera i dati dal valore o dai valori associati. Un'applicazione può chiamare la funzione [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) per enumerare le sottochiavi di una chiave specificata.

Per recuperare dati dettagliati su una sottochiave specifica, un'applicazione può chiamare la funzione [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) . La funzione [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) recupera una copia del descrittore di sicurezza che protegge una chiave.

Un'applicazione può usare la funzione [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) per enumerare i valori per una determinata chiave e la funzione [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) per recuperare un determinato valore per una chiave. Un'applicazione in genere chiama **RegEnumValue** per determinare i nomi dei valori e quindi **RegQueryValueEx** per recuperare i dati per i nomi.

La funzione [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) Recupera il tipo e i dati per un elenco di nomi di valore associato a una chiave del registro di sistema aperta. Questa funzione è utile per i provider di chiavi dinamiche perché garantisce la coerenza dei dati recuperando più valori in un'operazione atomica.

Poiché altre applicazioni possono modificare i dati in un valore del registro di sistema tra il momento in cui l'applicazione è in grado di leggere un valore e usarla, potrebbe essere necessario assicurarsi che l'applicazione disponga dei dati più recenti. È possibile usare la funzione [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) per notificare al thread chiamante quando sono state apportate modifiche agli attributi o al contenuto di una chiave del registro di sistema oppure se la chiave è stata eliminata. La funzione segnala a un oggetto evento di inviare una notifica al chiamante. Se il thread che chiama **RegNotifyChangeKeyValue** si chiude, l'evento viene segnalato e il monitoraggio della chiave del registro di sistema viene interrotto.

È possibile controllare o specificare le modifiche che devono essere segnalate tramite l'uso di un filtro o di un flag di notifica. In genere, le modifiche vengono segnalate segnalando un evento specificato alla funzione. Si noti che la funzione [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) non funziona con gli handle remoti.

Per monitorare le operazioni del registro di sistema in modo più dettagliato, vedere [**Registro di sistema**](/windows/desktop/ETW/registry).

 

 
