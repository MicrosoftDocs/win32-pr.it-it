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
# <a name="sockaddr"></a><span data-ttu-id="ecdd4-103">sockaddr</span><span class="sxs-lookup"><span data-stu-id="ecdd4-103">sockaddr</span></span>

<span data-ttu-id="ecdd4-104">La struttura SOCKADDR varia a seconda del protocollo selezionato.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-104">The sockaddr structure varies depending on the protocol selected.</span></span> <span data-ttu-id="ecdd4-105">Ad eccezione del parametro della *\* \_ famiglia sin* , il contenuto di SOCKADDR viene espresso nell'ordine dei byte di rete.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-105">Except for the *sin\*\_family* parameter, sockaddr contents are expressed in network byte order.</span></span>

<span data-ttu-id="ecdd4-106">Le funzioni Winsock che usano sockaddr non vengono interpretate in modo rigoroso come puntatori a una struttura sockaddr.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-106">Winsock functions using sockaddr are not strictly interpreted to be pointers to a sockaddr structure.</span></span> <span data-ttu-id="ecdd4-107">La struttura viene interpretata in modo diverso nel contesto di famiglie di indirizzi diverse.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-107">The structure is interpreted differently in the context of different address families.</span></span> <span data-ttu-id="ecdd4-108">Gli unici requisiti sono che il primo **\_ short u** è la famiglia di indirizzi e le dimensioni totali del buffer di memoria in byte sono *namelen*.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-108">The only requirements are that the first **u\_short** is the address family and the total size of the memory buffer in bytes is *namelen*.</span></span>

<span data-ttu-id="ecdd4-109">La struttura di [**\_ archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) archivia anche le informazioni sull'indirizzo del socket e la struttura è sufficientemente grande per archiviare le informazioni sull'indirizzo IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-109">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure also stores socket address information and the structure is sufficiently large to store IPv4 or IPv6 address information.</span></span> <span data-ttu-id="ecdd4-110">L'uso della struttura **di \_ archiviazione sockaddr** promuove la famiglia di protocolli e l'indipendenza dalla versione del protocollo e semplifica lo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-110">The use of the **SOCKADDR\_STORAGE** structure promotes protocol-family and protocol-version independence, and simplifies development.</span></span> <span data-ttu-id="ecdd4-111">È consigliabile usare la struttura **di \_ archiviazione sockaddr** al posto della struttura sockaddr.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-111">It is recommended that the **SOCKADDR\_STORAGE** structure be used in place of the sockaddr structure.</span></span> <span data-ttu-id="ecdd4-112">La struttura di **\_ archiviazione sockaddr** è supportata in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-112">The **SOCKADDR\_STORAGE** structure is supported on Windows Server 2003 and later.</span></span>

<span data-ttu-id="ecdd4-113">La struttura SOCKADDR e sockaddr \_ nelle strutture seguenti vengono usate con IPv4.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-113">The sockaddr structure and sockaddr\_in structures below are used with IPv4.</span></span> <span data-ttu-id="ecdd4-114">Altri protocolli utilizzano strutture simili.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-114">Other protocols use similar structures.</span></span>

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

<span data-ttu-id="ecdd4-115">\_ \_ Con IPv6 vengono usate le strutture sockaddr IN6 e sockaddr IN6 \_ precedenti.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-115">The sockaddr\_in6 and sockaddr\_in6\_old structures below are used with IPv6.</span></span>

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

<span data-ttu-id="ecdd4-116">In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, **sockaddr** e **sockaddr \_ nei** Tag typedef vengono definiti per SOCKADDR e sockaddr \_ nelle strutture come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ecdd4-116">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, **SOCKADDR** and **SOCKADDR\_IN** typedef tags are defined for sockaddr and sockaddr\_in structures as follows:</span></span>

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

<span data-ttu-id="ecdd4-117">Nella Windows SDK rilasciata per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è cambiata e le SOCKADDR e sockaddr \_ nelle strutture sono definite nel file di intestazione *Ws2def. h* , non nel file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="ecdd4-117">On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the sockaddr and sockaddr\_in structures are defined in the *Ws2def.h* header file, not the *Winsock2.h* header file.</span></span> <span data-ttu-id="ecdd4-118">Il file di intestazione *Ws2def. h* viene incluso automaticamente nel file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="ecdd4-118">The *Ws2def.h* header file is automatically included by the *Winsock2.h* header file.</span></span> <span data-ttu-id="ecdd4-119">La \_ struttura SOCKADDR IN6 viene definita nel file di intestazione *Ws2ipdef. h* , non nel file di intestazione *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="ecdd4-119">The sockaddr\_in6 structure is defined in the *Ws2ipdef.h* header file, not the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="ecdd4-120">Il file di intestazione *Ws2ipdef. h* viene incluso automaticamente nel file di intestazione *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="ecdd4-120">The *Ws2ipdef.h* header file is automatically included by the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="ecdd4-121">I file di intestazione *Ws2def. h* e *Ws2ipdef. h* non devono mai essere usati direttamente.</span><span class="sxs-lookup"><span data-stu-id="ecdd4-121">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="example-code"></a><span data-ttu-id="ecdd4-122">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="ecdd4-122">Example Code</span></span>

<span data-ttu-id="ecdd4-123">Nell'esempio seguente viene illustrato l'utilizzo della struttura **sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="ecdd4-123">The following example demonstrates the use of the **sockaddr** structure.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="ecdd4-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ecdd4-124">See Also</span></span>

<span data-ttu-id="ecdd4-125">[**\_archiviazione sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ecdd4-125">[**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span></span>


 

 
