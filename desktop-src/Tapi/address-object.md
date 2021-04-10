---
description: L'oggetto Address rappresenta un'entità che può effettuare o ricevere chiamate.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Oggetto Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883258"
---
# <a name="address-object"></a><span data-ttu-id="ceca7-103">Oggetto Address</span><span class="sxs-lookup"><span data-stu-id="ceca7-103">Address Object</span></span>

<span data-ttu-id="ceca7-104">L'oggetto Address rappresenta un'entità che può effettuare o ricevere chiamate.</span><span class="sxs-lookup"><span data-stu-id="ceca7-104">The Address object represents an entity that can make or receive calls.</span></span> <span data-ttu-id="ceca7-105">Questo oggetto espone interfacce e metodi che consentono a un'applicazione di eseguire una serie di operazioni, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="ceca7-105">This object exposes interfaces and methods that allow an application to perform a number of operations, such as:</span></span>

-   <span data-ttu-id="ceca7-106">Individuare se un indirizzo specificato può supportare un determinato set di requisiti del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="ceca7-106">Discover whether a specified address can support a particular set of media type needs.</span></span>
-   <span data-ttu-id="ceca7-107">Enumera le chiamate attualmente associate all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ceca7-107">Enumerate calls currently associated with the address.</span></span>
-   <span data-ttu-id="ceca7-108">Creare o inviare le chiamate.</span><span class="sxs-lookup"><span data-stu-id="ceca7-108">Create or forward calls.</span></span>
-   <span data-ttu-id="ceca7-109">Ottiene il nome del provider di servizi associato.</span><span class="sxs-lookup"><span data-stu-id="ceca7-109">Get the name of the associated service provider.</span></span>
-   <span data-ttu-id="ceca7-110">Se esiste un provider di servizi multimediali, ottenere i puntatori di interfaccia che consentono la manipolazione dettagliata del terminale.</span><span class="sxs-lookup"><span data-stu-id="ceca7-110">If a media service provider exists, get interface pointers that allow detailed terminal manipulation.</span></span>
-   <span data-ttu-id="ceca7-111">Ottenere e impostare altre informazioni, ad esempio se un messaggio è in attesa.</span><span class="sxs-lookup"><span data-stu-id="ceca7-111">Get and set other information, such as whether a message is waiting.</span></span>

<span data-ttu-id="ceca7-112">La maggior parte degli indirizzi è associata a un terminale, ma questo non è uniformemente il caso.</span><span class="sxs-lookup"><span data-stu-id="ceca7-112">Most addresses are associated with a terminal, but this is not uniformly the case.</span></span> <span data-ttu-id="ceca7-113">Ad esempio, un TSP remoto che fornisce l'accesso alle apparecchiature in un server avrà un indirizzo nel computer locale, ma non un terminale.</span><span class="sxs-lookup"><span data-stu-id="ceca7-113">For example, a remote TSP that provides access to equipment on a server will have an address on the local machine but not a terminal.</span></span> <span data-ttu-id="ceca7-114">Un modem senza voce non dispone anche di un terminale associato al relativo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ceca7-114">A speakerless modem also has no terminal associated with its address.</span></span>

<span data-ttu-id="ceca7-115">Se a un indirizzo non è associato un terminale, l'interfaccia [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) non viene esposta nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ceca7-115">If an address does not have an associated terminal, the [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) interface is not exposed on the object.</span></span>

<span data-ttu-id="ceca7-116">Nell'esempio di codice di [selezione di un indirizzo](select-an-address.md) viene illustrato il processo di base per l'acquisizione di un puntatore all'oggetto Address.</span><span class="sxs-lookup"><span data-stu-id="ceca7-116">The [Select an Address](select-an-address.md) code example shows the basic process for acquiring an address object pointer.</span></span>

<span data-ttu-id="ceca7-117">Vedere [Address Object Interfaces](address-object-interfaces.md) per un elenco di tutte le interfacce associate all'oggetto Address.</span><span class="sxs-lookup"><span data-stu-id="ceca7-117">See [Address Object Interfaces](address-object-interfaces.md) for a list of all interfaces associated with the Address object.</span></span>

 

 
