---
description: L' \_ ordinamento dell' \_ elenco di indirizzi sio \_ consente agli sviluppatori di applicazioni di ordinare un elenco di indirizzi IPv6 e IPv4 di destinazione per determinare il migliore indirizzo disponibile per l'esecuzione di una connessione. L' \_ ordinamento dell'elenco di indirizzi sio \_ \_ è supportato in Windows XP e versioni successive.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Utilizzo di SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233483"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="b3868-104">Uso dell' \_ \_ ordinamento dell'elenco di indirizzi sio \_</span><span class="sxs-lookup"><span data-stu-id="b3868-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="b3868-105">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** consente agli sviluppatori di applicazioni di ordinare un elenco di indirizzi IPv6 e IPv4 di destinazione per determinare il migliore indirizzo disponibile per l'esecuzione di una connessione.</span><span class="sxs-lookup"><span data-stu-id="b3868-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="b3868-106">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è supportato in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3868-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="b3868-107">In Windows Vista e versioni successive, la funzione [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) accetta un elenco fornito di indirizzi IP di destinazione potenziali, associa gli indirizzi di destinazione agli indirizzi IP locali del computer host e ordina le coppie in base alla coppia di indirizzi più adatta per la comunicazione tra i due peer.</span><span class="sxs-lookup"><span data-stu-id="b3868-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="b3868-108">La funzione **CreateSortedAddressPairs** deve essere utilizzata al posto dell' **elenco di indirizzi Sio di \_ \_ \_ ordinamento** in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3868-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="b3868-109">Le sezioni seguenti descrivono le considerazioni sull'utilizzo per l' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio**.</span><span class="sxs-lookup"><span data-stu-id="b3868-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3868-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3868-110">Parameters</span></span>

<span data-ttu-id="b3868-111">Il buffer passato all' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è una struttura dell' [**\_ \_ elenco di indirizzi del socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3868-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="b3868-112">Ogni [**\_ indirizzo del socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) nell'elenco deve essere in \_ formato sockaddr IN6.</span><span class="sxs-lookup"><span data-stu-id="b3868-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="b3868-113">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** Ordina gli indirizzi IPv6 e IPv4 in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3868-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="b3868-114">Tutti gli indirizzi IPv4 nell'elenco da ordinare devono essere nel formato di indirizzo IPv6 mappato a IPv4.</span><span class="sxs-lookup"><span data-stu-id="b3868-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="b3868-115">Per ulteriori informazioni sul formato degli indirizzi IPv6 con mapping IPv4, vedere [socket a doppio stack](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="b3868-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="b3868-116">In Windows Server 2003 e Windows XP, l' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** Ordina solo gli indirizzi IPv6.</span><span class="sxs-lookup"><span data-stu-id="b3868-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="b3868-117">Gli indirizzi IPv4 nel formato di indirizzo IPv6 con mapping IPv4 non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="b3868-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="b3868-118">Nell'output, il membro **iAddressCount** della struttura [**dell' \_ \_ elenco di indirizzi del socket**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) può essere minore dell'input se il codice IOCTL determina che alcuni indirizzi di destinazione non sono validi.</span><span class="sxs-lookup"><span data-stu-id="b3868-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="b3868-119">Determinazione dell'ordinamento</span><span class="sxs-lookup"><span data-stu-id="b3868-119">Sorting Determination</span></span>

<span data-ttu-id="b3868-120">L'ordinamento degli indirizzi IPv6 per l' \_ ordinamento dell'elenco di indirizzi sio \_ \_ è basato sulla tabella dei criteri di prefisso.</span><span class="sxs-lookup"><span data-stu-id="b3868-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="b3868-121">La tabella dei criteri di prefisso viene configurata tramite l'utilità da riga di comando *Netsh.exe* .</span><span class="sxs-lookup"><span data-stu-id="b3868-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="b3868-122">I frammenti di codice seguenti della riga di comando illustrano i comandi di configurazione della tabella dei criteri di base *Netsh.exe* prefisso:</span><span class="sxs-lookup"><span data-stu-id="b3868-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="b3868-123">In Windows Server 2003 e Windows XP il primo comando netsh elencato sopra è il seguente.</span><span class="sxs-lookup"><span data-stu-id="b3868-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="b3868-124">Tutti gli altri comandi correlati sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b3868-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="b3868-125">L'ordinamento degli indirizzi è determinato anche da un algoritmo descritto nella specifica RFC 3484 sulla *selezione di indirizzi predefiniti per il protocollo IP versione 6 (IPv6)* pubblicata da IETF.</span><span class="sxs-lookup"><span data-stu-id="b3868-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="b3868-126">Per altre informazioni, vedere [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span><span class="sxs-lookup"><span data-stu-id="b3868-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="b3868-127">Questa risorsa può essere disponibile solo in inglese.</span><span class="sxs-lookup"><span data-stu-id="b3868-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="b3868-128">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** Ordina gli indirizzi dal migliore al peggiore e compila i membri con **\_ \_ ID ambito sin6** , se necessario.</span><span class="sxs-lookup"><span data-stu-id="b3868-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="b3868-129">Per gli indirizzi locali del sito, l' \_ ordinamento dell'elenco di indirizzi sio \_ \_ riempie l'ID ambito o rimuove l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="b3868-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="b3868-130">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** ignora l'indirizzo di origine associato al socket e ordina in base all'elenco di indirizzi di destinazione passato come parametro.</span><span class="sxs-lookup"><span data-stu-id="b3868-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="b3868-131">La funzione [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) deve essere utilizzata al posto dell' **elenco di indirizzi Sio di \_ \_ \_ ordinamento** in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3868-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="b3868-132">La funzione **CreateSortedAddressPairs** restituisce un elenco di coppie di indirizzi che contengono un indirizzo di origine locale e un indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b3868-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="b3868-133">Fornisce a un'applicazione l'indirizzo di origine corretto da usare per ogni indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b3868-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="b3868-134">Un'applicazione può anche filtrare i risultati cercando un indirizzo di origine specifico.</span><span class="sxs-lookup"><span data-stu-id="b3868-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="b3868-135">nei risultati.</span><span class="sxs-lookup"><span data-stu-id="b3868-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3868-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3868-136">Requirements</span></span>

<span data-ttu-id="b3868-137">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è definito nel file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="b3868-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="b3868-138">In Microsoft Windows Software Development Kit (SDK) rilasciata per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e l' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è definito nel file di intestazione *Ws2def. h* .</span><span class="sxs-lookup"><span data-stu-id="b3868-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="b3868-139">Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="b3868-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="b3868-140">L' **\_ ordinamento dell' \_ elenco \_ di indirizzi sio** è supportato in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b3868-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3868-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3868-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3868-142">**CreateSortedAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="b3868-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
