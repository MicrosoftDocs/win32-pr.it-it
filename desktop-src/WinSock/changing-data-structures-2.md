---
description: Quando si aggiunge il supporto per IPv6, è necessario assicurarsi che l'applicazione definisca le strutture dei dati dimensionate correttamente.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Modifica delle strutture di dati per applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307022"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="59e38-103">Modifica delle strutture di dati per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="59e38-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="59e38-104">Quando si aggiunge il supporto per IPv6, è necessario assicurarsi che l'applicazione definisca le strutture dei dati dimensionate correttamente.</span><span class="sxs-lookup"><span data-stu-id="59e38-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="59e38-105">La dimensione di un indirizzo IPv6 è molto più grande di un indirizzo IPv4.</span><span class="sxs-lookup"><span data-stu-id="59e38-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="59e38-106">Le strutture hardcoded per gestire le dimensioni di un indirizzo IPv4 durante l'archiviazione di un indirizzo IP provocheranno problemi nell'applicazione e dovranno essere modificate.</span><span class="sxs-lookup"><span data-stu-id="59e38-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="59e38-107">Procedura consigliata</span><span class="sxs-lookup"><span data-stu-id="59e38-107">Best Practice</span></span>

<span data-ttu-id="59e38-108">L'approccio migliore per garantire che le strutture siano dimensionate correttamente consiste nell'usare la struttura di [**\_ archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="59e38-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="59e38-109">La struttura di **\_ archiviazione sockaddr** è indipendente dalla versione dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="59e38-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="59e38-110">Quando si usa la struttura di **\_ archiviazione sockaddr** per archiviare indirizzi IP, gli indirizzi IPv4 e IPv6 possono essere gestiti correttamente con una codebase.</span><span class="sxs-lookup"><span data-stu-id="59e38-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="59e38-111">Nell'esempio seguente, che è un estratto dal file server. c disponibile nell'Appendice B, identifica l'uso appropriato della struttura di **\_ archiviazione sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="59e38-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="59e38-112">Si noti che la struttura, se utilizzata correttamente come illustrato in questo esempio, gestisce normalmente un indirizzo IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="59e38-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> <span data-ttu-id="59e38-113">La struttura di [**\_ archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) è una novità di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59e38-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="59e38-114">Codice da evitare</span><span class="sxs-lookup"><span data-stu-id="59e38-114">Code To Avoid</span></span>

<span data-ttu-id="59e38-115">In genere, molte applicazioni utilizzano la struttura [**sockaddr**](sockaddr-2.md) per archiviare indirizzi indipendenti dal protocollo o **sockaddr \_ nella** struttura per gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="59e38-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="59e38-116">Né la struttura SOCKADDR né **sockaddr \_ nella** struttura sono sufficientemente grandi da contenere gli indirizzi IPv6 e pertanto entrambi sono insufficienti se l'applicazione deve essere compatibile con IPv6.</span><span class="sxs-lookup"><span data-stu-id="59e38-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="59e38-117">Attività di codifica</span><span class="sxs-lookup"><span data-stu-id="59e38-117">Coding Task</span></span>

<span data-ttu-id="59e38-118">**Per modificare la codebase esistente da IPv4 a IPv4 e IPv6-interoperabilità**</span><span class="sxs-lookup"><span data-stu-id="59e38-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="59e38-119">Acquisire l'utilità Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="59e38-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="59e38-120">L'utilità è inclusa nel Software Development Kit (SDK) di Microsoft Windows, che viene reso disponibile tramite l'abbonamento MSDN o dal Web come download.</span><span class="sxs-lookup"><span data-stu-id="59e38-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="59e38-121">Eseguire l'utilità Checkv4.exe sul codice.</span><span class="sxs-lookup"><span data-stu-id="59e38-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="59e38-122">Per informazioni su come eseguire l'utilità di Checkv4.exe sui file, vedere la sezione relativa all' [uso dell'utilità di Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="59e38-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="59e38-123">Tramite l'utilità viene visualizzato un avviso per l'utilizzo di **sockaddr** o **sockaddr \_ in** strutture e vengono fornite indicazioni su come sostituire con la struttura compatibile con IPv6 [**sockaddr \_ archiviazione**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59e38-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="59e38-124">Sostituire le istanze di questo tipo e il codice associato in modo appropriato per usare la struttura di **\_ archiviazione sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="59e38-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="59e38-125">In alternativa, è possibile eseguire una ricerca nella codebase per le istanze di **sockaddr** e **sockaddr \_ in** strutture e modificare tutto questo utilizzo (e altro codice associato, a seconda del caso) nella struttura di **\_ archiviazione sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="59e38-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="59e38-126">Le strutture di **\_ archiviazione** **addrinfo** e sockaddr includono rispettivamente i membri della famiglia di protocolli e indirizzi (famiglia di **intelligenza artificiale \_** e **\_ famiglia SS**).</span><span class="sxs-lookup"><span data-stu-id="59e38-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="59e38-127">RFC 2553 specifica il membro della **\_ famiglia di intelligenza artificiale** di [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) come int, mentre la **\_ famiglia SS** viene specificata come breve; di conseguenza, una copia diretta tra i membri genera un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="59e38-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="59e38-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59e38-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59e38-129">Guida a IPv6 per le applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="59e38-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="59e38-130">Socket dual stack per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="59e38-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="59e38-131">Chiamate di funzione per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="59e38-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="59e38-132">Utilizzo di indirizzi IPv4 hardcoded</span><span class="sxs-lookup"><span data-stu-id="59e38-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="59e38-133">Problemi dell'interfaccia utente per le applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="59e38-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="59e38-134">Protocolli sottostanti per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="59e38-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
