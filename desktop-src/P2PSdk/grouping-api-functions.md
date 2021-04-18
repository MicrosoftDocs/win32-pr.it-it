---
description: "L'API di raggruppamento usa le funzioni seguenti:"
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Raggruppamento di funzioni API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312273"
---
# <a name="grouping-api-functions"></a><span data-ttu-id="46f0d-103">Raggruppamento di funzioni API</span><span class="sxs-lookup"><span data-stu-id="46f0d-103">Grouping API Functions</span></span>

<span data-ttu-id="46f0d-104">L'API di raggruppamento usa le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="46f0d-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="46f0d-105">Funzioni di inizializzazione e pulizia del gruppo</span><span class="sxs-lookup"><span data-stu-id="46f0d-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="46f0d-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-106">Function</span></span>                                       | <span data-ttu-id="46f0d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-108">**PeerGroupShutdown**</span><span class="sxs-lookup"><span data-stu-id="46f0d-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="46f0d-109">Chiude un gruppo peer creato con [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) ed Elimina tutte le risorse allocate.</span><span class="sxs-lookup"><span data-stu-id="46f0d-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="46f0d-110">**PeerGroupStartup**</span><span class="sxs-lookup"><span data-stu-id="46f0d-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="46f0d-111">Avvia un gruppo peer utilizzando una versione richiesta dell'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="46f0d-112">Funzioni di creazione e accesso del gruppo</span><span class="sxs-lookup"><span data-stu-id="46f0d-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="46f0d-113">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-113">Function</span></span>                                                                       | <span data-ttu-id="46f0d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-115">**PeerGroupClose**</span><span class="sxs-lookup"><span data-stu-id="46f0d-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="46f0d-116">Invalida l'handle del gruppo peer ottenuto da una chiamata precedente alla funzione [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .</span><span class="sxs-lookup"><span data-stu-id="46f0d-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="46f0d-117">**PeerGroupConnect**</span><span class="sxs-lookup"><span data-stu-id="46f0d-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="46f0d-118">Avvia una ricerca PNRP per un gruppo peer e tenta di connettersi a tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="46f0d-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="46f0d-119">Quando questa funzione viene chiamata correttamente, un peer può comunicare con altri membri del gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="46f0d-120">**PeerGroupConnectByAddress**</span><span class="sxs-lookup"><span data-stu-id="46f0d-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="46f0d-121">Tenta di connettersi al gruppo peer a cui partecipano altri peer con indirizzi IPv6 noti.</span><span class="sxs-lookup"><span data-stu-id="46f0d-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="46f0d-122">**PeerGroupCreate**</span><span class="sxs-lookup"><span data-stu-id="46f0d-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="46f0d-123">Consente di creare un nuovo gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="46f0d-124">**PeerGroupCreateInvitation**</span><span class="sxs-lookup"><span data-stu-id="46f0d-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="46f0d-125">Restituisce una stringa XML che può essere utilizzata dal peer specificato per partecipare a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="46f0d-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="46f0d-126">**PeerGroupCreatePasswordInvitation**</span><span class="sxs-lookup"><span data-stu-id="46f0d-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="46f0d-127">Restituisce una stringa XML che può essere utilizzata dal peer specificato per unire in join un gruppo con una password corrispondente.</span><span class="sxs-lookup"><span data-stu-id="46f0d-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="46f0d-128">**PeerGroupDelete**</span><span class="sxs-lookup"><span data-stu-id="46f0d-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="46f0d-129">Elimina i dati locali e il certificato associato a un gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="46f0d-130">**PeerGroupGetStatus**</span><span class="sxs-lookup"><span data-stu-id="46f0d-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="46f0d-131">Recupera lo stato corrente di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="46f0d-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="46f0d-132">**PeerGroupIssueCredentials**</span><span class="sxs-lookup"><span data-stu-id="46f0d-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="46f0d-133">Rilascia le credenziali, incluso un GMC, a un'identità specifica e, facoltativamente, restituisce una stringa XML di invito che il peer invitato può utilizzare per aggiungere un gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="46f0d-134">**PeerGroupJoin**</span><span class="sxs-lookup"><span data-stu-id="46f0d-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="46f0d-135">Consente a un peer con invito a partecipare a un gruppo peer esistente.</span><span class="sxs-lookup"><span data-stu-id="46f0d-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="46f0d-136">**PeerGroupOpen**</span><span class="sxs-lookup"><span data-stu-id="46f0d-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="46f0d-137">Apre un gruppo peer creato o aggiunto da un peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="46f0d-138">**PeerGroupParseInvitation**</span><span class="sxs-lookup"><span data-stu-id="46f0d-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="46f0d-139">Restituisce una struttura di [**\_ \_ informazioni di invito peer**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) con i dettagli di un invito specifico.</span><span class="sxs-lookup"><span data-stu-id="46f0d-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="46f0d-140">**PeerGroupPasswordJoin**</span><span class="sxs-lookup"><span data-stu-id="46f0d-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="46f0d-141">Consente a un peer con un invito e la password corretta di partecipare a un gruppo peer protetto da password.</span><span class="sxs-lookup"><span data-stu-id="46f0d-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="46f0d-142">Funzioni di informazioni sui membri e sui gruppi</span><span class="sxs-lookup"><span data-stu-id="46f0d-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="46f0d-143">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-143">Function</span></span>                                                 | <span data-ttu-id="46f0d-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-145">**PeerGroupEnumMembers**</span><span class="sxs-lookup"><span data-stu-id="46f0d-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="46f0d-146">Crea un'enumerazione dei membri del gruppo peer disponibili e le informazioni di appartenenza associate.</span><span class="sxs-lookup"><span data-stu-id="46f0d-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="46f0d-147">**PeerGroupGetProperties**</span><span class="sxs-lookup"><span data-stu-id="46f0d-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="46f0d-148">Recupera le informazioni sulle proprietà di un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="46f0d-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="46f0d-149">**PeerGroupSetProperties**</span><span class="sxs-lookup"><span data-stu-id="46f0d-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="46f0d-150">Imposta le proprietà del gruppo peer corrente.</span><span class="sxs-lookup"><span data-stu-id="46f0d-150">Sets the current peer group properties.</span></span> <span data-ttu-id="46f0d-151">Nella versione 1,0 di questa API, solo l'autore del gruppo peer può eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="46f0d-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="46f0d-152">Record e funzioni di gestione dei record</span><span class="sxs-lookup"><span data-stu-id="46f0d-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="46f0d-153">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-153">Function</span></span>                                                 | <span data-ttu-id="46f0d-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-155">**PeerGroupAddRecord**</span><span class="sxs-lookup"><span data-stu-id="46f0d-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="46f0d-156">Aggiunge un nuovo record al gruppo peer, che viene propagato a tutti i peer partecipanti.</span><span class="sxs-lookup"><span data-stu-id="46f0d-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="46f0d-157">**PeerGroupDeleteRecord**</span><span class="sxs-lookup"><span data-stu-id="46f0d-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="46f0d-158">Elimina un record da un gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="46f0d-159">Solo l'autore di un record può eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="46f0d-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="46f0d-160">**PeerGroupEnumRecords**</span><span class="sxs-lookup"><span data-stu-id="46f0d-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="46f0d-161">Crea un'enumerazione di record di gruppi di peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="46f0d-162">**PeerGroupGetRecord**</span><span class="sxs-lookup"><span data-stu-id="46f0d-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="46f0d-163">Recupera un record di gruppo specifico.</span><span class="sxs-lookup"><span data-stu-id="46f0d-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="46f0d-164">**PeerGroupSearchRecords**</span><span class="sxs-lookup"><span data-stu-id="46f0d-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="46f0d-165">Esegue una ricerca nel database del gruppo peer locale per i record che corrispondono ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="46f0d-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="46f0d-166">**PeerGroupUpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="46f0d-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="46f0d-167">Aggiorna un record in un gruppo peer specifico.</span><span class="sxs-lookup"><span data-stu-id="46f0d-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="46f0d-168">Funzioni di importazione/esportazione di database di gruppo</span><span class="sxs-lookup"><span data-stu-id="46f0d-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="46f0d-169">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-169">Function</span></span>                                                   | <span data-ttu-id="46f0d-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-171">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="46f0d-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="46f0d-172">Esporta un database del gruppo peer in un file specifico, che può essere trasportato in un altro computer e importato con la funzione [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) .</span><span class="sxs-lookup"><span data-stu-id="46f0d-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="46f0d-173">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="46f0d-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="46f0d-174">Importa un database del gruppo peer da un file locale.</span><span class="sxs-lookup"><span data-stu-id="46f0d-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="46f0d-175">Funzioni di connessione diretta</span><span class="sxs-lookup"><span data-stu-id="46f0d-175">Direct Connection Functions</span></span>



| <span data-ttu-id="46f0d-176">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-176">Function</span></span>                                                                 | <span data-ttu-id="46f0d-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-178">**PeerGroupCloseDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="46f0d-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="46f0d-179">Chiude una connessione diretta specifica tra due peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="46f0d-180">**PeerGroupEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="46f0d-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="46f0d-181">Crea un'enumerazione delle connessioni attualmente attive nel peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="46f0d-182">**PeerGroupOpenDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="46f0d-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="46f0d-183">Stabilisce una connessione diretta con un altro peer in un gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="46f0d-184">**PeerGroupSendData**</span><span class="sxs-lookup"><span data-stu-id="46f0d-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="46f0d-185">Invia dati a un membro tramite una connessione diretta o adiacente.</span><span class="sxs-lookup"><span data-stu-id="46f0d-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="46f0d-186">Infrastruttura degli eventi di gruppo</span><span class="sxs-lookup"><span data-stu-id="46f0d-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="46f0d-187">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-187">Function</span></span>                                                     | <span data-ttu-id="46f0d-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-189">**PeerGroupGetEventData**</span><span class="sxs-lookup"><span data-stu-id="46f0d-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="46f0d-190">Consente a un'applicazione di recuperare i dati restituiti da un evento di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="46f0d-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="46f0d-191">**PeerGroupRegisterEvent**</span><span class="sxs-lookup"><span data-stu-id="46f0d-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="46f0d-192">Registra un peer per eventi specifici del gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="46f0d-193">**PeerGroupUnregisterEvent**</span><span class="sxs-lookup"><span data-stu-id="46f0d-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="46f0d-194">Annulla la registrazione di un peer dalla notifica degli eventi peer associati all'handle di evento fornito.</span><span class="sxs-lookup"><span data-stu-id="46f0d-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="46f0d-195">Funzioni di conversione dell'ora del gruppo</span><span class="sxs-lookup"><span data-stu-id="46f0d-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="46f0d-196">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-196">Function</span></span>                                                                     | <span data-ttu-id="46f0d-197">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-198">**PeerGroupPeerTimeToUniversalTime**</span><span class="sxs-lookup"><span data-stu-id="46f0d-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="46f0d-199">Converte il valore dell'ora di riferimento gestito dal gruppo peer in un valore di ora localizzato appropriato per la visualizzazione in un computer peer.</span><span class="sxs-lookup"><span data-stu-id="46f0d-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="46f0d-200">**PeerGroupUniversalTimeToPeerTime**</span><span class="sxs-lookup"><span data-stu-id="46f0d-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="46f0d-201">Converte un valore dell'ora locale dal computer di un peer a un valore di ora del gruppo peer comune.</span><span class="sxs-lookup"><span data-stu-id="46f0d-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="46f0d-202">Funzioni di configurazione del gruppo</span><span class="sxs-lookup"><span data-stu-id="46f0d-202">Group Configuration Functions</span></span>



| <span data-ttu-id="46f0d-203">Funzione</span><span class="sxs-lookup"><span data-stu-id="46f0d-203">Function</span></span>                                               | <span data-ttu-id="46f0d-204">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46f0d-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46f0d-205">**PeerGroupExportConfig**</span><span class="sxs-lookup"><span data-stu-id="46f0d-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="46f0d-206">Esporta la configurazione di gruppo per un peer come stringa XML che contiene l'identità, il nome del gruppo e il GMC per l'identità.</span><span class="sxs-lookup"><span data-stu-id="46f0d-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="46f0d-207">**PeerGroupImportConfig**</span><span class="sxs-lookup"><span data-stu-id="46f0d-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="46f0d-208">Importa una configurazione del gruppo peer per un'identità in base alle impostazioni specifiche in una stringa di configurazione XML specificata.</span><span class="sxs-lookup"><span data-stu-id="46f0d-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



