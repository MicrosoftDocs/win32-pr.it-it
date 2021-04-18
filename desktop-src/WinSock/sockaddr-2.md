---
description: La struttura SOCKADDR varia a seconda del protocollo selezionato.
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: sockaddr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310428"
---
# <a name="sockaddr"></a>sockaddr

La struttura SOCKADDR varia a seconda del protocollo selezionato. Ad eccezione del parametro della *\* \_ famiglia sin* , il contenuto di SOCKADDR viene espresso nell'ordine dei byte di rete.

Le funzioni Winsock che usano sockaddr non vengono interpretate in modo rigoroso come puntatori a una struttura sockaddr. La struttura viene interpretata in modo diverso nel contesto di famiglie di indirizzi diverse. Gli unici requisiti sono che il primo **\_ short u** è la famiglia di indirizzi e le dimensioni totali del buffer di memoria in byte sono *namelen*.

La struttura di [**\_ archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) archivia anche le informazioni sull'indirizzo del socket e la struttura è sufficientemente grande per archiviare le informazioni sull'indirizzo IPv4 o IPv6. L'uso della struttura **di \_ archiviazione sockaddr** promuove la famiglia di protocolli e l'indipendenza dalla versione del protocollo e semplifica lo sviluppo. È consigliabile usare la struttura **di \_ archiviazione sockaddr** al posto della struttura sockaddr. La struttura di **\_ archiviazione sockaddr** è supportata in Windows Server 2003 e versioni successive.

La struttura SOCKADDR e sockaddr \_ nelle strutture seguenti vengono usate con IPv4. Altri protocolli utilizzano strutture simili.

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

\_ \_ Con IPv6 vengono usate le strutture sockaddr IN6 e sockaddr IN6 \_ precedenti.

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, **sockaddr** e **sockaddr \_ nei** Tag typedef vengono definiti per SOCKADDR e sockaddr \_ nelle strutture come indicato di seguito:

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

Nella Windows SDK rilasciata per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è cambiata e le SOCKADDR e sockaddr \_ nelle strutture sono definite nel file di intestazione *Ws2def. h* , non nel file di intestazione *Winsock2. h* . Il file di intestazione *Ws2def. h* viene incluso automaticamente nel file di intestazione *Winsock2. h* . La \_ struttura SOCKADDR IN6 viene definita nel file di intestazione *Ws2ipdef. h* , non nel file di intestazione *Ws2tcpip. h* . Il file di intestazione *Ws2ipdef. h* viene incluso automaticamente nel file di intestazione *Ws2tcpip. h* . I file di intestazione *Ws2def. h* e *Ws2ipdef. h* non devono mai essere usati direttamente.

## <a name="example-code"></a>Codice di esempio

Nell'esempio seguente viene illustrato l'utilizzo della struttura **sockaddr** .


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a>Vedere anche

[**\_archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
