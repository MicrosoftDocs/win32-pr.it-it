---
description: L'operazione di parcheggio consente a un'applicazione di inviare una sessione a un indirizzo speciale in cui verrà mantenuta fino a quando non viene parcheggiato.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Park
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312714"
---
# <a name="park"></a><span data-ttu-id="46499-103">Park</span><span class="sxs-lookup"><span data-stu-id="46499-103">Park</span></span>

<span data-ttu-id="46499-104">L'operazione di parcheggio consente a un'applicazione di inviare una sessione a un indirizzo speciale in cui verrà mantenuta fino a quando non viene parcheggiato.</span><span class="sxs-lookup"><span data-stu-id="46499-104">The park operation allows an application to send a session to a special address where it will be held until unparked.</span></span> <span data-ttu-id="46499-105">Dal punto di vista dell'applicazione, questo aspetto è molto simile a quello di un trasferimento.</span><span class="sxs-lookup"><span data-stu-id="46499-105">From the point of view of the application, this looks much like a transfer.</span></span> <span data-ttu-id="46499-106">All'entità nell'altra estremità della connessione, questo aspetto è simile a quello in attesa.</span><span class="sxs-lookup"><span data-stu-id="46499-106">To the party on the other end of the connection, this resembles being put on hold.</span></span>

<span data-ttu-id="46499-107">La differenza tra Park e transfer consiste nel fatto che l'indirizzo parcheggiato non è un punto di connessione per la sessione e la sessione non avverte alcun timeout. La differenza tra Park e Holding è che una volta completata l'operazione di Park, la sessione non è più associata all'indirizzo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46499-107">The difference between park and transfer is that the parked address is not a connection point for the session, and the session does not alert or time out. The difference between park and hold is that once park operation completes, the session is no longer associated with the application's address.</span></span>

<span data-ttu-id="46499-108">Sono disponibili due forme di parcheggio per una sessione: *Park diretto* e non *diretto*.</span><span class="sxs-lookup"><span data-stu-id="46499-108">Two forms of parking a session are provided: *directed park* and *nondirected park*.</span></span> <span data-ttu-id="46499-109">In directed Call Park, l'applicazione specifica l'indirizzo di destinazione in cui deve essere parcheggiata la chiamata.</span><span class="sxs-lookup"><span data-stu-id="46499-109">In directed call park, the application specifies the destination address where the call is to be parked.</span></span> <span data-ttu-id="46499-110">Con un parcheggio non diretto, il provider di servizi o l'hardware sottostante determina l'indirizzo e lo restituisce all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46499-110">With nondirected park, the service provider or underlying hardware determines the address and returns it to the application.</span></span>

<span data-ttu-id="46499-111">Una sessione parcheggiata in genere entra nello stato inattivo dopo che è stata parcheggiata correttamente e l'applicazione deve quindi rilasciare le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="46499-111">A parked session typically enters the idle state after it has been successfully parked, and the application should then release the resources associated with it.</span></span> <span data-ttu-id="46499-112">Per un riepilogo su come eseguire questa operazione, vedere [terminare una sessione](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="46499-112">See [Terminate a Session](terminate-a-session-ovr.md) for a summary of how to do this.</span></span>

<span data-ttu-id="46499-113">Se l'applicazione Sblocca la sessione, vengono allocate nuove risorse della sessione anche se l'applicazione ha restituito i puntatori precedenti, pertanto l'esito negativo delle versioni appropriate può causare diversi problemi.</span><span class="sxs-lookup"><span data-stu-id="46499-113">If the application unparks the session, new session resources are allocated even if the application has returned the previous pointers, so failure to do proper releases can result in a variety of problems.</span></span>

<span data-ttu-id="46499-114">Alcuni provider di servizi possono ricordare all'utente che una sessione è stata parcheggiata per un lungo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="46499-114">Some service providers can remind the user after a session has been parked for some long amount of time.</span></span> <span data-ttu-id="46499-115">L'applicazione visualizza una chiamata a un'offerta con un [motivo](reason-ovr.md) della chiamata impostato su promemoria.</span><span class="sxs-lookup"><span data-stu-id="46499-115">The application sees an offering call with a call [reason](reason-ovr.md) set to reminder.</span></span>

<span data-ttu-id="46499-116">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="46499-116">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="46499-117">**TAPI 2. x:** Vedere [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span><span class="sxs-lookup"><span data-stu-id="46499-117">**TAPI 2.x:** See [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span></span>

<span data-ttu-id="46499-118">**TAPI 3:** Vedere [**ITBasicCallControl::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span><span class="sxs-lookup"><span data-stu-id="46499-118">**TAPI 3:** See [**ITBasicCallControl::ParkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::ParkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span></span>

 

 
