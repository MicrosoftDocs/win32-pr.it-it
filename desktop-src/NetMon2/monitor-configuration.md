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
# <a name="monitor-configuration-network-monitor"></a><span data-ttu-id="3e959-104">Configurazione del monitoraggio (Network Monitor)</span><span class="sxs-lookup"><span data-stu-id="3e959-104">Monitor Configuration (Network Monitor)</span></span>

<span data-ttu-id="3e959-105">I monitoraggi possono essere configurati tramite l'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="3e959-105">Monitors can be configured using the Network Monitor UI.</span></span> <span data-ttu-id="3e959-106">Gli utenti finali possono passare i criteri di configurazione al monitoraggio usando un modulo HTML archiviato come file HTM nella sottocartella seguente del Network Monitor SDK installato.</span><span class="sxs-lookup"><span data-stu-id="3e959-106">End-users can pass configuration criteria to your monitor using an HTML form stored as an HTM file in the following sub folder of your installed Network Monitor SDK.</span></span>

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

<span data-ttu-id="3e959-107">Quando un utente finale seleziona il pulsante **imposta Monitoraggio configurazione** , il browser genera un messaggio HTML **post** , che include i nomi e i valori per tutti gli elementi del form HTML.</span><span class="sxs-lookup"><span data-stu-id="3e959-107">When an end user selects the **Set Monitor Configuration** button, the browser generates an HTML **POST** message, which includes the names and values for all the HTML form elements.</span></span>

<span data-ttu-id="3e959-108">Quando MCSVC chiama il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) , il parametro *pConfiguration* punta ai dati del messaggio post.</span><span class="sxs-lookup"><span data-stu-id="3e959-108">When the MCSVC calls the [IMonitor::DoConfigure](imonitor-doconfigure.md) method, the *pConfiguration* parameter points to the data from the POST message.</span></span> <span data-ttu-id="3e959-109">Nell'esempio di codice riportato di seguito viene fornito un esempio di dati POST messaggio:</span><span class="sxs-lookup"><span data-stu-id="3e959-109">The following example code provides an example of POST message data:</span></span>

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Questi dati vengono passati come stringa long ASCII. La stringa sembra peculiare, sia per la lunghezza che per l'aspetto di sezioni come% 3A% 5C e% 0D% 0A. Questa peculiarità è causata da HTML, che richiede che un metodo inserisca tutte le possibili stringhe ANSI, DBCS e Unicode in un formato ASCII. Il metodo **DoConfigure** , ad esempio, inserisce alcuni caratteri, ad esempio la e commerciale (&), davanti a ogni nome di variabile per identificarlo come nome di variabile. % 3A% 5C è un formato codificato del carattere due punti e% 0D% 0A indica una coppia ritorno a capo/avanzamento riga. <span data-ttu-id="3e959-115">Nell'esempio di codice riportato di seguito viene fornito il codice HTML risultante come interpretato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="3e959-115">The following example code provides the resulting HTML code as interpreted by the monitor.</span></span>

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



