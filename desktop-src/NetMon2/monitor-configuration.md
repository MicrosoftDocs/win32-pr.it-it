---
description: I monitoraggi possono essere configurati usando l'interfaccia Network Monitor interfaccia utente. Gli utenti finali possono passare i criteri di configurazione al monitoraggio usando un modulo HTML archiviato come file HTM nella seguente sottocartella dell'SDK Network Monitor installato.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Monitorare la configurazione (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b55765774df3be2722c448a1af264162bcd9cdc51ac958cc555bf820d646b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364699"
---
# <a name="monitor-configuration-network-monitor"></a>Monitorare la configurazione (Network Monitor)

I monitoraggi possono essere configurati usando l'interfaccia Network Monitor interfaccia utente. Gli utenti finali possono passare i criteri di configurazione al monitoraggio usando un modulo HTML archiviato come file HTM nella seguente sottocartella dell'SDK Network Monitor installato.

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

Quando un utente finale  seleziona il pulsante Imposta configurazione monitoraggio, il browser genera un messaggio HTML **POST,** che include i nomi e i valori per tutti gli elementi del modulo HTML.

Quando MCSVC chiama il [metodo IMonitor::D oConfigure,](imonitor-doconfigure.md) il *parametro pConfiguration* punta ai dati del messaggio POST. Il codice di esempio seguente fornisce un esempio di dati del messaggio POST:

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Questi dati vengono passati come stringa ASCII lunga. La stringa ha un aspetto particolare, sia per la lunghezza che per l'aspetto delle sezioni, ad esempio %3A%5C e %0D%0A. Questa particolarità è causata dal codice HTML, che richiede che un metodo metto tutte le possibili stringhe ANSI, DBCS e Unicode in un formato ASCII. Ad esempio, il **metodo DoConfigure inserisce** alcuni caratteri, ad esempio la e commerciale (&) davanti a ogni nome di variabile per identificarlo come nome di variabile. %3A%5C è una forma codificata dei due punti e %0D%0A indica una coppia ritorno a capo/avanzamento riga. Il codice di esempio seguente fornisce il codice HTML risultante come interpretato dal monitoraggio.

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



