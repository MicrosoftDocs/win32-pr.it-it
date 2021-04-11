---
title: Configurazione del provider di servizi Microsoft Locator Name
description: È possibile modificare il provider di servizi dei nomi specificato modificando il file di configurazione Rpcreg. dat, che contiene i parametri NSP e le impostazioni del protocollo RPC. Usare un editor di testo per modificare le voci NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330751"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>Configurazione del provider di servizi Microsoft Locator Name

È possibile modificare il provider di servizi dei nomi specificato modificando il file di configurazione Rpcreg. dat, che contiene i parametri NSP e le impostazioni del protocollo RPC. Usare un editor di testo per modificare le voci NSP.

**Per riconfigurare il provider di servizi Microsoft Locator Name**

1.  Aprire il file RPCREG. dat usando un editor di testo.

    Rpcreg. dat si trova nella directory radice, a meno che non sia stato specificato un percorso diverso durante l'installazione.

2.  Impostare i valori seguenti per le voci del registro di sistema. 

    | Voce del Registro di sistema                                         | Valore                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Software \\ Microsoft \\ RPC \\ NameService \\ Protocol       | Sequenza di protocollo per il protocollo utilizzato. Il valore predefinito è **ncacn \_ NP**.                                                                   |
    | Software \\ Microsoft \\ RPC \\ NameService \\ networkaddress | Nome del computer che esegue il localizzatore usato dai client durante le operazioni di ricerca del nome del servizio. Il valore predefinito è il controller di dominio primario. |
    | Software \\ Microsoft \\ RPC \\ NameService \\ endpoint       | Nome dell'endpoint utilizzato dal servizio del nome. Il valore predefinito \\ è \\ Locator pipe.                                                                    |

    

     

3.  Salvare e chiudere il file.

 

 




