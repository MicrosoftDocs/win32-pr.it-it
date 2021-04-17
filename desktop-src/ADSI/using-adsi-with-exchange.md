---
title: Uso di ADSI con Exchange
description: Per Exchange 2000, le informazioni per l'utilizzo di ADSI con Exchange sono contenute in Exchange 2000 SDK. Per ulteriori informazioni, vedere attività di gestione per ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI per Exchange ADSI
- ADSI per Exchange ADSI, cassette postali
- ADSI per Exchange ADSI, cassette postali, creazione
- ADSI per Exchange ADSI, cassette postali, eliminazione
- ADSI per Exchange ADSI, cassette postali, impostazione del descrittore di sicurezza in
- ADSI per Exchange ADSI, cassette postali, ricerca del server Home per
- ADSI per Exchange ADSI, recupero e modifica dei messaggi
- ADSI per Exchange ADSI, descrittori di sicurezza
- ADSI per Exchange ADSI, descrittori di sicurezza, manipolazione
- ADSI per Exchange ADSI, descrittori di sicurezza, impostazione
- ADSI per Exchange ADSI, contenitore dei destinatari
- ADSI per Exchange ADSI, visualizzazione delle proprietà degli oggetti Exchange
- ADSI per Exchange ADSI, contenitore dei destinatari, personalizzato
- ADSI per Exchange ADSI, Exchange Server
- ADSI per Exchange ADSI, Exchange Server, visualizzazione e modifica dello schema
- ADSI per Exchange ADSI, Exchange Server, elenco versione server
- ADSI per Exchange ADSI, Exchange Server, organizzazione e nome sito
- ADSI per Exchange ADSI, Exchange Server, ricerca del server principale della cassetta postale
- ADSI per Exchange ADSI, indirizzi di posta elettronica, recupero
- ADSI per Exchange ADSI, elenchi di distribuzione, creazione
- ADSI per Exchange ADSI, elementi nascosti o eliminati
- ADSI per Exchange ADSI, recupero delle modifiche al servizio directory
- ADSI per Exchange ADSI, dimensioni del messaggio
- ADSI per Exchange ADSI, risoluzione dei problemi
- ADSI delle cassette postali
- cassette postali ADSI, creazione
- cassette postali ADSI, eliminazione
- cassette postali ADSI, impostazione del descrittore di sicurezza
- cassette postali ADSI, ricerca del server Home per
- messaggi ADSI, recupero e modifica
- ADSI di Exchange
- Exchange ADSI, cassette postali
- Exchange ADSI, cassette postali, creazione
- Exchange ADSI, cassette postali, eliminazione
- Exchange ADSI, cassette postali, impostazione del descrittore di sicurezza in
- Exchange ADSI, cassette postali, ricerca del server principale per
- Exchange ADSI, recupero e modifica dei messaggi
- Exchange ADSI, descrittori di sicurezza
- Exchange ADSI, descrittori di sicurezza, manipolazione
- Exchange ADSI, descrittori di sicurezza, impostazione
- Exchange ADSI, contenitore destinatari
- Exchange ADSI, visualizzazione delle proprietà degli oggetti Exchange
- Exchange ADSI, contenitore destinatari, personalizzato
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, visualizzazione e modifica dello schema
- Exchange ADSI, Exchange Server, elenco versione server
- Exchange ADSI, Exchange Server, organizzazione e nome sito
- Exchange ADSI, Exchange Server, ricerca del server principale della cassetta postale
- Exchange ADSI, indirizzi di posta elettronica, recupero
- Exchange ADSI, liste di distribuzione, creazione
- Exchange ADSI, hidden o Deleted entry
- Exchange ADSI, recupero delle modifiche al servizio directory
- ADSI di Exchange, dimensioni del messaggio
- Exchange ADSI, risoluzione dei problemi
- descrittori di sicurezza ADSI, per oggetti Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300433"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="b0da1-159">Uso di ADSI con Exchange</span><span class="sxs-lookup"><span data-stu-id="b0da1-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="b0da1-160">Per Exchange 2000, le informazioni per l'utilizzo di ADSI con Exchange sono contenute in Exchange 2000 SDK.</span><span class="sxs-lookup"><span data-stu-id="b0da1-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="b0da1-161">Per ulteriori informazioni, vedere [attività di gestione per ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="b0da1-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="b0da1-162">In questa sezione sono disponibili le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0da1-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="b0da1-163">Creazione di un URL utente</span><span class="sxs-lookup"><span data-stu-id="b0da1-163">Creating a user URL</span></span>
-   <span data-ttu-id="b0da1-164">Compilazione di percorsi di Active Directory</span><span class="sxs-lookup"><span data-stu-id="b0da1-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="b0da1-165">Enumerazione dei server Exchange 2000 con ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="b0da1-166">Manipolazione degli attributi di estensione con ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="b0da1-167">Aggiunta o rimozione di un oggetto Manager con ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="b0da1-168">Enumerazione delle proprietà degli oggetti di Exchange con ADSI/ADO</span><span class="sxs-lookup"><span data-stu-id="b0da1-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="b0da1-169">Recupero di un nome distinto Exchange legacy con ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="b0da1-170">Individuazione del nome dell'organizzazione di Exchange tramite ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="b0da1-171">Individuazione degli elenchi di indirizzi di Exchange con ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="b0da1-172">Creazione di una lista di distribuzione con CDOEX e ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="b0da1-173">Impostazione della restrizione Message su un server virtuale SMTP tramite ADSI</span><span class="sxs-lookup"><span data-stu-id="b0da1-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="b0da1-174">Per Exchange 5,5, il riferimento ADSI e le informazioni using sono reperibili nella Guida di [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) .</span><span class="sxs-lookup"><span data-stu-id="b0da1-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="b0da1-175">In questa sezione sono disponibili le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0da1-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="b0da1-176">Visualizzazione e modifica dello schema di Exchange Server</span><span class="sxs-lookup"><span data-stu-id="b0da1-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="b0da1-177">Visualizzazione delle proprietà non elaborate di un oggetto Exchange</span><span class="sxs-lookup"><span data-stu-id="b0da1-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="b0da1-178">Creazione di una cassetta postale di Exchange</span><span class="sxs-lookup"><span data-stu-id="b0da1-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="b0da1-179">Impostazione del descrittore di sicurezza in una cassetta postale di Exchange</span><span class="sxs-lookup"><span data-stu-id="b0da1-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="b0da1-180">Modifica di descrittori di sicurezza e SID</span><span class="sxs-lookup"><span data-stu-id="b0da1-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="b0da1-181">Eliminazione di un oggetto cassetta postale</span><span class="sxs-lookup"><span data-stu-id="b0da1-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="b0da1-182">Creazione di un destinatario personalizzato</span><span class="sxs-lookup"><span data-stu-id="b0da1-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="b0da1-183">Creazione di un contenitore di destinatari</span><span class="sxs-lookup"><span data-stu-id="b0da1-183">Creating a recipients container</span></span>
-   <span data-ttu-id="b0da1-184">Recupero del nome dell'organizzazione e del sito da un server</span><span class="sxs-lookup"><span data-stu-id="b0da1-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="b0da1-185">Elenco della versione di tutti i server di Exchange Server nell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="b0da1-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="b0da1-186">Individuazione del server principale di una cassetta postale</span><span class="sxs-lookup"><span data-stu-id="b0da1-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="b0da1-187">Recupero degli indirizzi di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="b0da1-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="b0da1-188">Accesso a voci nascoste o eliminate</span><span class="sxs-lookup"><span data-stu-id="b0da1-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="b0da1-189">Recupero delle modifiche apportate al servizio directory</span><span class="sxs-lookup"><span data-stu-id="b0da1-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="b0da1-190">Creazione di una lista di distribuzione dai risultati di una query</span><span class="sxs-lookup"><span data-stu-id="b0da1-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="b0da1-191">Recupero o modifica delle dimensioni del messaggio</span><span class="sxs-lookup"><span data-stu-id="b0da1-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="b0da1-192">Utilizzo di codici di errore LDAP per la risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="b0da1-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 