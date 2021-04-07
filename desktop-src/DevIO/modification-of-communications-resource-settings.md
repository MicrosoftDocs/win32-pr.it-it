---
description: Quando la funzione CreateFile apre un handle per una risorsa di comunicazione seriale, il sistema Inizializza e configura la risorsa in base ai valori impostati per l'ultima apertura della risorsa.
ms.assetid: a39881d8-32af-4846-a2d3-508f1945b666
title: Modifica delle impostazioni delle risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8658029470fae9ee2d70ffb1459312c3c4d80ecf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049186"
---
# <a name="modification-of-communications-resource-settings"></a>Modifica delle impostazioni delle risorse di comunicazione

Quando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) apre un handle per una risorsa di comunicazione seriale, il sistema Inizializza e configura la risorsa in base ai valori impostati per l'ultima apertura della risorsa. La conservazione delle impostazioni precedenti consente all'utente di mantenere le impostazioni specificate tramite un comando **mode** quando il dispositivo viene riaperto. I valori ereditati dall'operazione di apertura precedente includono le impostazioni di configurazione del blocco di controllo del dispositivo (struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) ) e i valori di timeout utilizzati nelle operazioni di I/O. Se il dispositivo non è mai stato aperto, viene configurato con le impostazioni predefinite del sistema.

Per determinare la configurazione iniziale di una risorsa di comunicazione seriale, un processo chiama la funzione [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) , che compila una struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) della porta seriale con le impostazioni di configurazione correnti. Per modificare questa configurazione, un processo specifica una struttura **DCB** in una chiamata alla funzione [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) .

I membri della struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) specificano le impostazioni di configurazione, ad esempio la velocità in baud, il numero di bit di dati per byte e il numero di bit di interruzione per byte. Altri membri **DCB** specificano caratteri speciali e abilitano il controllo della parità e il controllo di flusso. Quando un processo deve modificare solo alcune di queste impostazioni di configurazione, deve prima chiamare [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate) per compilare una struttura **DCB** con la configurazione corrente. Il processo può quindi modificare i valori importanti nella struttura **DCB** e riconfigurare il dispositivo chiamando [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) e specificando la struttura **DCB** modificata. Questa procedura garantisce che i membri non modificati della struttura **DCB** contengano valori appropriati. Ad esempio, un errore comune è la configurazione di un dispositivo con una struttura **DCB** in cui il membro **XonChar** della struttura è uguale al membro **XoffChar** .

La funzione [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba) fornisce un altro modo per modificare una struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) . **BuildCommDCB** usa una stringa con lo stesso formato degli argomenti della riga di comando del comando **mode** per specificare la velocità in baud, lo schema di parità, il numero di bit di interruzione e il numero di bit di dati. I membri rimanenti di [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) non vengono modificati da questa funzione, ad eccezione del fatto che i membri appropriati sono impostati per disabilitare XON/XOFF e il controllo del flusso hardware. **BuildCommDCB** modifica solo una struttura **DCB** ; non riconfigura il dispositivo.

Un processo può riconfigurare una risorsa di comunicazione usando la funzione [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) per ottenere informazioni da un driver di dispositivo sulle impostazioni di configurazione supportate. Il processo può utilizzare queste informazioni per evitare di specificare una configurazione non supportata.

La funzione [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) riconfigura la risorsa di comunicazione, ma non influisce sui buffer di input e di output interni del driver specificato. I buffer non vengono scaricati e le operazioni di lettura e scrittura in sospeso non vengono terminate in modo anomalo.

Un processo reinizializza una risorsa di comunicazione usando la funzione [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm) , che esegue le attività seguenti:

-   Termina le operazioni di lettura e scrittura in sospeso, anche se non sono state completate.
-   Elimina i caratteri non letti e libera i buffer di input e di output interni del driver associato alla risorsa specificata.
-   Rialloca l'output interno e i buffer di input.

Non è necessario un processo per chiamare [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm). In caso contrario, il driver della risorsa Inizializza il dispositivo con le impostazioni predefinite la prima volta che si usa l'handle delle risorse di comunicazione.

 

 
