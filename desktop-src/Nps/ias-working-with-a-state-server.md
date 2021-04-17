---
title: Utilizzo di un server di stato
description: NPS esegue l'autenticazione usando un database configurato nel sito del server NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299923"
---
# <a name="working-with-a-state-server"></a><span data-ttu-id="1ad80-103">Utilizzo di un server di stato</span><span class="sxs-lookup"><span data-stu-id="1ad80-103">Working With a State Server</span></span>

> [!Note]  
> <span data-ttu-id="1ad80-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1ad80-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1ad80-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="1ad80-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1ad80-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="1ad80-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1ad80-107">NPS esegue l'autenticazione usando un database configurato nel sito del server NPS.</span><span class="sxs-lookup"><span data-stu-id="1ad80-107">NPS performs authentication using a database that is configured at the NPS server site.</span></span> <span data-ttu-id="1ad80-108">Questo database di autenticazione può essere il database utente per un dominio di Windows oppure può attingere alle informazioni utente ottenute dalla Active Directory di Windows.</span><span class="sxs-lookup"><span data-stu-id="1ad80-108">This authentication database could be the user database for a Windows Domain or it could draw upon the user information obtained from the Windows Active Directory.</span></span> <span data-ttu-id="1ad80-109">Il diagramma seguente illustra una configurazione tipica che mostra il modo in cui NPS interagisce con i database di autenticazione, ad esempio un database utente di dominio di Windows o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ad80-109">The following diagram illustrates a typical configuration that shows how NPS interacts with authentication databases such as a Windows Domain user database or Active Directory.</span></span> <span data-ttu-id="1ad80-110">Nel diagramma viene inoltre illustrato il modo in cui NPS può interagire con un server di stato fornito da terze parti.</span><span class="sxs-lookup"><span data-stu-id="1ad80-110">The diagram also shows how NPS could interact with a state server that is provided by a third party.</span></span> <span data-ttu-id="1ad80-111">Lo scopo principale di un server di stato è limitare il numero di sessioni di accesso simultanee che possono essere eseguite da un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="1ad80-111">The primary purpose of a state server is to limit the number of simultaneous logon sessions a single user can run.</span></span>

![NPS che interagisce con il server di stato e i database di autenticazione](images/ias02.png)

<span data-ttu-id="1ad80-113">Esistono due punti di interazione tra NPS e il server di stato.</span><span class="sxs-lookup"><span data-stu-id="1ad80-113">There are two points of interaction between NPS and the state server.</span></span> <span data-ttu-id="1ad80-114">Una delle interazioni si verifica quando NPS riceve una richiesta di autenticazione dal server NAS.</span><span class="sxs-lookup"><span data-stu-id="1ad80-114">One interaction takes place when NPS receives an authentication request from the NAS.</span></span> <span data-ttu-id="1ad80-115">Il server di stato fornisce informazioni dal database per determinare se accettare o rifiutare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="1ad80-115">The state server provides information from its database to determine whether to accept or deny the request.</span></span> <span data-ttu-id="1ad80-116">L'altra interazione si verifica quando NPS riceve le richieste di Accounting dal server NAS.</span><span class="sxs-lookup"><span data-stu-id="1ad80-116">The other interaction takes place when NPS receives accounting requests from the NAS.</span></span> <span data-ttu-id="1ad80-117">Il server di stato utilizza le informazioni contenute in queste richieste di contabilità per aggiornare il relativo database.</span><span class="sxs-lookup"><span data-stu-id="1ad80-117">The state server uses the information form these accounting requests to update its database.</span></span>

<span data-ttu-id="1ad80-118">Per ulteriori informazioni sui server di stato, vedere:</span><span class="sxs-lookup"><span data-stu-id="1ad80-118">For more information on state servers see:</span></span>

-   [<span data-ttu-id="1ad80-119">Considerazioni sulla progettazione del server di stato</span><span class="sxs-lookup"><span data-stu-id="1ad80-119">State Server Design Considerations</span></span>](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a><span data-ttu-id="1ad80-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ad80-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad80-121">Servizio di autenticazione Internet e server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="1ad80-121">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="1ad80-122">Autenticazione, autorizzazione e accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="1ad80-122">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="1ad80-123">Registrazione con server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="1ad80-123">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 