---
description: Abilita la scalabilità della porta locale per un socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565caeb472ac5cb15061d32b47a048a9a210885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129119"
---
# <a name="so_port_scalability"></a><span data-ttu-id="dbb1a-103">\_ \_ scalabilità delle porte</span><span class="sxs-lookup"><span data-stu-id="dbb1a-103">SO\_PORT\_SCALABILITY</span></span>

<span data-ttu-id="dbb1a-104">L'opzione socket **\_ \_ scalabilità porta** è in grado di abilitare la scalabilità delle porte locali per un socket.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-104">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability for a socket.</span></span>

<dl> <dt>

<span data-ttu-id="dbb1a-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_ \_ scalabilità delle porte**</span><span class="sxs-lookup"><span data-stu-id="dbb1a-105"><span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**SO\_PORT\_SCALABILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbb1a-106">0x3006</span><span class="sxs-lookup"><span data-stu-id="dbb1a-106">0x3006</span></span>
</dt> <dt>



<span data-ttu-id="dbb1a-107">L'opzione per il socket di **\_ \_ scalabilità** delle porte consente la scalabilità della porta locale consentendo l'ingrandimento dell'allocazione delle porte allocando più volte le porte con caratteri jolly per diverse coppie di porte di indirizzi locali in un computer locale</span><span class="sxs-lookup"><span data-stu-id="dbb1a-107">The **SO\_PORT\_SCALABILITY** socket option enables local port scalability by allowing port allocation to be maximized by allocating wildcard ports multiple times for different local address port pairs on a local machine.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbb1a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbb1a-108">Remarks</span></span>

<span data-ttu-id="dbb1a-109">Nota: sulle piattaforme in cui \_ \_ sono supportate sia la scalabilità delle porte che quindi il \_ riutilizzo \_ di UNICASTPORT, è preferibile usare questo \_ \_ UNICASTPORT.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-109">Note: on platforms where both SO\_PORT\_SCALABILITY and SO\_REUSE\_UNICASTPORT are supported, prefer to use SO\_REUSE\_UNICASTPORT.</span></span>

<span data-ttu-id="dbb1a-110">Gli ambienti del server proxy presentano problemi di scalabilità a causa della disponibilità limitata delle porte locali.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-110">Proxy server environments have scalability issues because of limited local port availability.</span></span> <span data-ttu-id="dbb1a-111">Un modo per risolvere questo problema consiste nell'aggiungere altri indirizzi IP al computer.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-111">One way to work around this is to add more IP addresses to the machine.</span></span> <span data-ttu-id="dbb1a-112">Tuttavia, per impostazione predefinita, le porte con caratteri jolly usati con la funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) sono limitate alla dimensione dell'intervallo di porte dinamiche nel computer locale (fino alle porte 64K, ma in genere meno) indipendentemente dal numero di indirizzi IP nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-112">However, by default wildcard ports used with the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function are limited to the size of the dynamic port range on the local machine (up to 64K ports, but usually less) no matter the number of IP addresses on the local machine.</span></span> <span data-ttu-id="dbb1a-113">Per risolvere questo problema, è necessario che l'applicazione mantenga il proprio pool di porte con la prenotazione delle porte o con l'euristica.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-113">Working around this requires the application to maintain its own port pool either with port reservation or by using heuristics.</span></span>

<span data-ttu-id="dbb1a-114">Per evitare che tutte le applicazioni che richiedono la scalabilità gestiscano il proprio pool di porte e che consentano una maggiore scalabilità mantenendo la compatibilità delle applicazioni, in Windows Server 2008 è stata introdotta l'opzione per il socket di **\_ \_ scalabilità** delle porte che consente di ottimizzare l'allocazione</span><span class="sxs-lookup"><span data-stu-id="dbb1a-114">To avoid having every application that requires scalability manage its own port pool, and to allow for greater scalability while maintaining application compatibility, Windows Server 2008 introduced the **SO\_PORT\_SCALABILITY** socket option to help maximize wildcard port allocation.</span></span> <span data-ttu-id="dbb1a-115">L'allocazione delle porte viene ottimizzata consentendo a un'applicazione di allocare le porte con caratteri jolly per ogni coppia di porte e indirizzi locali univoci.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-115">Port allocation is maximized by allowing an application to allocate wildcard ports for each unique local address and port pair.</span></span> <span data-ttu-id="dbb1a-116">Quindi, se un computer locale dispone di quattro indirizzi IP, è possibile allocare fino a 256 K porte con caratteri jolly (64 K porte × 4 indirizzi IP) tramite le richieste di funzioni di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-116">So if a local machine has four IP addresses, then up to 256 K wildcard ports (64 K ports × 4 IP addresses) can be allocated by wildcard [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function requests.</span></span>

<span data-ttu-id="dbb1a-117">Quando l'opzione socket **\_ \_ scalabilità porta** è impostata su un socket e viene eseguita una chiamata alla funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) per un indirizzo specificato e una porta con caratteri jolly (il parametro *Name* è impostato con un indirizzo specifico e una porta 0), Winsock alloca una porta per l'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-117">When the **SO\_PORT\_SCALABILITY** socket option is set on a socket and a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is made for a specified address and wildcard port (the *name* parameter is set with a specific address and a port of 0), Winsock will allocate a port for the specified address.</span></span> <span data-ttu-id="dbb1a-118">Questa allocazione sarà basata su tutti i possibili indirizzi IP e porte/per indirizzo nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-118">This allocation will be based on all of the possible IP addresses and ports/per address on the local computer.</span></span> <span data-ttu-id="dbb1a-119">Se una porta con caratteri jolly viene acquisita utilizzando l'opzione **per la \_ \_ scalabilità della porta** , tale porta non può essere allocata da un altro socket senza l'opzione di **\_ \_ scalabilità delle porte** .</span><span class="sxs-lookup"><span data-stu-id="dbb1a-119">If a wildcard port is acquired using the **SO\_PORT\_SCALABILITY** option, that port cannot be allocated by another socket without the **SO\_PORT\_SCALABILITY** option.</span></span> <span data-ttu-id="dbb1a-120">Questa restrizione è prevista per evitare problemi di compatibilità con le applicazioni che presuppongono una porta locale con caratteri jolly non può essere riutilizzata.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-120">This restriction is in place to avoid backward-compatibility problems with applications that assume a wildcard local port cannot be reused.</span></span> <span data-ttu-id="dbb1a-121">Si noti che questo significa che le applicazioni che acquisiscono un numero elevato di porte usando **così la \_ \_ scalabilità** delle porte possono decarere le applicazioni legacy delle porte.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-121">Note that this means that applications which acquire a large number of ports using **SO\_PORT\_SCALABILITY** can starve legacy applications of ports.</span></span> <span data-ttu-id="dbb1a-122">Se tutte le porte temporanee disponibili sono state acquisite per almeno un indirizzo con la **\_ \_ scalabilità della porta** , non è possibile allocare più porte con caratteri jolly senza l'opzione socket.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-122">If all available ephemeral ports have been acquired for at least one address with **SO\_PORT\_SCALABILITY** , then no more wildcard port allocations are possible without the socket option.</span></span>

<span data-ttu-id="dbb1a-123">Per avere un effetto, è necessario impostare l'opzione per la **\_ \_ scalabilità della porta** , prima di chiamare la funzione di [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="dbb1a-123">To have any effect, the **SO\_PORT\_SCALABILITY** option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called.</span></span> <span data-ttu-id="dbb1a-124">Di seguito è riportato un esempio di come verrà usato in un computer con due indirizzi:</span><span class="sxs-lookup"><span data-stu-id="dbb1a-124">An example of how this would be used on a computer with two addresses is outlined below:</span></span>

-   <span data-ttu-id="dbb1a-125">La funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) viene chiamata da un processo per creare un socket.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-125">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by a process to create a socket.</span></span>
-   <span data-ttu-id="dbb1a-126">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) viene chiamata per abilitare l'opzione socket di **\_ \_ scalabilità delle porte** nel socket appena creato.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-126">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created socket.</span></span>
-   <span data-ttu-id="dbb1a-127">La funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) viene chiamata per eseguire un'associazione su uno degli indirizzi IP del computer locale e sulla porta 0.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-127">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called to do a bind on one of the local computer's IP addresses and port 0.</span></span>
-   <span data-ttu-id="dbb1a-128">La funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene quindi chiamata per connettersi a un indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-128">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="dbb1a-129">Il socket viene usato dall'applicazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-129">The socket is used by the application as needed.</span></span>
-   <span data-ttu-id="dbb1a-130">Una funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) viene chiamata dallo stesso processo (possibilmente un thread diverso) per creare un secondo socket.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-130">A [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function is called by the same process (possibly a different thread) to create a second socket.</span></span>
-   <span data-ttu-id="dbb1a-131">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) viene chiamata per abilitare l'opzione socket di **\_ \_ scalabilità delle porte** nel secondo socket appena creato.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-131">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function is called to enable the **SO\_PORT\_SCALABILITY** socket option on the newly created second socket.</span></span>
-   <span data-ttu-id="dbb1a-132">La funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) viene chiamata con il secondo indirizzo IP del computer locale e la porta 0.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-132">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called with the local computer's second IP address and port 0.</span></span> <span data-ttu-id="dbb1a-133">Anche quando tutte le porte sono state allocate in precedenza, la chiamata ha esito positivo perché nel computer locale sono disponibili più indirizzi IP e l'opzione per il socket di **\_ \_ scalabilità della porta** è stata impostata su entrambi i socket nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-133">Even when all ports have been previously allocated, this call succeeds because there are multiple IP addresses available on the local computer and the **SO\_PORT\_SCALABILITY** socket option was set on both sockets in the same process.</span></span>
-   <span data-ttu-id="dbb1a-134">La funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) viene quindi chiamata per connettersi a un indirizzo IP remoto.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-134">The [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function is then called to connect to a remote IP address.</span></span> <span data-ttu-id="dbb1a-135">Il secondo socket viene usato dall'applicazione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="dbb1a-135">The second socket is used by the application as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb1a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbb1a-136">Requirements</span></span>



| <span data-ttu-id="dbb1a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb1a-137">Requirement</span></span> | <span data-ttu-id="dbb1a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="dbb1a-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb1a-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbb1a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb1a-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dbb1a-140">None supported</span></span><br/>                                                           |
| <span data-ttu-id="dbb1a-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbb1a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb1a-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbb1a-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dbb1a-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbb1a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb1a-144"><dt>Ws2def. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb1a-144"><dt>Ws2def.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb1a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbb1a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb1a-146">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="dbb1a-146">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="dbb1a-147">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="dbb1a-147">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="dbb1a-148">**\_Opzioni Socket socket Sol**</span><span class="sxs-lookup"><span data-stu-id="dbb1a-148">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="dbb1a-149">**Opzioni socket**</span><span class="sxs-lookup"><span data-stu-id="dbb1a-149">**Socket Options**</span></span>](socket-options.md)
</dt> </dl>

 

 




