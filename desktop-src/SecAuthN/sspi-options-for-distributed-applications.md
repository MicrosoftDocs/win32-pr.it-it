---
description: Opzioni SSPI per le applicazioni distribuite
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: Opzioni SSPI per le applicazioni distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878526"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="17224-103">Opzioni SSPI per le applicazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="17224-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="17224-104">Gli sviluppatori hanno molte opzioni per la creazione di applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="17224-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="17224-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) fornisce un livello di astrazione tra i protocolli a livello di applicazione e i [*protocolli di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="17224-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="17224-106">Le applicazioni possono sfruttare i protocolli di sicurezza SSPI in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="17224-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="17224-107">Chiamare le routine SSPI direttamente (per le applicazioni tradizionali basate su socket).</span><span class="sxs-lookup"><span data-stu-id="17224-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="17224-108">Le routine utilizzano i messaggi di richiesta/risposta per implementare il [*protocollo dell'applicazione*](../secgloss/a-gly.md) che contiene dati correlati alla sicurezza SSPI.</span><span class="sxs-lookup"><span data-stu-id="17224-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="17224-109">Usare COM per chiamare le opzioni di sicurezza implementate tramite la RPC autenticata e SSPI a livelli inferiori.</span><span class="sxs-lookup"><span data-stu-id="17224-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="17224-110">Queste applicazioni non chiamano direttamente le funzioni SSPI.</span><span class="sxs-lookup"><span data-stu-id="17224-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="17224-111">Usare [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) con l'interfaccia Winsock estesa per consentire ai provider di trasporto di usare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="17224-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="17224-112">Questo approccio integra il [*Security Support Provider*](../secgloss/s-gly.md) (SSP) nello stack di rete e fornisce servizi di sicurezza e trasporto tramite un'interfaccia comune.</span><span class="sxs-lookup"><span data-stu-id="17224-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="17224-113">Utilizzare l' [API Windows Internet Extensions](../wininet/portal.md) (WinInet) e un'interfaccia progettata per supportare protocolli di sicurezza Internet, ad esempio il protocollo [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL).</span><span class="sxs-lookup"><span data-stu-id="17224-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="17224-114">Le applicazioni utilizzano l'interfaccia SSPI per il provider di sicurezza del [canale sicuro](secure-channel.md) (Schannel) per implementare la sicurezza di WinInet.</span><span class="sxs-lookup"><span data-stu-id="17224-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="17224-115">Schannel è l'implementazione Microsoft di SSL.</span><span class="sxs-lookup"><span data-stu-id="17224-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="17224-116">Diverse funzioni SSPI restituiscono indicatori temporali che rappresentano la durata di diversi oggetti.</span><span class="sxs-lookup"><span data-stu-id="17224-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="17224-117">I [*pacchetti di sicurezza*](../secgloss/s-gly.md) possono mantenere l'ora e fornire timestamp in modi diversi, ma l'utilizzo dell'ora locale semplifica il lavoro di applicazioni che utilizzano funzioni SSPI.</span><span class="sxs-lookup"><span data-stu-id="17224-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 
