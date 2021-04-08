---
description: Quando un pacchetto di sicurezza SSP/AP funziona come pacchetto di autenticazione, viene caricato nello spazio di processo dell'autorità di protezione locale (LSA) e viene definito in modalità LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Modalità LSA rispetto alla modalità utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058036"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="701d6-103">Modalità LSA rispetto alla modalità utente</span><span class="sxs-lookup"><span data-stu-id="701d6-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="701d6-104">Quando un pacchetto di [*sicurezza*](../secgloss/s-gly.md) SSP/AP funziona come [*pacchetto di autenticazione*](../secgloss/a-gly.md), viene caricato nello spazio di processo dell'autorità di [*protezione locale*](../secgloss/l-gly.md) (LSA) e viene definito in modalità LSA.</span><span class="sxs-lookup"><span data-stu-id="701d6-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="701d6-105">Le applicazioni di accesso accedono alla funzionalità del pacchetto di autenticazione tramite le [funzioni di accesso LSA](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="701d6-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="701d6-106">Gli sviluppatori possono utilizzare le funzioni di supporto LSA disponibili solo per i pacchetti di sicurezza in modalità LSA per implementare pacchetti di autenticazione più sofisticati rispetto a quelli precedentemente supportati.</span><span class="sxs-lookup"><span data-stu-id="701d6-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="701d6-107">Quando un [*pacchetto di sicurezza*](../secgloss/s-gly.md) fornisce servizi di sicurezza a un'applicazione client/server, viene caricato nei processi client e server e viene definito in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="701d6-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="701d6-108">Le applicazioni client/server accedono ai servizi di supporto per la sicurezza del pacchetto di sicurezza tramite Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span><span class="sxs-lookup"><span data-stu-id="701d6-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="701d6-109">Il supporto LSA per SSP/APs include funzioni che possono essere utilizzate dalle istanze in modalità LSA e in modalità utente di un pacchetto di sicurezza per la comunicazione.</span><span class="sxs-lookup"><span data-stu-id="701d6-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="701d6-110">Inoltre, l'istanza in modalità utente di un pacchetto di sicurezza può delegare le richieste selezionate per le informazioni all'istanza in modalità LSA del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="701d6-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="701d6-111">Per informazioni dettagliate sull'inizializzazione dei pacchetti di sicurezza per ogni modalità, vedere [inizializzazione in modalità LSA](lsa-mode-initialization.md) e [inizializzazione in modalità utente](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="701d6-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
