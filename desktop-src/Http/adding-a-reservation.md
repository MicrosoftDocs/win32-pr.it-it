---
title: Aggiunta di una prenotazione
description: Il database di routing contiene l'elenco delle prenotazioni.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104517200"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="145d0-103">Aggiunta di una prenotazione</span><span class="sxs-lookup"><span data-stu-id="145d0-103">Adding a Reservation</span></span>

<span data-ttu-id="145d0-104">Il database di routing contiene l'elenco delle prenotazioni.</span><span class="sxs-lookup"><span data-stu-id="145d0-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="145d0-105">L'elenco delle prenotazioni è costituito dagli utenti a cui è consentito l'accesso allo spazio dei nomi, nonché dal livello di accesso per ogni utente elencato sotto la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="145d0-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="145d0-106">Quando si aggiungono o eliminano prenotazioni, viene eseguita la ricerca del database di routing per determinare i privilegi di accesso.</span><span class="sxs-lookup"><span data-stu-id="145d0-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="145d0-107">Oltre a controllare l'ID utente, l'API server HTTP verifica anche la presenza di conflitti nelle prenotazioni esistenti prima di installare una nuova prenotazione.</span><span class="sxs-lookup"><span data-stu-id="145d0-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="145d0-108">**Per aggiungere una nuova prenotazione**</span><span class="sxs-lookup"><span data-stu-id="145d0-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="145d0-109">Se il numero di porta in UrlPrefix include prenotazioni o registrazioni per uno schema diverso dallo schema nella UrlPrefix, la registrazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="145d0-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="145d0-110">HTTP e HTTPS non possono essere supportati sulla stessa porta.</span><span class="sxs-lookup"><span data-stu-id="145d0-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="145d0-111">Individuare il bucket appropriato per la registrazione (vedere la sezione [routing delle richieste in ingresso](routing-incoming-requests.md) ), in base al tipo di host.</span><span class="sxs-lookup"><span data-stu-id="145d0-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="145d0-112">I passaggi rimanenti sono relativi a questo bucket.</span><span class="sxs-lookup"><span data-stu-id="145d0-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="145d0-113">Selezionare le voci di prenotazione con i componenti schema, host e porta che corrispondono ai UrlPrefix riservati.</span><span class="sxs-lookup"><span data-stu-id="145d0-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="145d0-114">Da questi individuare la voce con il *relativeUri* corrispondente più lungo che non è uguale a relativeUri nella prenotazione, ovvero il *nodo padre*.</span><span class="sxs-lookup"><span data-stu-id="145d0-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="145d0-115">Se la voce esiste, valutare i diritti di accesso in base all'ACL assegnato a tale voce.</span><span class="sxs-lookup"><span data-stu-id="145d0-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="145d0-116">Se non è stato trovato alcun nodo padre, si tratta di una prenotazione con una relativeUri vuota o una *prenotazione radice*.</span><span class="sxs-lookup"><span data-stu-id="145d0-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="145d0-117">Concedere i diritti di accesso solo se il chiamante viene registrato con gli account LocalSystem o Administrator.</span><span class="sxs-lookup"><span data-stu-id="145d0-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="145d0-118">Se vengono concessi i diritti di accesso, verificare la presenza di prenotazioni duplicate.</span><span class="sxs-lookup"><span data-stu-id="145d0-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="145d0-119">Se esiste una voce di prenotazione con lo stesso schema, porta, host e relativeUri, viene restituito un errore di \_ \_ codice esistente.</span><span class="sxs-lookup"><span data-stu-id="145d0-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="145d0-120">L'aggiornamento di una voce esistente deve essere eseguito in due passaggi: eliminare la voce e aggiungerne una nuova.</span><span class="sxs-lookup"><span data-stu-id="145d0-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="145d0-121">Se il passaggio precedente ha esito positivo, viene immessa una nuova voce di prenotazione nel database di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="145d0-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="145d0-122">La nuova voce viene creata con l'ACL specificato e non eredita gli ACL dalla voce *padre* .</span><span class="sxs-lookup"><span data-stu-id="145d0-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="145d0-123">Gli esempi seguenti illustrano il processo di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="145d0-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="145d0-124">Prenotazione 1: `https://+:80/vroot/subdir/` per amministratore per l'utente A e l'utente C ha esito positivo e viene immesso nel bucket "+".</span><span class="sxs-lookup"><span data-stu-id="145d0-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="145d0-125">Prenotazione 2: `https://adatum.com:80/vroot/` l'amministratore dell'utente B ha esito positivo e viene immesso nel bucket "host esplicito".</span><span class="sxs-lookup"><span data-stu-id="145d0-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="145d0-126">Prenotazione 3: l' `https://adatum.com:80/vroot/subdir/otherdir/` utente B per l'utente C ha esito positivo a causa della prenotazione 2.</span><span class="sxs-lookup"><span data-stu-id="145d0-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="145d0-127">Prenotazione 4: `https://+:80/vroot/subdir/otherdir/` l'utente a per l'utente E ha esito positivo a causa della prenotazione 1.</span><span class="sxs-lookup"><span data-stu-id="145d0-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="145d0-128">Prenotazione 5: `https://adatum.com:80/vroot/subdir/otherdir/` l'utente a per l'utente E non riesce.</span><span class="sxs-lookup"><span data-stu-id="145d0-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="145d0-129">Accesso negato a causa della prenotazione 2.</span><span class="sxs-lookup"><span data-stu-id="145d0-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="145d0-130">Prenotazione 6: `https://+:80/vroot/subdir/` l'amministratore per l'utente a ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="145d0-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="145d0-131">La prenotazione è in conflitto con la prenotazione 1.</span><span class="sxs-lookup"><span data-stu-id="145d0-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="145d0-132">Prenotazione 7: l' `https://adatum.com:80/newroot/` utente a per l'utente a ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="145d0-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="145d0-133">Accesso negato a causa della prenotazione radice implicita di `https://adatum.com:80/` per LocalSystem o Administrator.</span><span class="sxs-lookup"><span data-stu-id="145d0-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="145d0-134">Le prenotazioni possono influenzare il set di URL nelle richieste recapitate a un processo che ha precedentemente registrato un UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="145d0-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="145d0-135">Ad esempio, si consideri lo scenario seguente.</span><span class="sxs-lookup"><span data-stu-id="145d0-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="145d0-136">Registrazione: `https://adatum.com:80/vroot/` per l'applicazione 1 per l'utente a.</span><span class="sxs-lookup"><span data-stu-id="145d0-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="145d0-137">Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene recapitata all'applicazione 1.</span><span class="sxs-lookup"><span data-stu-id="145d0-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="145d0-138">Prenotazione: `https://+:80/vroot/subdir/` per l'utente B.</span><span class="sxs-lookup"><span data-stu-id="145d0-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="145d0-139">Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` è stata rifiutata.</span><span class="sxs-lookup"><span data-stu-id="145d0-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="145d0-140">Registrazione: `https://adatum.com:80/vroot/subdir/` per l'applicazione 2 per l'utente B.</span><span class="sxs-lookup"><span data-stu-id="145d0-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="145d0-141">Una richiesta per `https://adatum.com:80/vroot/subdir/file.htm` viene recapitata all'applicazione 2.</span><span class="sxs-lookup"><span data-stu-id="145d0-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 




