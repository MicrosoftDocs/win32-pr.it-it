---
description: Perché un provider dello spazio dei nomi sia accessibile tramite Windows Socket, deve essere installato correttamente nel sistema e registrato con Windows Socket.
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: Configurazione e installazione della risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64177b1a41ac45317497d47e7873fda7a02a73d4e0e5b7e0ff2e39c8fc5ee096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111906"
---
# <a name="name-resolution-configuration-and-installation"></a>Configurazione e installazione della risoluzione dei nomi

Perché un provider dello spazio dei nomi sia accessibile tramite Windows Socket, deve essere installato correttamente nel sistema e registrato con Windows Socket. Quando un provider dello spazio dei nomi viene installato richiamando il programma di installazione di un fornitore, le informazioni di configurazione devono essere aggiunte a un database di configurazione per fornire al32.dll Ws2 le informazioni necessarie relative al provider di \_ servizi. Il32.dll Ws2 \_ esporta [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) per l'uso da parte del programma di installazione del fornitore. Questa funzione viene usata per fornire informazioni rilevanti sul provider di servizi da installare. Sono incluse le informazioni seguenti:

-   Nome provider: stringa che rappresenta il provider per la visualizzazione in Pannello di controllo.
-   Versione provider: versione del provider.
-   Percorso provider: nome del percorso della DLL del provider.
-   Spazio dei nomi : spazio dei nomi supportato dal provider.
-   GUID provider: numero univoco fornito dal fornitore che rappresenta questa combinazione di provider/spazio dei nomi. Viene usato come chiave per tutti i riferimenti successivi a questo provider e per la disinstallazione. Questi valori vengono creati usando l'utilità Uuidgen.exe .
-   Archivia tutti i flag, ovvero un flag che indica se il provider dello spazio dei nomi sarà responsabile della conservazione di tutte le informazioni sullo schema della classe del servizio per tutte le classi del servizio. Se esiste un provider di questo tipo, il32.dll Ws2 non deve eseguire una query su ogni singolo provider dello spazio \_ dei nomi per ottenere queste informazioni.

In Windows Vista e versioni successive viene fornita una funzione [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) avanzata che consente al provider dello spazio dei nomi di passare un BLOB aggiuntivo di dati specifico dello spazio dei nomi.

Nelle piattaforme a 64 bit vengono fornite funzioni [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) e [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) simili per installare uno spazio dei nomi nel catalogo a 32 bit.

Il32.dll Ws2 fornisce anche una \_ funzione, [**WSCUnInstallNameSpace,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)per il programma di installazione di un fornitore per rimuovere tutte le informazioni rilevanti dal database di configurazione. La posizione e il formato esatti di queste informazioni di configurazione sono privati per il32.dll Ws2 e possono essere manipolati solo dalle funzioni indicate \_ in precedenza.

Nelle piattaforme a 64 bit viene fornita una funzione [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) simile per disinstallare uno spazio dei nomi nel catalogo a 32 bit.

In qualsiasi momento, un provider dello spazio dei nomi viene considerato attivo o inattivo, con questa impostazione controllata tramite le funzioni [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) e [**WSCEnableNSProvider32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) I provider dello spazio dei nomi inattivi continuano a essere visualizzati quando vengono enumerati (usando le funzioni [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa), [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa), [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)e [**WSCEnumNameSpaceProvidersEx32),**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) ma il32.dll WS2 non instraderà alcuna operazione di query o registrazione del servizio a questi \_ provider. Questa funzionalità può essere utile nelle situazioni in cui più provider di spazi dei nomi installati possono supportare uno spazio dei nomi specificato.

Quando si fa riferimento a più provider di spazi dei nomi in una singola funzione API, l'ordine in cui le query e le operazioni di registrazione vengono indirizzate ai provider dello spazio dei nomi non è specificato. L'ordine non è correlato all'ordine in cui vengono installati i provider dello spazio dei nomi. Esistono due modi per controllare quali provider di spazi dei nomi vengono usati per risolvere una query del nome. In primo luogo, è possibile usare le funzioni [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) per abilitare e disabilitare gli spazi dei nomi in modo permanente a livello di computer. In secondo momento, le applicazioni possono indirizzare una singola query a un provider specifico specificando il GUID di identificazione del provider come parte della query.

 

 



