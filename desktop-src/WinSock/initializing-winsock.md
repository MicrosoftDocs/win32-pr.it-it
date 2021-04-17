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
# <a name="initializing-winsock"></a><span data-ttu-id="65de1-104">Inizializzazione di Winsock</span><span class="sxs-lookup"><span data-stu-id="65de1-104">Initializing Winsock</span></span>

<span data-ttu-id="65de1-105">Tutti i processi (applicazioni o dll) che chiamano funzioni Winsock devono inizializzare l'utilizzo della DLL di Windows Sockets prima di eseguire altre chiamate di funzioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="65de1-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="65de1-106">In questo modo è anche possibile verificare che Winsock sia supportato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="65de1-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="65de1-107">**Per inizializzare Winsock**</span><span class="sxs-lookup"><span data-stu-id="65de1-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="65de1-108">Creare un oggetto [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) denominato WSADATA.</span><span class="sxs-lookup"><span data-stu-id="65de1-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="65de1-109">Chiamare [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) e restituire il relativo valore come intero e verificare la presenza di errori.</span><span class="sxs-lookup"><span data-stu-id="65de1-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="65de1-110">La funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) viene chiamata per avviare l'uso di WS2 \_32.dll.</span><span class="sxs-lookup"><span data-stu-id="65de1-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="65de1-111">La struttura [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) contiene informazioni sull'implementazione di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="65de1-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="65de1-112">Il parametro MAKEWORD (2, 2) di [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) esegue una richiesta per la versione 2,2 di Winsock nel sistema e imposta la versione passata come la versione più recente del supporto di Windows Sockets che il chiamante può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="65de1-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="65de1-113">Passaggio successivo per un client: [creazione di un socket per il client](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="65de1-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="65de1-114">Passaggio successivo per un server: [creazione di un socket per il server](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="65de1-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="65de1-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65de1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65de1-116">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="65de1-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="65de1-117">Creazione di un'applicazione Winsock di base</span><span class="sxs-lookup"><span data-stu-id="65de1-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



