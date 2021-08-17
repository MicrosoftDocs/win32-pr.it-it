---
description: La struttura sockaddr varia a seconda del protocollo selezionato.
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
ms.openlocfilehash: afdacd0b4579bcb73bfaaa2da0b3714c7d597d94c0d25020e7353e3afd168d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927322"
---
# <a name="sockaddr"></a>sockaddr

La struttura sockaddr varia a seconda del protocollo selezionato. Ad eccezione del *parametro \* \_ sin family,* il contenuto di sockaddr viene espresso nell'ordine dei byte di rete.

Le funzioni Winsock che usano sockaddr non vengono interpretate in modo rigoroso come puntatori a una struttura sockaddr. La struttura viene interpretata in modo diverso nel contesto di diverse famiglie di indirizzi. Gli unici requisiti sono che il primo **u \_ short** sia la famiglia di indirizzi e la dimensione totale del buffer di memoria in byte sia *namelen*.

La [**struttura SOCKADDR \_ STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) archivia anche le informazioni sull'indirizzo socket e la struttura è sufficientemente grande per archiviare le informazioni sugli indirizzi IPv4 o IPv6. L'uso della **struttura SOCKADDR \_ STORAGE** promuove l'indipendenza della famiglia di protocolli e della versione del protocollo e semplifica lo sviluppo. È consigliabile usare la **struttura SOCKADDR \_ STORAGE** al posto della struttura sockaddr. La **struttura SOCKADDR \_ STORAGE** è supportata in Windows Server 2003 e versioni successive.

La struttura sockaddr e il sockaddr nelle strutture seguenti \_ vengono usati con IPv4. Altri protocolli usano strutture simili.

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

I sockaddr \_ in6 e sockaddr in6 strutture vecchie seguenti \_ vengono usati con \_ IPv6.

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

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, i tag typedef **SOCKADDR** e **SOCKADDR \_ IN** vengono definiti per sockaddr e sockaddr nelle strutture come indicato di \_ seguito:

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

In Windows SDK rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il sockaddr e il sockaddr nelle strutture sono definiti nel file di intestazione \_ *Ws2def.h,* non nel file di intestazione *Winsock2.h.* Il file *di intestazione Ws2def.h* viene incluso automaticamente dal file *di intestazione Winsock2.h.* La struttura sockaddr in6 è definita nel file di intestazione \_ *Ws2ipdef.h,* non nel file di intestazione *Ws2tcpip.h.* Il file *di intestazione Ws2ipdef.h* viene incluso automaticamente dal file di intestazione *Ws2tcpip.h.* I *file di intestazione Ws2def.h* e *Ws2ipdef.h* non devono mai essere usati direttamente.

## <a name="example-code"></a>Codice di esempio

L'esempio seguente illustra l'uso della **struttura sockaddr.**


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

[**ARCHIVIAZIONE SOCKADDR \_**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
