---
title: Applicazione del punto di controllo utente generico
description: L'applicazione del punto di controllo utente generico consente di individuare i dispositivi, controllare i dispositivi individuati e visualizzare le informazioni relative agli eventi, usando un'interfaccia grafica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551851"
---
# <a name="generic-user-control-point-application"></a>Applicazione del punto di controllo utente generico

L'applicazione del punto di controllo utente generico consente di individuare i dispositivi, controllare i dispositivi individuati e visualizzare le informazioni relative agli eventi, usando un'interfaccia grafica.

**Per avviare l'applicazione del punto di controllo dell'utilità generico**

1.  Creare e configurare gli esempi \\ netds \\ UPnP \\ GenericUCP \\ cpp \\devtype.txt file (o il \\ \\ file VisualBasicdevtype.txt) con le informazioni sul dispositivo. Questo file consente di configurare il punto di controllo dell'utilità generico per le ricerche "trova per tipo" e "ricerca asincrona". Ogni riga del file deve contenere un tipo di dispositivo e la relativa descrizione. Ad esempio:

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Questo esempio è relativo a un dispositivo di riproduzione multimediale fittizio. La "Media Player" alla fine della seconda riga non fa parte del tipo di dispositivo, ma è a scopo informativo nell'applicazione del punto di controllo dell'utilità generica. Lo stesso vale per "tutti i dispositivi radice" nella prima riga.

    Aggiungere una riga che contiene il tipo di dispositivo e la descrizione specifici per ogni dispositivo.

2.  Creare e configurare gli esempi \\ netds \\ UPnP \\ GenericUCP \\ cpp \\udn.txt file (o il \\ \\ file VisualBasicudn.txt) con le informazioni UDN per i dispositivi. Questo file consente di configurare il punto di controllo dell'utilità generico per la ricerca "Find by UDN". Ogni riga usa il formato seguente:

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Aggiungere una riga che contiene il UDN specifico per ogni dispositivo.

3.  Eseguire GenericUCP.exe. Viene visualizzata la finestra punto di controllo dell' **utilità generica** .

    ![finestra punto di controllo dell'utilità generica](images/generic-ucp.png)

> [!Note]  
> Il servizio **View Presentation** and **View View.** la funzionalità non è implementata nel codice di esempio C++.

 

 

 




