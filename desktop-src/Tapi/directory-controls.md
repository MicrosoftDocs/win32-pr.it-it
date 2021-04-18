---
description: Il diagramma seguente illustra gli oggetti principali che coinvolgono i controlli directory di TAPI 3 Rendezvous. Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controlli di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307202"
---
# <a name="directory-controls"></a><span data-ttu-id="24487-104">Controlli di directory</span><span class="sxs-lookup"><span data-stu-id="24487-104">Directory Controls</span></span>

<span data-ttu-id="24487-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="24487-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="24487-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="24487-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="24487-107">Il diagramma seguente illustra gli oggetti principali che coinvolgono i controlli directory di TAPI 3 Rendezvous.</span><span class="sxs-lookup"><span data-stu-id="24487-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="24487-108">Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.</span><span class="sxs-lookup"><span data-stu-id="24487-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![interfacce e oggetti di controllo della directory Rendezvous](images/renddir.png)

<span data-ttu-id="24487-110">L'interfaccia di controllo della directory principale è [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), che deve essere creata chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="24487-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="24487-111">L'oggetto Rendezvous espone metodi per ottenere elenchi di directory disponibili e per creare nuove directory o oggetti directory.</span><span class="sxs-lookup"><span data-stu-id="24487-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="24487-112">Una directory risiede in un server ed è un elenco di oggetti directory insieme a informazioni descrittive.</span><span class="sxs-lookup"><span data-stu-id="24487-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="24487-113">I metodi associati a [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) possono ottenere informazioni associate alla directory nel suo complesso, ad esempio se si tratta di una directory ILS.</span><span class="sxs-lookup"><span data-stu-id="24487-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="24487-114">Un oggetto directory può rappresentare una conferenza o un utente.</span><span class="sxs-lookup"><span data-stu-id="24487-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="24487-115">L'interfaccia [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) fornisce metodi che consentono di recuperare o modificare informazioni generiche in un oggetto directory, ad esempio l'indirizzo di connessione remota.</span><span class="sxs-lookup"><span data-stu-id="24487-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="24487-116">Le informazioni relative a conferenze e utenti, ad esempio l'URL di una conferenza o il telefono IP primario di un utente, vengono modificate dai metodi forniti nelle interfacce [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) e [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .</span><span class="sxs-lookup"><span data-stu-id="24487-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



