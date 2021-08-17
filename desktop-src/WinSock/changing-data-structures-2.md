---
description: Quando si aggiunge il supporto per IPv6, è necessario assicurarsi che l'applicazione definirà strutture di dati dimensionate correttamente.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Modifica delle strutture dei dati per le applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741551"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Modifica delle strutture dei dati per le applicazioni Winsock IPv6

Quando si aggiunge il supporto per IPv6, è necessario assicurarsi che l'applicazione definirà strutture di dati dimensionate correttamente. Le dimensioni di un indirizzo IPv6 sono molto più grandi di un indirizzo IPv4. Le strutture hard-coded per gestire le dimensioni di un indirizzo IPv4 quando si archivia un indirizzo IP causeranno problemi nell'applicazione e devono essere modificate.

Procedura consigliata

L'approccio migliore per assicurarsi che le strutture siano dimensionate correttamente consiste nell'usare la struttura di archiviazione [**SOCKADDR. \_**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) La **struttura di \_ archiviazione SOCKADDR** è indipendente dalla versione dell'indirizzo IP. Quando la struttura di archiviazione **SOCKADDR \_** viene usata per archiviare gli indirizzi IP, gli indirizzi IPv4 e IPv6 possono essere gestiti correttamente con una codebase.

L'esempio seguente, che è un estratto del file Server.c disponibile nell'Appendice B, identifica un uso appropriato della struttura di archiviazione **SOCKADDR. \_** Si noti che la struttura , se usata correttamente come illustrato in questo esempio, gestisce normalmente un indirizzo IPv4 o IPv6.


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
> La [**struttura DI \_ ARCHIVIAZIONE SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) è una novità per Windows XP.

 

Codice da evitare

In genere, molte applicazioni usava la struttura [**sockaddr**](sockaddr-2.md) per archiviare gli indirizzi indipendenti dal protocollo o **il sockaddr \_ nella** struttura per gli indirizzi IP. Né la struttura sockaddr né il **sockaddr \_** nella struttura sono sufficientemente grandi da contenere gli indirizzi IPv6 e pertanto entrambi non sono sufficienti se l'applicazione deve essere compatibile con IPv6.

Attività Di codifica

**Per modificare la codebase esistente da IPv4 all'interoperabilità IPv4 e IPv6**

1.  Acquisire l'Checkv4.exe di installazione. L'utilità è inclusa in Microsoft Windows Software Development Kit (SDK) che viene reso disponibile tramite la sottoscrizione MSDN o dal Web come download.
2.  Eseguire l'Checkv4.exe'utilità sul codice. Per informazioni su come eseguire l'utilità Checkv4.exe sui file, vedere la sezione [Uso dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  L'utilità avvisa l'utente dell'utilizzo di **sockaddr** o **sockaddr \_** nelle strutture e fornisce indicazioni su come sostituire con la struttura compatibile con IPv6 [**SOCKADDR \_ STORAGE.**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))
4.  Sostituire tali istanze e il codice associato in base alle esigenze per usare la struttura di archiviazione **SOCKADDR. \_**

In alternativa, è possibile cercare nella codebase le istanze di **sockaddr** e **sockaddr \_ nelle** strutture e modificare tutto questo utilizzo (e altro codice associato, in base alle esigenze) nella struttura DI ARCHIVIAZIONE **SOCKADDR. \_**

> [!Note]  
> Le strutture di archiviazione **addrinfo** e **\_ SOCKADDR** includono rispettivamente i membri della famiglia di protocolli e indirizzi **(famiglia di \_** intelligenza artificiale e famiglia **ss). \_** RFC 2553 specifica **\_** il membro della famiglia di intelligenza artificiale di [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) come int, mentre la famiglia **ss \_** viene specificata come breve; di conseguenza, una copia diretta tra tali membri genera un errore del compilatore.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Dual-Stack Sockets per applicazioni Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interfaccia utente problemi relativi alle applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
