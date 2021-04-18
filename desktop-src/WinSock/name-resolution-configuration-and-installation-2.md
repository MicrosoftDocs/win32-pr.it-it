---
description: Affinché un provider dello spazio dei nomi sia accessibile tramite Windows Sockets, è necessario che sia installato correttamente nel sistema e registrato con Windows Sockets.
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: Configurazione e installazione della risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e0ca7c9c5290a040a17e0f1ded2a97a1aed15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306924"
---
# <a name="name-resolution-configuration-and-installation"></a>Configurazione e installazione della risoluzione dei nomi

Affinché un provider dello spazio dei nomi sia accessibile tramite Windows Sockets, è necessario che sia installato correttamente nel sistema e registrato con Windows Sockets. Quando un provider dello spazio dei nomi viene installato richiamando il programma di installazione di un fornitore, le informazioni di configurazione devono essere aggiunte a un database di configurazione per fornire al WS2 \_32.dll le informazioni necessarie relative al provider di servizi. Il \_32.dll WS2 Esporta [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) per il programma di installazione del fornitore da usare. Questa funzione viene utilizzata per fornire informazioni rilevanti sul provider di servizi da installare. Sono incluse le informazioni seguenti:

-   Nome provider: stringa che rappresenta il provider per la visualizzazione nel pannello di controllo.
-   Versione del provider: la versione del provider.
-   Percorso del provider: nome del percorso della DLL del provider.
-   Namespace: spazio dei nomi supportato dal provider.
-   GUID del provider: numero univoco fornito dal fornitore che rappresenta questa combinazione di provider/spazio dei nomi. Viene utilizzato come chiave per tutti i riferimenti successivi a questo provider e per la disinstallazione. Questi valori vengono creati utilizzando l'utilità Uuidgen.exe.
-   Archivia tutti i flag, ovvero un flag che indica se il provider dello spazio dei nomi sarà responsabile del mantenimento di tutte le informazioni sullo schema della classe di servizio per tutte le classi del servizio. Se esiste un provider di questo tipo, il32.dll WS2 non \_ deve eseguire una query su ogni singolo provider dello spazio dei nomi per queste informazioni.

In Windows Vista e versioni successive viene fornita una funzione [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) avanzata che consente al provider dello spazio dei nomi di passare un BLOB aggiuntivo di dati specifici dello spazio dei nomi.

Sulle piattaforme a 64 bit sono disponibili funzioni [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) e [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) simili per installare uno spazio dei nomi nel catalogo a 32 bit.

Il \_32.dll WS2 fornisce anche una funzione, [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace), per il programma di disinstallazione di un fornitore per rimuovere tutte le informazioni rilevanti dal database di configurazione. Il percorso esatto e il formato di queste informazioni di configurazione sono privati per la \_32.dll WS2 e possono essere modificati solo dalle funzioni sopra indicate.

Sulle piattaforme a 64 bit, viene fornita una funzione [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) simile per disinstallare uno spazio dei nomi nel catalogo a 32 bit.

In qualsiasi momento, un provider dello spazio dei nomi viene considerato attivo o inattivo, con questa impostazione controllata tramite le funzioni [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) . I provider dello spazio dei nomi inattivi continuano a essere visualizzati quando vengono enumerati (usando le funzioni [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa), [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa), [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)e [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) ), ma il \_32.dll WS2 non instraderà le operazioni di registrazione di query o servizi a tali provider. Questa funzionalità può essere utile nelle situazioni in cui più di uno dei provider dello spazio dei nomi installati può supportare un determinato spazio dei nomi.

Quando si fa riferimento a più provider dello spazio dei nomi in una singola funzione API, l'ordine in cui le query e le operazioni di registrazione vengono indirizzate ai provider dello spazio dei nomi non è specificato. L'ordine non è correlato all'ordine in cui sono installati i provider dello spazio dei nomi. Esistono due modi per controllare quali provider dello spazio dei nomi vengono utilizzati per risolvere una query del nome. In primo luogo, le funzioni [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) possono essere utilizzate per abilitare e disabilitare gli spazi dei nomi in modo permanente e a livello di computer. In secondo luogo, le applicazioni possono indirizzare una singola query a un particolare provider specificando il GUID di identificazione del provider nell'ambito della query.

 

 



