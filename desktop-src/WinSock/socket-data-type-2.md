---
description: Nelle applicazioni Winsock, un descrittore di socket non è un descrittore di file e deve essere usato con le funzioni Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo di dati socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347066"
---
# <a name="socket-data-type"></a><span data-ttu-id="2f9e9-103">Tipo di dati socket</span><span class="sxs-lookup"><span data-stu-id="2f9e9-103">Socket Data Type</span></span>

<span data-ttu-id="2f9e9-104">Nelle applicazioni Winsock, un descrittore di socket non è un descrittore di file e deve essere usato con le funzioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="2f9e9-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="2f9e9-105">In UNIX, un descrittore di socket è rappresentato da un descrittore di file standard.</span><span class="sxs-lookup"><span data-stu-id="2f9e9-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="2f9e9-106">Di conseguenza, un descrittore di socket in UNIX può essere passato a una delle funzioni standard di I/O dei file (ad esempio, lettura e scrittura).</span><span class="sxs-lookup"><span data-stu-id="2f9e9-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="2f9e9-107">Inoltre, tutti gli handle in UNIX, inclusi gli handle di socket, sono numeri interi non negativi e alcune applicazioni si basano su presupposti che questa operazione sarà vera.</span><span class="sxs-lookup"><span data-stu-id="2f9e9-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="2f9e9-108">Gli handle di Windows Sockets non hanno restrizioni, a parte il valore \_ socket non valido non è un socket valido.</span><span class="sxs-lookup"><span data-stu-id="2f9e9-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="2f9e9-109">Gli handle di socket possono avere un valore compreso nell'intervallo da 0 a socket non valido \_ -1.</span><span class="sxs-lookup"><span data-stu-id="2f9e9-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="2f9e9-110">Poiché il tipo di **socket** non è firmato, la compilazione del codice sorgente esistente da, ad esempio, un ambiente UNIX può causare avvisi del compilatore sulle mancate corrispondenze tra tipi di dati firmati e non firmati.</span><span class="sxs-lookup"><span data-stu-id="2f9e9-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="2f9e9-111">Ciò significa, ad esempio, che il controllo degli errori quando le funzioni [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) restituite non deve essere eseguito confrontando il valore restituito con-1 o verificando se il valore è negativo (approcci comuni e validi in UNIX).</span><span class="sxs-lookup"><span data-stu-id="2f9e9-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="2f9e9-112">Al contrario, un'applicazione deve usare il socket costante manifesto non valido \_ come definito nel file di intestazione *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="2f9e9-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="2f9e9-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2f9e9-113">For example:</span></span>

<span data-ttu-id="2f9e9-114">Tipico stile BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="2f9e9-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="2f9e9-115">Stile preferito</span><span class="sxs-lookup"><span data-stu-id="2f9e9-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="2f9e9-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f9e9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f9e9-117">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="2f9e9-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="2f9e9-118">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="2f9e9-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



