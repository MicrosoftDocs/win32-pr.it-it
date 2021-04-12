---
title: Dettagli di implementazione EAP
description: I punti di accesso (APs), ad esempio il servizio di accesso remoto (RAS), interagiscono con le implementazioni EAP tramite l'utilizzo di chiamate di funzione che devono essere esportate dalla DLL EAP di terze parti.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337142"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="a11cd-103">Dettagli di implementazione EAP</span><span class="sxs-lookup"><span data-stu-id="a11cd-103">EAP Implementation Details</span></span>

<span data-ttu-id="a11cd-104">I punti di accesso (APs), ad esempio il servizio di accesso remoto (RAS), interagiscono con le implementazioni EAP tramite l'utilizzo di chiamate di funzione che devono essere esportate dalla DLL EAP di terze parti.</span><span class="sxs-lookup"><span data-stu-id="a11cd-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="a11cd-105">In altre parole, EAP è un'API del provider, vale a dire che i plug-in o le DLL implementano il codice per diventare un provider EAP, ma non devono chiamare le API EAP stesse.</span><span class="sxs-lookup"><span data-stu-id="a11cd-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="a11cd-106">Ad esempio, un programmatore di una DLL EAP crea codice per una routine di inizializzazione EAP e inserisce il codice nella funzione predefinita EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a11cd-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="a11cd-107">Quindi, in fase di esecuzione, la gestione connessione AP chiama la funzione **RasEapInitialize** , che contiene il codice, per inizializzare l'implementazione EAP.</span><span class="sxs-lookup"><span data-stu-id="a11cd-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="a11cd-108">Negli argomenti seguenti viene illustrata in dettaglio questa interazione:</span><span class="sxs-lookup"><span data-stu-id="a11cd-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="a11cd-109">Inizializzazione del punto di accesso di EAP</span><span class="sxs-lookup"><span data-stu-id="a11cd-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="a11cd-110">Inizializzazione del protocollo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="a11cd-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="a11cd-111">Interazione del punto di accesso e del protocollo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="a11cd-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="a11cd-112">Completamento della sessione di autenticazione</span><span class="sxs-lookup"><span data-stu-id="a11cd-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 