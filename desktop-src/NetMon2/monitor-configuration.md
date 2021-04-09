---
description: I monitoraggi possono essere configurati tramite l'interfaccia utente di Network Monitor. Gli utenti finali possono passare i criteri di configurazione al monitoraggio usando un modulo HTML archiviato come file HTM nella sottocartella seguente del Network Monitor SDK installato.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Configurazione del monitoraggio (Network Monitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89125450fc71bba21250a66f5c5458317138899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966769"
---
# <a name="monitor-configuration-network-monitor"></a>Configurazione del monitoraggio (Network Monitor)

I monitoraggi possono essere configurati tramite l'interfaccia utente di Network Monitor. Gli utenti finali possono passare i criteri di configurazione al monitoraggio usando un modulo HTML archiviato come file HTM nella sottocartella seguente del Network Monitor SDK installato.

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

Quando un utente finale seleziona il pulsante **imposta Monitoraggio configurazione** , il browser genera un messaggio HTML **post** , che include i nomi e i valori per tutti gli elementi del form HTML.

Quando MCSVC chiama il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) , il parametro *pConfiguration* punta ai dati del messaggio post. Nell'esempio di codice riportato di seguito viene fornito un esempio di dati POST messaggio:

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Questi dati vengono passati come stringa long ASCII. La stringa sembra peculiare, sia per la lunghezza che per l'aspetto di sezioni come% 3A% 5C e% 0D% 0A. Questa peculiarità è causata da HTML, che richiede che un metodo inserisca tutte le possibili stringhe ANSI, DBCS e Unicode in un formato ASCII. Il metodo **DoConfigure** , ad esempio, inserisce alcuni caratteri, ad esempio la e commerciale (&), davanti a ogni nome di variabile per identificarlo come nome di variabile. % 3A% 5C è un formato codificato del carattere due punti e% 0D% 0A indica una coppia ritorno a capo/avanzamento riga. Nell'esempio di codice riportato di seguito viene fornito il codice HTML risultante come interpretato dal monitoraggio.

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



