---
description: Ogni riga contiene uno o più canali. I provider di servizi gestiscono in genere il modo in cui i canali vengono esposti come indirizzi a un'applicazione e l'utente finale o il server non richiede una conoscenza specifica dei canali.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canale (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527235"
---
# <a name="channel-telephony-api"></a><span data-ttu-id="8aca0-104">Canale (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="8aca0-104">Channel (Telephony API)</span></span>

<span data-ttu-id="8aca0-105">Ogni riga contiene uno o più canali.</span><span class="sxs-lookup"><span data-stu-id="8aca0-105">Each line has one or more channels.</span></span> <span data-ttu-id="8aca0-106">I provider di servizi gestiscono in genere il modo in cui i canali vengono esposti come indirizzi a un'applicazione e l'utente finale o il server non richiede una conoscenza specifica dei canali.</span><span class="sxs-lookup"><span data-stu-id="8aca0-106">The service providers normally handle how channels are exposed as addresses to an application, and the end user or server does not require specific knowledge of channels.</span></span>

<span data-ttu-id="8aca0-107">I canali sono identici e pertanto intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="8aca0-107">Channels are identical and therefore interchangeable.</span></span> <span data-ttu-id="8aca0-108">In POTS (servizio telefonico normale), esiste esattamente un canale su una riga e il canale viene usato esclusivamente per la voce.</span><span class="sxs-lookup"><span data-stu-id="8aca0-108">In POTS (Plain Old Telephone Service), exactly one channel exists on a line, and the channel is used exclusively for voice.</span></span> <span data-ttu-id="8aca0-109">Con ISDN è possibile che esistano almeno tre canali (e fino a 30) su una riga contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="8aca0-109">With ISDN, at least three (and as many as 30 or more) channels can exist on a line simultaneously.</span></span>

<span data-ttu-id="8aca0-110">Ogni canale può avere un proprio indirizzo, il che significa che una linea può avere il numero di indirizzi configurati per i canali.</span><span class="sxs-lookup"><span data-stu-id="8aca0-110">Each channel can have its own address, which means a line could have as many addresses as it has channels.</span></span> <span data-ttu-id="8aca0-111">La relazione precisa tra i canali e gli indirizzi esposti a un'applicazione dipende dall'implementazione di un provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="8aca0-111">The precise relationship between channels and addresses exposed to an application is dependent on a service provider's implementation.</span></span>

<span data-ttu-id="8aca0-112">Alcuni provider di servizi supportano l'assegnazione di più di un indirizzo a un singolo canale.</span><span class="sxs-lookup"><span data-stu-id="8aca0-112">Some service providers support the assignment of more than one address to a single channel.</span></span> <span data-ttu-id="8aca0-113">Nelle linee di PENTOLe sono possibili più indirizzi da parte di vari sistemi, ad esempio la composizione diretta verso l'interno (DID) o la suoneria distinta, ovvero servizi aggiuntivi forniti dall'azienda telefonica.</span><span class="sxs-lookup"><span data-stu-id="8aca0-113">On POTS lines, multiple addresses are made possible by various systems, such as direct inward dialing (DID) or distinctive ringing, which are extra-fee services that the telephone company provides.</span></span>

<span data-ttu-id="8aca0-114">Molte aziende di grandi dimensioni usano per le chiamate in ingresso.</span><span class="sxs-lookup"><span data-stu-id="8aca0-114">Many large corporations use DID for incoming calls.</span></span> <span data-ttu-id="8aca0-115">Prima che venga connessa una chiamata, il numero di estensione di destinazione viene segnalato al PBX, che fa sì che l'estensione venga squillata al posto del telefono dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="8aca0-115">Before a call is connected, its destination extension number is signaled to the PBX, which causes the extension to ring instead of the operator's phone.</span></span> <span data-ttu-id="8aca0-116">Un esempio di suoneria distinta in una casa privata è costituito dal caso in cui gli elementi padre utilizzano un indirizzo, l'altro figlio e un computer fax al terzo.</span><span class="sxs-lookup"><span data-stu-id="8aca0-116">An example of distinctive ringing in a private home would be if the parents used one address, the children another, and a fax machine a third.</span></span> <span data-ttu-id="8aca0-117">Poiché una sola linea connette la casa alla rete telefonica, tutti i telefoni squillano quando viene visualizzata una chiamata, ma lo schema circolare è diverso a seconda del numero che l'entità chiamante ha composto.</span><span class="sxs-lookup"><span data-stu-id="8aca0-117">Because only one line connects the house to the telephone network, all phones ring when a call appears, but the ring pattern is different depending on the number that the calling party dialed.</span></span> <span data-ttu-id="8aca0-118">Con la suoneria distinta, le persone sanno chi è la chiamata in ingresso e il computer fax risponde alle chiamate riconoscendo il proprio stile di suoneria.</span><span class="sxs-lookup"><span data-stu-id="8aca0-118">With distinctive ringing, the people know who the incoming call is for, and the fax machine answers its calls by recognizing its own ringing style.</span></span>

<span data-ttu-id="8aca0-119">In ISDN i diversi canali B potrebbero non avere indirizzi distinti.</span><span class="sxs-lookup"><span data-stu-id="8aca0-119">In ISDN, the various B channels might not have separate addresses.</span></span> <span data-ttu-id="8aca0-120">Poiché questi canali B potrebbero trovarsi nello stesso indirizzo, è il provider di servizi (e non l'applicazione o una persona che ha composto il numero) che assegna chiamate a questi canali.</span><span class="sxs-lookup"><span data-stu-id="8aca0-120">Because these B channels might be on the same address, it is the service provider (and not the application or a person who has dialed the number) that assigns calls to these channels.</span></span>

 

 



