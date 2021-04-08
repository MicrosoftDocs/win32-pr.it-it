---
title: Creazione e gestione di un punto di connessione del servizio
description: Quando si esegue la pubblicazione con un SCP, tenere presente che deve contenere dati correnti sull'istanza del servizio.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Creazione e gestione di un punto di connessione del servizio AD
- AD, creazione e gestione del punto di connessione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046533"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a>Creazione e gestione di un punto di connessione del servizio

Quando si esegue la pubblicazione con un SCP, tenere presente che deve contenere dati correnti sull'istanza del servizio. In caso contrario, i client che si associano al SCP recuperano i dati obsoleti. Il programma di installazione del servizio, che crea un SCP, specifica i valori iniziali per gli attributi convergenza. Quindi, quando l'istanza del servizio viene avviata, deve individuare SCP e aggiornare i valori di attributo, se necessario. In questo modo, i client sono in grado di garantire i dati più recenti.

Dopo la creazione del SCP, il programma di installazione del servizio esegue due passaggi aggiuntivi che consentono al servizio di aggiornare SCP:

-   Impostare le voci ACE nel descrittore di sicurezza dell'oggetto SCP per consentire al servizio di modificare gli attributi SCP in fase di esecuzione. Per ulteriori informazioni e un esempio di codice, vedere [Abilitazione dell'account del servizio per l'accesso alle proprietà SCP](enabling-service-account-to-access-scp-properties.md).
-   Memorizzare nella cache il **objectGUID** del SCP nel registro di sistema del computer host del servizio. Il servizio recupera il GUID memorizzato nella cache per l'associazione all'SCP per verificare e aggiornare i relativi attributi.

Il programma di installazione del servizio memorizza nella cache il **OBJECTGUID** SCP anziché il DN. Il **objectGUID** non cambia mai, indipendentemente dal fatto che SCP venga spostato o rinominato. Il DN può cambiare se un amministratore sposta o Rinomina SCP. Se, ad esempio, si crea un SCP come figlio di un oggetto computer, il nome distinto del SCP viene modificato se il computer viene rinominato o spostato in un dominio o in un'unità organizzativa diversa.

Quando un programma di installazione del servizio crea un SCP, deve leggere il **objectGUID** dell'oggetto appena creato e memorizzarlo nella cache nel registro di sistema del computer host del servizio. Usare il metodo [**IADs:: Get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) per ottenere il valore **objectGUID** in formato stringa adatto per l'associazione. Memorizzare nella cache la stringa GUID come valore nella seguente chiave del registro di sistema.

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

Dove "nome fornitore" e "nome prodotto" identificano il fornitore e il prodotto.

Quando il servizio viene avviato, recupera la stringa GUID memorizzata nella cache dal registro di sistema e la usa per l'associazione al SCP. Il servizio legge gli attributi SCP importanti e li confronta con i valori correnti. Se i valori SCP sono obsoleti, il servizio li aggiorna. I valori che possono essere richiesti dal servizio per l'aggiornamento includono **Keywords**, **serviceBindingInformation**, **serviceDNSName** e **serviceDNSNameType**.

## <a name="examples"></a>Esempio

-   [Esempi di script](script-samples-for-managing-service-connection-points.md)
-   [Esempi di codice (C/C++)](code-samples-for-managing-service-connection-points.md)

 

 