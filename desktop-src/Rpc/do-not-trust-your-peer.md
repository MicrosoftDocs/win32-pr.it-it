---
title: Non considerare attendibile il peer
description: '\ 0034; non considerare attendibile il peer \ 0034; è una regola di sicurezza di base, ma è spesso trascurata.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709964"
---
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="7f87b-103">Non considerare attendibile il peer</span><span class="sxs-lookup"><span data-stu-id="7f87b-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="7f87b-104">"Non considerare attendibile il peer" è una regola di sicurezza di base, ma è spesso trascurata.</span><span class="sxs-lookup"><span data-stu-id="7f87b-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="7f87b-105">Non presupporre che l'altra parte di una comunicazione si comporterà correttamente e non presupporre che il peer superi i dati previsti.</span><span class="sxs-lookup"><span data-stu-id="7f87b-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="7f87b-106">MIDL e RPC eseguono alcuni controlli per conto dell'utente, ma non tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="7f87b-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="7f87b-107">Conoscere l'aspetto dei parametri che viene verificato da MIDL o RPC e quali aspetti è necessario verificare autonomamente.</span><span class="sxs-lookup"><span data-stu-id="7f87b-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="7f87b-108">Per gli handle di contesto in/out, ad esempio, RPC verifica che l'handle del contesto non sia un valore non null non valido.</span><span class="sxs-lookup"><span data-stu-id="7f87b-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="7f87b-109">Consente valori null e valori validi, ma molti sviluppatori non sono consapevoli del fatto che i valori null sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="7f87b-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="7f87b-110">Si tratta di un elemento da controllare.</span><span class="sxs-lookup"><span data-stu-id="7f87b-110">This is something to check for.</span></span>

<span data-ttu-id="7f87b-111">Anche se in genere si considera attendibile il peer, assicurarsi di non introdurre nuovi percorsi in base ai quali un computer compromesso o un account principale può attaccare altri computer.</span><span class="sxs-lookup"><span data-stu-id="7f87b-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="7f87b-112">Si supponga che un utente scelga il suo compleanno come password ed è indovinato da un utente malintenzionato.</span><span class="sxs-lookup"><span data-stu-id="7f87b-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="7f87b-113">Anche dopo l'autenticazione delle richieste provenienti dall'utente e l'accesso ai relativi dati, assicurarsi che non esistano vulnerabilità sfruttabili, ad esempio sovraccarichi dello stack che possono consentire a un utente malintenzionato di assumere il controllo del server ed estendere la violazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7f87b-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




