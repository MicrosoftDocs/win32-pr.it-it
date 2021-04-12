---
description: Il file di inclusione originale per l'uso con Windows Sockets 1,1 è il file di intestazione Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: File di inclusione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343501"
---
# <a name="include-files"></a><span data-ttu-id="d484d-103">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="d484d-103">Include Files</span></span>

<span data-ttu-id="d484d-104">Il file di inclusione originale per l'uso con Windows Sockets 1,1 è il file di intestazione *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="d484d-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="d484d-105">Per semplificare il porting di codice sorgente esistente basato su socket UNIX Berkeley in Windows Sockets, è stato consigliato di fornire i kit di sviluppo di Windows Sockets per Winsock 1,1 con diversi file di inclusione con gli stessi nomi dei file di inclusione UNIX standard (ad esempio, i file di intestazione *sys/socket. h* e arpa/inet. h).</span><span class="sxs-lookup"><span data-stu-id="d484d-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="d484d-106">Tuttavia, questi file di intestazione Winsock con nome analogo contengono semplicemente una direttiva per includere il file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="d484d-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="d484d-107">Quando Windows Sockets 2 è stato rilasciato, il file di inclusione primario per l'uso con Windows Sockets è stato rinominato in *Winsock2. h*.</span><span class="sxs-lookup"><span data-stu-id="d484d-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="d484d-108">Il file di intestazione *Winsock. h* precedente per Winsock 1,1 è stato mantenuto anche per la compatibilità con le applicazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d484d-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="d484d-109">Lo sviluppo di applicazioni compatibili con Winsock 1,1 è stato deprecato poiché Windows 2000 è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="d484d-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="d484d-110">Tutte le applicazioni dovrebbero ora usare la direttiva include *Winsock2. h* nei file di origine dell'applicazione Winsock.</span><span class="sxs-lookup"><span data-stu-id="d484d-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="d484d-111">Il file di intestazione *Winsock2. h* contiene la maggior parte delle funzioni, delle strutture e delle definizioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="d484d-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="d484d-112">Il file di intestazione *Ws2tcpip. h* contiene le definizioni introdotte nel documento di allegato WinSock 2 Protocol-Specific per TCP/IP che include funzioni e strutture più recenti utilizzate per recuperare gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="d484d-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="d484d-113">Sono incluse la famiglia di funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) che forniscono la risoluzione dei nomi per gli indirizzi IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="d484d-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="d484d-114">Il file di intestazione *Ws2tcpip. h* è necessario solo se le funzioni di denominazione indipendenti dall'IP sono richieste dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d484d-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="d484d-115">Il file di intestazione *mswsock. h* contiene le definizioni per le estensioni specifiche di Microsoft per Windows Sockets 2 (ad esempio,[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)e [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)).</span><span class="sxs-lookup"><span data-stu-id="d484d-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="d484d-116">Il file di intestazione *mswsock. h* non è in genere necessario, a meno che le estensioni specifiche di Microsoft non vengano utilizzate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d484d-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="d484d-117">Il file di intestazione *Winsock2. h* include internamente gli elementi di base del file di intestazione di *Windows. h* , quindi non esiste in genere una \# riga di inclusione per il file di intestazione di *Windows. h* nelle applicazioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="d484d-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="d484d-118">Se \# è necessaria una riga di inclusione per il file di intestazione di *Windows. h* , questa operazione deve essere preceduta dalla macro per la \# definizione e la media di Win32 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d484d-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="d484d-119">Per motivi cronologici, per impostazione predefinita l'intestazione *Windows. h* include il file di intestazione *Winsock. h* per Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="d484d-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="d484d-120">Le dichiarazioni nel file di intestazione *Winsock. h* sono in conflitto con le dichiarazioni nel file di intestazione *Winsock2. h* richiesto da Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="d484d-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="d484d-121">La \_ macro Win32 snello \_ e \_ media impedisce che *Winsock. h* venga incluso nell'intestazione *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="d484d-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="d484d-122">Di seguito è riportato un esempio che illustra questo problema.</span><span class="sxs-lookup"><span data-stu-id="d484d-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="d484d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d484d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d484d-124">Creazione di un'applicazione Winsock di base</span><span class="sxs-lookup"><span data-stu-id="d484d-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="d484d-125">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="d484d-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="d484d-126">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="d484d-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="d484d-127">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="d484d-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
