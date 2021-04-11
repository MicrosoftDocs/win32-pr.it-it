---
description: Componenti peer di Windows per persone nelle vicinanze
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Componenti peer di Windows per persone nelle vicinanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967526"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="f9b64-103">Componenti peer di Windows per persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="f9b64-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="f9b64-104">All'interno del file eseguibile principale di Windows Peer Networking (P2phost.exe), l' [architettura persone nelle vicinanze](people-near-me-architecture.md) usa i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9b64-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="f9b64-105">Persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="f9b64-105">People Near Me</span></span>

<span data-ttu-id="f9b64-106">Il componente persone nelle vicinanze (persone nelle vicinanze) avvia l'individuazione tramite l'individuazione dei servizi Web nella subnet locale per i nomi utente dei computer con supporto per persone nelle vicinanze.</span><span class="sxs-lookup"><span data-stu-id="f9b64-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="f9b64-107">Publisher persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="f9b64-107">People Near Me Publisher</span></span>

<span data-ttu-id="f9b64-108">Il componente server di pubblicazione persone nelle vicinanze pubblica gli alias degli utenti connessi per indicare la disponibilità ad altri computer che usano persone nelle vicinanze sulla subnet locale.</span><span class="sxs-lookup"><span data-stu-id="f9b64-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="f9b64-109">L'utente connesso deve scegliere di pubblicare il nome alternativo prima che venga annunciato.</span><span class="sxs-lookup"><span data-stu-id="f9b64-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="f9b64-110">Il nome alternativo viene pubblicato nella subnet mediante l'individuazione dei servizi Web.</span><span class="sxs-lookup"><span data-stu-id="f9b64-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="f9b64-111">Inoltre, gli oggetti e le applicazioni possono essere pubblicati.</span><span class="sxs-lookup"><span data-stu-id="f9b64-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="f9b64-112">Tuttavia, l'utente deve specificare la pubblicazione di oggetti e applicazioni per gli ambiti '**people near me**'**o ' all'**.</span><span class="sxs-lookup"><span data-stu-id="f9b64-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="f9b64-113">Enumeratore people near me</span><span class="sxs-lookup"><span data-stu-id="f9b64-113">People Near Me Enumerator</span></span>

<span data-ttu-id="f9b64-114">Il componente enumeratore people near me enumera l'elenco di utenti nella subnet locale.</span><span class="sxs-lookup"><span data-stu-id="f9b64-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="f9b64-115">Utilizzando questo elenco, l'individuazione dei servizi Web invia una query multicast e riceve le risposte.</span><span class="sxs-lookup"><span data-stu-id="f9b64-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="f9b64-116">Una volta ottenuta l'elenco di nomi alternativi, un'applicazione può usare l'API per recuperare più dati pubblicati dall'utente (crittografato con [Schannel](windows-vista-components-for-people-near-me.md)), ad esempio l'elenco di applicazioni registrate e tutti gli oggetti da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="f9b64-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="f9b64-117">Il processo di ricerca e enumerazione non viene eseguito automaticamente, ma deve essere avviato in modo esplicito da un utente o da un'applicazione tramite l'accesso a persone nelle vicinanze.</span><span class="sxs-lookup"><span data-stu-id="f9b64-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="f9b64-118">I risultati della ricerca sono l'elenco di nomi alternativi di altri utenti nella stessa subnet che annunciano i propri soprannomi usando l'API persone nelle vicinanze.</span><span class="sxs-lookup"><span data-stu-id="f9b64-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="f9b64-119">Responsabile pubblicazione</span><span class="sxs-lookup"><span data-stu-id="f9b64-119">Publication Manager</span></span>

<span data-ttu-id="f9b64-120">Il componente responsabile della pubblicazione è responsabile della pubblicazione degli aggiornamenti della presenza, dell'applicazione o dell'oggetto a contatti o persone nelle vicinanze che hanno effettuato la sottoscrizione o eseguono il polling dei dati.</span><span class="sxs-lookup"><span data-stu-id="f9b64-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="f9b64-121">Segnalazione peer</span><span class="sxs-lookup"><span data-stu-id="f9b64-121">Peer Signaling</span></span>

<span data-ttu-id="f9b64-122">Il componente di segnalazione del peer gestisce la creazione di connessioni tra peer per scambiare dati.</span><span class="sxs-lookup"><span data-stu-id="f9b64-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="f9b64-123">Per le persone nelle vicinanze, la segnalazione del peer viene usata quando un utente o un'applicazione invia la query unicast a un computer specifico per la chiave pubblica, le applicazioni e gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="f9b64-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="f9b64-124">Gestore di invito di ricezione/UX</span><span class="sxs-lookup"><span data-stu-id="f9b64-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="f9b64-125">Il componente gestore dell'invito di ricezione/UX riceve un invito in ingresso da un altro utente, chiede all'utente di stabilire se desidera avviare l'applicazione associata all'invito e quindi avvia l'applicazione in base all'utente che accetta l'invito.</span><span class="sxs-lookup"><span data-stu-id="f9b64-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="f9b64-126">Un invito è un messaggio di un'altra persona per avviare l'attività di collaborazione usando un'applicazione specifica installata in entrambi i computer dell'utente e viene annunciata dall'utente invitato.</span><span class="sxs-lookup"><span data-stu-id="f9b64-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="f9b64-127">Sicurezza peer</span><span class="sxs-lookup"><span data-stu-id="f9b64-127">Peer Security</span></span>

<span data-ttu-id="f9b64-128">Quando la presenza, l'applicazione e l'oggetto vengono inviati, le informazioni vengono crittografate tramite un canale SSL ([Schannel](windows-vista-components-for-people-near-me.md)).</span><span class="sxs-lookup"><span data-stu-id="f9b64-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="f9b64-129">Il computer di origine utilizza la chiave pubblica del computer invitato per negoziare una chiave privata utilizzata per crittografare i dati successivi inviati tra i due peer.</span><span class="sxs-lookup"><span data-stu-id="f9b64-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



