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
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Modifica delle strutture di dati per applicazioni Winsock IPv6

Quando si aggiunge il supporto per IPv6, è necessario assicurarsi che l'applicazione definisca le strutture dei dati dimensionate correttamente. La dimensione di un indirizzo IPv6 è molto più grande di un indirizzo IPv4. Le strutture hardcoded per gestire le dimensioni di un indirizzo IPv4 durante l'archiviazione di un indirizzo IP provocheranno problemi nell'applicazione e dovranno essere modificate.

Procedura consigliata

L'approccio migliore per garantire che le strutture siano dimensionate correttamente consiste nell'usare la struttura di [**\_ archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) . La struttura di **\_ archiviazione sockaddr** è indipendente dalla versione dell'indirizzo IP. Quando si usa la struttura di **\_ archiviazione sockaddr** per archiviare indirizzi IP, gli indirizzi IPv4 e IPv6 possono essere gestiti correttamente con una codebase.

Nell'esempio seguente, che è un estratto dal file server. c disponibile nell'Appendice B, identifica l'uso appropriato della struttura di **\_ archiviazione sockaddr** . Si noti che la struttura, se utilizzata correttamente come illustrato in questo esempio, gestisce normalmente un indirizzo IPv4 o IPv6.


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
> La struttura di [**\_ archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) è una novità di Windows XP.

 

Codice da evitare

In genere, molte applicazioni utilizzano la struttura [**sockaddr**](sockaddr-2.md) per archiviare indirizzi indipendenti dal protocollo o **sockaddr \_ nella** struttura per gli indirizzi IP. Né la struttura SOCKADDR né **sockaddr \_ nella** struttura sono sufficientemente grandi da contenere gli indirizzi IPv6 e pertanto entrambi sono insufficienti se l'applicazione deve essere compatibile con IPv6.

Attività di codifica

**Per modificare la codebase esistente da IPv4 a IPv4 e IPv6-interoperabilità**

1.  Acquisire l'utilità Checkv4.exe. L'utilità è inclusa nel Software Development Kit (SDK) di Microsoft Windows, che viene reso disponibile tramite l'abbonamento MSDN o dal Web come download.
2.  Eseguire l'utilità Checkv4.exe sul codice. Per informazioni su come eseguire l'utilità di Checkv4.exe sui file, vedere la sezione relativa all' [uso dell'utilità di Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  Tramite l'utilità viene visualizzato un avviso per l'utilizzo di **sockaddr** o **sockaddr \_ in** strutture e vengono fornite indicazioni su come sostituire con la struttura compatibile con IPv6 [**sockaddr \_ archiviazione**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).
4.  Sostituire le istanze di questo tipo e il codice associato in modo appropriato per usare la struttura di **\_ archiviazione sockaddr** .

In alternativa, è possibile eseguire una ricerca nella codebase per le istanze di **sockaddr** e **sockaddr \_ in** strutture e modificare tutto questo utilizzo (e altro codice associato, a seconda del caso) nella struttura di **\_ archiviazione sockaddr** .

> [!Note]  
> Le strutture di **\_ archiviazione** **addrinfo** e sockaddr includono rispettivamente i membri della famiglia di protocolli e indirizzi (famiglia di **intelligenza artificiale \_** e **\_ famiglia SS**). RFC 2553 specifica il membro della **\_ famiglia di intelligenza artificiale** di [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) come int, mentre la **\_ famiglia SS** viene specificata come breve; di conseguenza, una copia diretta tra i membri genera un errore del compilatore.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Socket dual stack per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilizzo di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemi dell'interfaccia utente per le applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
