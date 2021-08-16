---
description: Per recuperare dati dal Registro di sistema, un'applicazione enumera in genere le sottochiavi di una chiave finché non trova una chiave specifica e quindi recupera i dati dal valore o dai valori associati.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Recupero di dati dal Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bedbe0631015188a8a9fe280ba17d929c83663e995f440f4528c0913fc69cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763480"
---
# <a name="retrieving-data-from-the-registry"></a>Recupero di dati dal Registro di sistema

Per recuperare dati dal Registro di sistema, un'applicazione enumera in genere le sottochiavi di una chiave finché non trova una chiave specifica e quindi recupera i dati dal valore o dai valori associati. Un'applicazione può chiamare [**la funzione RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) per enumerare le sottochiavi di una determinata chiave.

Per recuperare dati dettagliati su una determinata sottochiave, un'applicazione può chiamare la [**funzione RegQueryInfoKey.**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) La [**funzione RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) recupera una copia del descrittore di sicurezza che protegge una chiave.

Un'applicazione può usare la [**funzione RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) per enumerare i valori per una determinata chiave e la funzione [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) per recuperare un determinato valore per una chiave. Un'applicazione chiama **in genere RegEnumValue per** determinare i nomi dei valori e quindi **RegQueryValueEx** per recuperare i dati per i nomi.

La [**funzione RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) recupera il tipo e i dati per un elenco di nomi di valore associati a una chiave del Registro di sistema aperta. Questa funzione è utile per i provider di chiavi dinamici perché garantisce la coerenza dei dati recuperando più valori in un'operazione atomica.

Poiché altre applicazioni possono modificare i dati in un valore del Registro di sistema tra il momento in cui l'applicazione può leggere un valore e usarlo, potrebbe essere necessario assicurarsi che l'applicazione abbia i dati più recenti. È possibile usare la [**funzione RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) per notificare al thread chiamante quando vengono apportate modifiche agli attributi o al contenuto di una chiave del Registro di sistema o se la chiave viene eliminata. La funzione segnala un oggetto evento per notificare al chiamante. Se il thread che chiama **RegNotifyChangeKeyValue** viene chiuso, l'evento viene segnalato e il monitoraggio della chiave del Registro di sistema viene arrestato.

È possibile controllare o specificare quali modifiche devono essere segnalate tramite l'uso di un filtro o di un flag di notifica. In genere, le modifiche vengono segnalate segnalando un evento specificato alla funzione. Si noti che [**la funzione RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) non funziona con gli handle remoti.

Per monitorare le operazioni del Registro di sistema in modo più dettagliato, vedere [**Registro di sistema.**](/windows/desktop/ETW/registry)

 

 
