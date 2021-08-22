---
title: Applicazione punto di controllo utente generico
description: L'applicazione punto di controllo utente generico consente di individuare i dispositivi, controllarne i dispositivi individuati e visualizzare le relative informazioni sugli eventi, il tutto usando un'interfaccia grafica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0bbf454da2bf36becb3c8b0aff2babc87925df7ac658fc9dc7963ba9182fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655736"
---
# <a name="generic-user-control-point-application"></a>Applicazione punto di controllo utente generico

L'applicazione punto di controllo utente generico consente di individuare i dispositivi, controllarne i dispositivi individuati e visualizzare le relative informazioni sugli eventi, il tutto usando un'interfaccia grafica.

**Per avviare l'applicazione del punto di controllo dell'utilità generica**

1.  Creare e configurare gli esempi \\ netds \\ upnp \\ GenericUCP CPPdevtype.txt file (o il file di \\ \\devtype.txt VisualBasic) con le informazioni sul \\ \\ dispositivo. Questo file consente di configurare il punto di controllo dell'utilità generico per le ricerche "trova per tipo" e "ricerca asincrona". Ogni riga del file deve contenere un tipo di dispositivo e la descrizione correlata. Esempio:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Questo esempio è per un dispositivo lettore multimediale fittizio. Il "Media Player" alla fine della seconda riga non fa parte del tipo di dispositivo, ma è a scopo informativo nell'applicazione punto di controllo dell'utilità generico. Lo stesso vale per "Tutti i dispositivi radice" nella prima riga.

    Aggiungere una riga che contiene il tipo di dispositivo e la descrizione specifici per ogni dispositivo.

2.  Creare e configurare gli esempi \\ netds \\ upnp \\ GenericUCP \\ CPPudn.txt file (o il file diudn.txt VisualBasic) con le informazioni \\ \\ \\ UDN per i dispositivi. Questo file consente di configurare il punto di controllo dell'utilità generico per la ricerca "trova in base alla rete definita dall'utente". Ogni riga usa il formato seguente:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Aggiungere una riga che contiene la rete definita dall'utente specifica per ogni dispositivo.

3.  Eseguire GenericUCP.exe. Verrà visualizzata **la finestra Punto di controllo dell'utilità** generico.

    ![finestra ucp generica](images/generic-ucp.png)

> [!Note]  
> Visualizzazione **della presentazione** e visualizzazione del **servizio** La funzionalità non è implementata nel codice di esempio C++.

 

 

 




