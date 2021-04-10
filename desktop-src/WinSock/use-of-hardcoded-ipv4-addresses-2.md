---
description: La longevità di IPv4 ha comportato la codifica hardware di molti indirizzi IPv4 noti, ad esempio gli indirizzi di loopback (127. x. x. x), le costanti integer come il loopback inaddr \_ , tra gli altri.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Utilizzo di indirizzi IPv4 hardcoded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343456"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="07cd0-103">Utilizzo di indirizzi IPv4 hardcoded</span><span class="sxs-lookup"><span data-stu-id="07cd0-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="07cd0-104">La longevità di IPv4 ha comportato la codifica hardware di molti indirizzi IPv4 noti, ad esempio gli indirizzi di loopback (127. x. x. x), le costanti integer come il loopback inaddr \_ , tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="07cd0-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="07cd0-105">La pratica della codifica hardware di questi indirizzi presenta problemi evidenti quando si modifica un'applicazione esistente per il supporto di IPv6 o la creazione di nuovi programmi indipendenti dalla versione.</span><span class="sxs-lookup"><span data-stu-id="07cd0-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="07cd0-106">Procedura consigliata</span><span class="sxs-lookup"><span data-stu-id="07cd0-106">Best Practice</span></span>

-   <span data-ttu-id="07cd0-107">L'approccio migliore consiste nell'evitare il hardcoded degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="07cd0-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="07cd0-108">Codice da evitare</span><span class="sxs-lookup"><span data-stu-id="07cd0-108">Code To Avoid</span></span>

-   <span data-ttu-id="07cd0-109">Evitare di utilizzare indirizzi hardcoded nel codice.</span><span class="sxs-lookup"><span data-stu-id="07cd0-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="07cd0-110">**Per modificare la codebase esistente da IPv4 a IPv4 e IPv6-interoperabilità**</span><span class="sxs-lookup"><span data-stu-id="07cd0-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="07cd0-111">Acquisire l'utilità *Checkv4.exe* .</span><span class="sxs-lookup"><span data-stu-id="07cd0-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="07cd0-112">L'utilità *Checkv4.exe* viene installata come parte di Microsoft Windows Software Development Kit (SDK) rilasciata per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="07cd0-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="07cd0-113">Il Windows SDK è disponibile tramite un abbonamento MSDN e può essere scaricato anche dal sito Web Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="07cd0-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="07cd0-114">Eseguire l'utilità *Checkv4.exe* sul codice.</span><span class="sxs-lookup"><span data-stu-id="07cd0-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="07cd0-115">Per informazioni su come eseguire l'utilità di *Checkv4.exe* sui file, vedere la sezione relativa all' [uso dell'utilità di Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="07cd0-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="07cd0-116">L'utilità *Checkv4.exe* segnala la presenza di definizioni comuni per gli indirizzi IPv4, ad esempio il loopback inaddr \_ .</span><span class="sxs-lookup"><span data-stu-id="07cd0-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="07cd0-117">Modificare il codice che utilizza stringhe letterali con codice indipendente dalla versione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="07cd0-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="07cd0-118">Eseguire una ricerca nella codebase per altre stringhe letterali potenziali, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="07cd0-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="07cd0-119">L'utilità *Checkv4.exe* può essere utile per trovare stringhe letterali comuni, ma potrebbero essere presenti altre specifiche per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="07cd0-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="07cd0-120">È consigliabile eseguire ricerche e test completi per assicurarsi che la codebase abbia eliminato i potenziali problemi associati alle stringhe letterali.</span><span class="sxs-lookup"><span data-stu-id="07cd0-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07cd0-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07cd0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cd0-122">Guida a IPv6 per le applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="07cd0-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="07cd0-123">Modifica delle strutture di dati per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="07cd0-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="07cd0-124">Socket dual stack per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="07cd0-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="07cd0-125">Chiamate di funzione per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="07cd0-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="07cd0-126">Problemi dell'interfaccia utente per le applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="07cd0-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="07cd0-127">Protocolli sottostanti per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="07cd0-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



