---
description: Tutti i processi (applicazioni o DLL) che chiamano funzioni Winsock devono inizializzare l'uso della DLL di Windows Sockets prima di effettuare altre chiamate di funzioni Winsock. Ciò garantisce anche che Winsock sia supportato nel sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inizializzazione di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aad1dc5bffb09490a963bd86c61c6cc2a857fec45251b38111ab790db8a26e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051519"
---
# <a name="initializing-winsock"></a>Inizializzazione di Winsock

Tutti i processi (applicazioni o DLL) che chiamano funzioni Winsock devono inizializzare l'uso della DLL di Windows Sockets prima di effettuare altre chiamate di funzioni Winsock. Ciò garantisce anche che Winsock sia supportato nel sistema.

**Per inizializzare Winsock**

1.  Creare un [**oggetto WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) denominato wsaData.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Chiamare [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) e restituirne il valore come integer e verificare la presenza di errori.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

La [**funzione WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) viene chiamata per avviare l'uso di WS2 \_32.dll.

La [**struttura WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contiene informazioni sull'implementazione Windows Sockets. Il parametro MAKEWORD(2,2) di [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) effettua una richiesta per la versione 2.2 di Winsock nel sistema e imposta la versione passata come versione più recente del supporto di Windows Sockets che il chiamante può usare.

Passaggio successivo per un client: [Creazione di un socket per il client](creating-a-socket-for-the-client.md)

Passaggio successivo per un server: [Creazione di un socket per il server](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



