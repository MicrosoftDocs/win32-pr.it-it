---
description: Il modello SSPI (Security Support Provider Interface) fornisce una singola interfaccia per un'applicazione di trasporto client/server utilizzando i vari pacchetti di sicurezza disponibili in un computer o in una rete.
ms.assetid: ffd7e531-3e0e-40c4-865e-34fa24321655
title: Procedure utilizzate con la maggior parte dei pacchetti e protocolli di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1053f21fdd085680da1e72f0acf9c7f816e788ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525854"
---
# <a name="procedures-used-with-most-security-packages-and-protocols"></a><span data-ttu-id="f0d45-103">Procedure utilizzate con la maggior parte dei pacchetti e protocolli di sicurezza</span><span class="sxs-lookup"><span data-stu-id="f0d45-103">Procedures Used with Most Security Packages and Protocols</span></span>

<span data-ttu-id="f0d45-104">Il modello SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) fornisce una singola interfaccia per un'applicazione di trasporto client/server utilizzando i vari [*pacchetti di sicurezza*](../secgloss/s-gly.md) disponibili in un computer o in una rete.</span><span class="sxs-lookup"><span data-stu-id="f0d45-104">The [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) model provides a single interface for a client/server transport application using the various [*security packages*](../secgloss/s-gly.md) available on a computer or network.</span></span> <span data-ttu-id="f0d45-105">SSPI consente a un'applicazione di utilizzare un pacchetto di sicurezza senza gestire i [*protocolli di sicurezza*](../secgloss/s-gly.md) sottostanti del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f0d45-105">SSPI allows an application to use a security package without dealing with the underlying [*security protocols*](../secgloss/s-gly.md) of the package.</span></span> <span data-ttu-id="f0d45-106">Allo stesso tempo, SSPI consente inoltre alle applicazioni sofisticate e in grado di riconoscere la sicurezza di sfruttare le funzionalità avanzate di pacchetti di sicurezza specifici.</span><span class="sxs-lookup"><span data-stu-id="f0d45-106">At the same time, SSPI also allows sophisticated, security-aware applications to take advantage of the advanced capabilities of specific security packages.</span></span>

<span data-ttu-id="f0d45-107">Le applicazioni inizializzano SSPI attenendosi alla procedura seguente per proteggere una connessione di rete per la maggior parte dei pacchetti di sicurezza:</span><span class="sxs-lookup"><span data-stu-id="f0d45-107">Applications initialize SSPI using the following steps to secure a network connection for most security packages:</span></span>

-   [<span data-ttu-id="f0d45-108">Uso di SecBufferDesc e SecBuffer</span><span class="sxs-lookup"><span data-stu-id="f0d45-108">Using SecBufferDesc and SecBuffer</span></span>](using-secbufferdesc-and-secbuffer.md)
-   [<span data-ttu-id="f0d45-109">Inizializzazione di SSPI</span><span class="sxs-lookup"><span data-stu-id="f0d45-109">Initializing SSPI</span></span>](initializing-sspi.md)
-   [<span data-ttu-id="f0d45-110">Stabilire una connessione protetta con l'autenticazione</span><span class="sxs-lookup"><span data-stu-id="f0d45-110">Establishing a Secure Connection with Authentication</span></span>](establishing-a-secure-connection-with-authentication.md)
-   [<span data-ttu-id="f0d45-111">Verifica dell'integrità della comunicazione durante lo scambio di messaggi</span><span class="sxs-lookup"><span data-stu-id="f0d45-111">Ensuring Communication Integrity During Message Exchange</span></span>](ensuring-communication-integrity-during-message-exchange.md)
-   [<span data-ttu-id="f0d45-112">Chiusura di una sessione SSPI</span><span class="sxs-lookup"><span data-stu-id="f0d45-112">Ending an SSPI Session</span></span>](ending-an-sspi-session.md)

 

 
