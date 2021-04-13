---
description: È sempre necessario tenere conto di eventuali differenze tra l'ordine dei byte utilizzato per archiviare numeri interi dall'architettura host e l'ordine dei byte utilizzato in transito dai singoli protocolli di trasporto.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordine dei byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484956"
---
# <a name="byte-ordering"></a><span data-ttu-id="8b1ba-103">ordine dei byte</span><span class="sxs-lookup"><span data-stu-id="8b1ba-103">Byte Ordering</span></span>

<span data-ttu-id="8b1ba-104">È sempre necessario tenere conto di eventuali differenze tra l'ordine dei byte utilizzato per archiviare numeri interi dall'architettura host e l'ordine dei byte utilizzato in transito dai singoli protocolli di trasporto.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="8b1ba-105">Qualsiasi riferimento a un indirizzo o a un numero di porta passato a o da una routine di Windows Sockets deve essere nell'ordine di rete (big-endian) per il protocollo utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="8b1ba-106">Nel caso di IP, sono inclusi i parametri relativi all'indirizzo IP e alla porta di una struttura [**sockaddr**](sockaddr-2.md) (ma non al parametro della *\_ famiglia sin* ).</span><span class="sxs-lookup"><span data-stu-id="8b1ba-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="8b1ba-107">Alcuni sistemi UNIX operano su CPU che rappresentano numeri interi in ordine byte di rete (big-endian).</span><span class="sxs-lookup"><span data-stu-id="8b1ba-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="8b1ba-108">Pertanto la necessità di convertire numeri interi dall'ordine dei byte dell'host all'ordine dei byte di rete può essere ignorata senza causare problemi anche se questa opzione non è consigliata per la portabilità.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="8b1ba-109">Al contrario, l'ordine dei byte utilizzato per rappresentare i numeri interi per la maggior parte delle CPU Intel® è Little-endian.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="8b1ba-110">Pertanto, è diventato obbligatorio che i numeri interi vengano convertiti da host byte order a byte di rete prima di essere utilizzati nelle funzioni e nelle strutture dei socket Winsock.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="8b1ba-111">Si consideri un'applicazione che in genere Contatta un server sulla porta TCP corrispondente al servizio ora, ma fornisce un meccanismo che consente all'utente di specificare una porta alternativa.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="8b1ba-112">Il numero di porta restituito da [**GetServByName**](/windows/desktop/api/winsock/nf-winsock-getservbyname) è già in ordine di rete, ovvero il formato necessario per costruire un indirizzo in modo che non sia necessaria alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="8b1ba-113">Tuttavia, se l'utente sceglie di usare una porta diversa, immessa come Integer, l'applicazione deve convertirla dall'host all'ordine di rete TCP/IP (usando la funzione [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) o [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) prima di usarla per costruire un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="8b1ba-114">Viceversa, se l'applicazione dovesse visualizzare il numero di porta all'interno di un indirizzo (restituito da [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , ad esempio), il numero di porta deve essere convertito dalla rete all'ordine host (usando la funzione [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) o [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) prima di poter essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="8b1ba-115">Poiché gli ordini di byte Intel e Internet sono diversi, le conversioni descritte in precedenza sono inevitabili.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="8b1ba-116">Gli sviluppatori di applicazioni si avvertono che devono utilizzare le funzioni di conversione standard fornite come parte di Winsock anziché scrivere il proprio codice di conversione, in quanto le future implementazioni di Winsock probabilmente verranno eseguite su sistemi per i quali l'ordine host è identico all'ordine dei byte di rete.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="8b1ba-117">Sono probabilmente portabili solo le applicazioni che utilizzano le funzioni di conversione standard tra l'ordine dei byte host e rete.</span><span class="sxs-lookup"><span data-stu-id="8b1ba-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b1ba-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b1ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b1ba-119">**getpeername**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="8b1ba-120">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="8b1ba-121">**htonl**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="8b1ba-122">**htons**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="8b1ba-123">**ntohl**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="8b1ba-124">**ntohs**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="8b1ba-125">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="8b1ba-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="8b1ba-126">**sockaddr**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="8b1ba-127">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="8b1ba-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="8b1ba-128">**WSAHtonl**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="8b1ba-129">**WSAHtons**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="8b1ba-130">**WSANtohl**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="8b1ba-131">**WSANtohs**</span><span class="sxs-lookup"><span data-stu-id="8b1ba-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



