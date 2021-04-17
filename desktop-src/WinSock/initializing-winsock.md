---
description: Tutti i processi (applicazioni o dll) che chiamano funzioni Winsock devono inizializzare l'utilizzo della DLL di Windows Sockets prima di eseguire altre chiamate di funzioni Winsock. In questo modo è anche possibile verificare che Winsock sia supportato nel sistema.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Inizializzazione di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526160"
---
# <a name="initializing-winsock"></a>Inizializzazione di Winsock

Tutti i processi (applicazioni o dll) che chiamano funzioni Winsock devono inizializzare l'utilizzo della DLL di Windows Sockets prima di eseguire altre chiamate di funzioni Winsock. In questo modo è anche possibile verificare che Winsock sia supportato nel sistema.

**Per inizializzare Winsock**

1.  Creare un oggetto [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) denominato WSADATA.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Chiamare [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) e restituire il relativo valore come intero e verificare la presenza di errori.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

La funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) viene chiamata per avviare l'uso di WS2 \_32.dll.

La struttura [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contiene informazioni sull'implementazione di Windows Sockets. Il parametro MAKEWORD (2, 2) di [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) esegue una richiesta per la versione 2,2 di Winsock nel sistema e imposta la versione passata come la versione più recente del supporto di Windows Sockets che il chiamante può utilizzare.

Passaggio successivo per un client: [creazione di un socket per il client](creating-a-socket-for-the-client.md)

Passaggio successivo per un server: [creazione di un socket per il server](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



