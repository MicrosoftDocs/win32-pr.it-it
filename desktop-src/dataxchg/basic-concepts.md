---
title: Concetti di base
description: In questo argomento vengono illustrati i concetti chiave relativi a Dynamic Data Exchange.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), interazione del server client
- DDE (Dynamic Data Exchange), interazione server client
- scambio di dati, Dynamic Data Exchange (DDE)
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), applicazioni client
- DDE (Dynamic Data Exchange), applicazioni client
- Dynamic Data Exchange (DDE), applicazioni server
- DDE (Dynamic Data Exchange), applicazioni server
- Dynamic Data Exchange (DDE), funzioni di callback
- DDE (Dynamic Data Exchange), funzioni di callback
- Dynamic Data Exchange (DDE), transazioni
- DDE (Dynamic Data Exchange), transazioni
- Dynamic Data Exchange (DDE), nomi di servizio
- DDE (Dynamic Data Exchange), nomi di servizio
- Dynamic Data Exchange (DDE), nomi di elementi
- DDE (Dynamic Data Exchange), nomi di elementi
- Dynamic Data Exchange (DDE), nomi degli argomenti
- DDE (Dynamic Data Exchange), nomi degli argomenti
- Dynamic Data Exchange (DDE), argomento di sistema
- DDE (Dynamic Data Exchange), argomento di sistema
- Libreria di gestione Dynamic Data Exchange (DDEML), inizializzazione
- DDEML (libreria di gestione Dynamic Data Exchange), inizializzazione
- Libreria di gestione Dynamic Data Exchange (DDEML), funzioni di callback
- DDEML (libreria di gestione Dynamic Data Exchange), funzioni di callback
- Libreria di gestione Dynamic Data Exchange (DDEML), gestione delle stringhe
- DDEML (libreria di gestione Dynamic Data Exchange), gestione delle stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727919"
---
# <a name="basic-concepts-dde"></a><span data-ttu-id="cf38f-131">Concetti di base (DDE)</span><span class="sxs-lookup"><span data-stu-id="cf38f-131">Basic Concepts (DDE)</span></span>

<span data-ttu-id="cf38f-132">Questi concetti sono chiave per comprendere Dynamic Data Exchange (DDE) e la libreria di gestione Dynamic Data Exchange (DDEML).</span><span class="sxs-lookup"><span data-stu-id="cf38f-132">These concepts are key to understanding Dynamic Data Exchange (DDE) and the Dynamic Data Exchange Management Library (DDEML).</span></span>

-   [<span data-ttu-id="cf38f-133">Interazione tra client e server</span><span class="sxs-lookup"><span data-stu-id="cf38f-133">Client and Server Interaction</span></span>](#client-and-server-interaction)
-   [<span data-ttu-id="cf38f-134">Transazioni e funzione di callback DDE</span><span class="sxs-lookup"><span data-stu-id="cf38f-134">Transactions and the DDE Callback Function</span></span>](#transactions-and-the-dde-callback-function)
-   [<span data-ttu-id="cf38f-135">Nomi di servizi, nomi di argomenti e nomi di elementi</span><span class="sxs-lookup"><span data-stu-id="cf38f-135">Service Names, Topic Names, and Item Names</span></span>](#service-names-topic-names-and-item-names)
-   [<span data-ttu-id="cf38f-136">Argomento di sistema</span><span class="sxs-lookup"><span data-stu-id="cf38f-136">System Topic</span></span>](#system-topic)
-   [<span data-ttu-id="cf38f-137">Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="cf38f-137">Initialization</span></span>](#initialization)
-   [<span data-ttu-id="cf38f-138">Funzione di callback</span><span class="sxs-lookup"><span data-stu-id="cf38f-138">Callback Function</span></span>](#callback-function)
-   [<span data-ttu-id="cf38f-139">Gestione delle stringhe</span><span class="sxs-lookup"><span data-stu-id="cf38f-139">String Management</span></span>](#string-management)
-   [<span data-ttu-id="cf38f-140">DDEML e thread</span><span class="sxs-lookup"><span data-stu-id="cf38f-140">DDEML and Threads</span></span>](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a><span data-ttu-id="cf38f-141">Interazione tra client e server</span><span class="sxs-lookup"><span data-stu-id="cf38f-141">Client and Server Interaction</span></span>

<span data-ttu-id="cf38f-142">Il DDE si verifica sempre tra un'applicazione client e un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-142">DDE always occurs between a client application and a server application.</span></span> <span data-ttu-id="cf38f-143">L' *applicazione client DDE* avvia lo scambio stabilendo una conversazione con il server per l'invio di transazioni al server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-143">The *DDE client application* initiates the exchange by establishing a conversation with the server to send transactions to the server.</span></span> <span data-ttu-id="cf38f-144">Una transazione è una richiesta di dati o servizi.</span><span class="sxs-lookup"><span data-stu-id="cf38f-144">A transaction is a request for data or services.</span></span> <span data-ttu-id="cf38f-145">L' *applicazione server DDE* risponde alle transazioni fornendo dati o servizi al client.</span><span class="sxs-lookup"><span data-stu-id="cf38f-145">The *DDE server application* responds to transactions by providing data or services to the client.</span></span> <span data-ttu-id="cf38f-146">Ad esempio, un'applicazione grafica potrebbe contenere un grafico a barre che rappresenta i profitti trimestrali di un'azienda, ma i dati per il grafico a barre potrebbero essere contenuti in un'applicazione del foglio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="cf38f-146">For example, a graphics application might contain a bar graph representing a corporation's quarterly profits, but the data for the bar graph might be contained in a spreadsheet application.</span></span> <span data-ttu-id="cf38f-147">Per ottenere le cifre di profitto più recenti, l'applicazione grafica (il client) potrebbe stabilire una conversazione con l'applicazione del foglio di calcolo (il server).</span><span class="sxs-lookup"><span data-stu-id="cf38f-147">To obtain the latest profit figures, the graphics application (the client) could establish a conversation with the spreadsheet application (the server).</span></span> <span data-ttu-id="cf38f-148">L'applicazione grafica potrebbe quindi inviare una transazione all'applicazione foglio di calcolo, richiedendo le cifre di profitto più recenti.</span><span class="sxs-lookup"><span data-stu-id="cf38f-148">The graphics application could then send a transaction to the spreadsheet application, requesting the latest profit figures.</span></span>

<span data-ttu-id="cf38f-149">Un server può avere molti client contemporaneamente e un client può richiedere dati da più server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-149">A server can have many clients at the same time, and a client can request data from multiple servers.</span></span> <span data-ttu-id="cf38f-150">Un'applicazione può essere anche un client e un server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-150">An application can also be both a client and a server.</span></span> <span data-ttu-id="cf38f-151">Il client o il server può terminare la conversazione in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="cf38f-151">Either the client or the server can terminate the conversation at any time.</span></span>

## <a name="transactions-and-the-dde-callback-function"></a><span data-ttu-id="cf38f-152">Transazioni e funzione di callback DDE</span><span class="sxs-lookup"><span data-stu-id="cf38f-152">Transactions and the DDE Callback Function</span></span>

<span data-ttu-id="cf38f-153">DDEML notifica a un'applicazione l'attività DDE che influiscono sull'applicazione inviando transazioni alla funzione di callback DDE dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-153">The DDEML notifies an application about DDE activity that affects the application by sending transactions to the application's DDE callback function.</span></span> <span data-ttu-id="cf38f-154">Una *transazione DDE* è simile a un messaggio che è una costante denominata accompagnata da altri parametri che contengono informazioni aggiuntive sulla transazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-154">A *DDE transaction* is similar to a message   it is a named constant accompanied by other parameters that contain additional information about the transaction.</span></span>

<span data-ttu-id="cf38f-155">DDEML passa una transazione a una funzione di callback DDE definita dall'applicazione che esegue un'azione appropriata per il tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-155">The DDEML passes a transaction to an application-defined DDE callback function that carries out an action appropriate to the type of transaction.</span></span> <span data-ttu-id="cf38f-156">Ad esempio, quando un'applicazione client tenta di stabilire una conversazione con un'applicazione server, il client chiama la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="cf38f-156">For example, when a client application attempts to establish a conversation with a server application, the client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span> <span data-ttu-id="cf38f-157">Questa funzione fa in modo che DDEML invii una transazione di [**\_ connessione XTYP**](xtyp-connect.md) alla funzione di callback DDE del server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-157">This function causes the DDEML to send an [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="cf38f-158">La funzione di callback può consentire la conversazione restituendo **true** a DDEML oppure può negare la conversazione restituendo **false**.</span><span class="sxs-lookup"><span data-stu-id="cf38f-158">The callback function can allow the conversation by returning **TRUE** to the DDEML, or it can deny the conversation by returning **FALSE**.</span></span> <span data-ttu-id="cf38f-159">Per una descrizione dettagliata delle transazioni, vedere [gestione delle](transaction-management.md)transazioni.</span><span class="sxs-lookup"><span data-stu-id="cf38f-159">For a detailed discussion of transactions, see [Transaction Management](transaction-management.md).</span></span>

## <a name="service-names-topic-names-and-item-names"></a><span data-ttu-id="cf38f-160">Nomi di servizi, nomi di argomenti e nomi di elementi</span><span class="sxs-lookup"><span data-stu-id="cf38f-160">Service Names, Topic Names, and Item Names</span></span>

<span data-ttu-id="cf38f-161">Un server DDE utilizza un nome di servizio della gerarchia a tre livelli (denominato "nome applicazione" nella documentazione DDE precedente), il nome dell'argomento e il nome dell'elemento per identificare in modo univoco un'unità di dati che il server può scambiare durante una conversazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-161">A DDE server uses a three-level hierarchy   service name (called "application name" in previous DDE documentation), topic name, and item name   to uniquely identify a unit of data the server can exchange during a conversation.</span></span>

<span data-ttu-id="cf38f-162">Un *nome di servizio* è una stringa a cui risponde un'applicazione server quando un client tenta di stabilire una conversazione con il server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-162">A *service name* is a string a server application responds to when a client attempts to establish a conversation with the server.</span></span> <span data-ttu-id="cf38f-163">Un client deve specificare il nome del servizio per stabilire una conversazione con il server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-163">A client must specify this service name to establish a conversation with the server.</span></span> <span data-ttu-id="cf38f-164">Sebbene un server possa rispondere a molti nomi di servizio, la maggior parte dei server risponde a un solo nome.</span><span class="sxs-lookup"><span data-stu-id="cf38f-164">Although a server can respond to many service names, most servers respond to only one name.</span></span>

<span data-ttu-id="cf38f-165">Il *nome* di un argomento è una stringa che identifica un contesto dati logico.</span><span class="sxs-lookup"><span data-stu-id="cf38f-165">A *topic name* is a string that identifies a logical data context.</span></span> <span data-ttu-id="cf38f-166">Per i server che operano su documenti basati su file, i nomi degli argomenti sono in genere nomi file; per gli altri server, si tratta di altre stringhe specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-166">For servers that operate on file-based documents, topic names are typically filenames; for other servers, they are other application-specific strings.</span></span> <span data-ttu-id="cf38f-167">Un client deve specificare un nome di argomento insieme al nome del servizio di un server durante il tentativo di stabilire una conversazione con un server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-167">A client must specify a topic name along with a server's service name when it attempts to establish a conversation with a server.</span></span>

<span data-ttu-id="cf38f-168">Il *nome* di un elemento è una stringa che identifica un'unità di dati che un server può passare a un client durante una transazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-168">An *item name* is a string that identifies a unit of data a server can pass to a client during a transaction.</span></span> <span data-ttu-id="cf38f-169">Ad esempio, un nome di elemento può identificare un numero intero, una stringa, diversi paragrafi di testo o una bitmap.</span><span class="sxs-lookup"><span data-stu-id="cf38f-169">For example, an item name might identify an integer, a string, several paragraphs of text, or a bitmap.</span></span>

<span data-ttu-id="cf38f-170">I nomi di servizio, argomento e elemento consentono al client di stabilire una conversazione con un server e di ricevere i dati dal server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-170">The service, topic, and item names enable the client to establish a conversation with a server and to receive data from the server.</span></span>

## <a name="system-topic"></a><span data-ttu-id="cf38f-171">Argomento di sistema</span><span class="sxs-lookup"><span data-stu-id="cf38f-171">System Topic</span></span>

<span data-ttu-id="cf38f-172">L'argomento System fornisce un contesto per informazioni di interesse generale per qualsiasi client DDE.</span><span class="sxs-lookup"><span data-stu-id="cf38f-172">The System topic provides a context for information of general interest to any DDE client.</span></span> <span data-ttu-id="cf38f-173">È consigliabile che le applicazioni server supportino l'argomento di sistema in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="cf38f-173">It is recommended that server applications support the System topic at all times.</span></span> <span data-ttu-id="cf38f-174">L'argomento di sistema è definito in DDEML. File di intestazione H come \_ argomento SZDDESYS.</span><span class="sxs-lookup"><span data-stu-id="cf38f-174">The System topic is defined in the DDEML.H header file as SZDDESYS\_TOPIC.</span></span>

<span data-ttu-id="cf38f-175">Per determinare quali server sono presenti e i tipi di informazioni che possono fornire, un'applicazione client può richiedere una conversazione nell'argomento del sistema all'avvio, impostando il nome del dispositivo su **null**.</span><span class="sxs-lookup"><span data-stu-id="cf38f-175">To determine which servers are present and the kinds of information they can provide, a client application can request a conversation on the System topic upon starting, setting the device name to **NULL**.</span></span> <span data-ttu-id="cf38f-176">Queste conversazioni con caratteri jolly sono costose in termini di prestazioni del sistema, pertanto devono essere conservate come minimo.</span><span class="sxs-lookup"><span data-stu-id="cf38f-176">Such wildcard conversations are costly in terms of system performance, so they should be kept to a minimum.</span></span> <span data-ttu-id="cf38f-177">Per ulteriori informazioni sull'avvio delle conversazioni DDE, vedere [gestione conversazioni](conversation-management.md).</span><span class="sxs-lookup"><span data-stu-id="cf38f-177">For more information about initiating DDE conversations, see [Conversation Management](conversation-management.md).</span></span>

<span data-ttu-id="cf38f-178">Un server deve supportare i nomi di elemento seguenti all'interno dell'argomento di sistema e di qualsiasi altro nome di elemento utile a un client.</span><span class="sxs-lookup"><span data-stu-id="cf38f-178">A server must support the following item names within the System topic and any other item names that are useful to a client.</span></span>



| <span data-ttu-id="cf38f-179">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf38f-179">Item</span></span>                     | <span data-ttu-id="cf38f-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf38f-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf38f-181">elemento SZDDE Item \_ \_</span><span class="sxs-lookup"><span data-stu-id="cf38f-181">SZDDE\_ITEM\_ITEMLIST</span></span>    | <span data-ttu-id="cf38f-182">Elenco degli elementi supportati in un argomento non di sistema.</span><span class="sxs-lookup"><span data-stu-id="cf38f-182">A list of the items supported under a non-System topic.</span></span> <span data-ttu-id="cf38f-183">(Questo elenco può variare a seconda del momento e dall'argomento all'argomento).</span><span class="sxs-lookup"><span data-stu-id="cf38f-183">(This list can vary from moment to moment and from topic to topic.)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cf38f-184">\_formati di elementi SZDDESYS \_</span><span class="sxs-lookup"><span data-stu-id="cf38f-184">SZDDESYS\_ITEM\_FORMATS</span></span>  | <span data-ttu-id="cf38f-185">Elenco di stringhe delimitate da tabulazioni che rappresentano tutti i formati degli Appunti potenzialmente supportati dall'applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="cf38f-185">A tab-delimited list of strings representing all clipboard formats potentially supported by the service application.</span></span> <span data-ttu-id="cf38f-186">Le stringhe che rappresentano formati degli appunti predefiniti sono equivalenti ai \_ valori CF con il prefisso "CF \_ " rimosso.</span><span class="sxs-lookup"><span data-stu-id="cf38f-186">Strings that represent predefined clipboard formats are equivalent to the CF\_ values with the "CF\_" prefix removed.</span></span> <span data-ttu-id="cf38f-187">Ad esempio, il \_ formato del testo CF è rappresentato dalla stringa "Text".</span><span class="sxs-lookup"><span data-stu-id="cf38f-187">For example, the CF\_TEXT format is represented by the string "TEXT".</span></span> <span data-ttu-id="cf38f-188">Queste stringhe devono essere maiuscole per identificarle ulteriormente come formati predefiniti.</span><span class="sxs-lookup"><span data-stu-id="cf38f-188">These strings must be uppercase to further identify them as predefined formats.</span></span> <span data-ttu-id="cf38f-189">L'elenco dei formati deve comparire nell'ordine di contenuto più completo per il contenuto meno ricco.</span><span class="sxs-lookup"><span data-stu-id="cf38f-189">The list of formats must appear in the order of most rich in content to least rich in content.</span></span> <span data-ttu-id="cf38f-190">Per ulteriori informazioni sui formati degli Appunti e sul rendering dei dati, vedere [Appunti](clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="cf38f-190">For more information about clipboard formats and rendering data, see [Clipboard](clipboard.md).</span></span><br/> |
| <span data-ttu-id="cf38f-191">\_Guida dell'elemento SZDDESYS \_</span><span class="sxs-lookup"><span data-stu-id="cf38f-191">SZDDESYS\_ITEM\_HELP</span></span>     | <span data-ttu-id="cf38f-192">Informazioni leggibili dall'utente di interesse generale.</span><span class="sxs-lookup"><span data-stu-id="cf38f-192">User-readable information of general interest.</span></span> <span data-ttu-id="cf38f-193">Questo elemento deve contenere almeno le informazioni su come utilizzare le funzionalità DDE dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-193">This item must contain, at a minimum, information on how to use the server application's DDE features.</span></span> <span data-ttu-id="cf38f-194">Queste informazioni possono includere, a differenza di, come specificare gli elementi all'interno degli argomenti, quali sono le stringhe di esecuzione che il server può eseguire, le transazioni poke consentite e come trovare la guida per altri elementi dell'argomento di sistema.</span><span class="sxs-lookup"><span data-stu-id="cf38f-194">This information can include, but is not limited to, how to specify items within topics, what execute strings the server can perform, what poke transactions are allowed, and how to find help on other System topic items.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="cf38f-195">\_elemento SZDDESYS \_ RTNMSG</span><span class="sxs-lookup"><span data-stu-id="cf38f-195">SZDDESYS\_ITEM\_RTNMSG</span></span>   | <span data-ttu-id="cf38f-196">Dettagli di supporto per il messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) usato più di recente.</span><span class="sxs-lookup"><span data-stu-id="cf38f-196">Supporting detail for the most recently used [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="cf38f-197">Questo elemento è utile quando sono necessari più di 8 bit di dati restituiti specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-197">This item is useful when more than 8 bits of application-specific return data are required.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf38f-198">\_stato elemento \_ SZDDESYS</span><span class="sxs-lookup"><span data-stu-id="cf38f-198">SZDDESYS\_ITEM\_STATUS</span></span>   | <span data-ttu-id="cf38f-199">Indica lo stato corrente del server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-199">An indication of the current status of the server.</span></span> <span data-ttu-id="cf38f-200">In genere, questo elemento supporta solo il \_ formato di testo CF e contiene la stringa pronta o occupata.</span><span class="sxs-lookup"><span data-stu-id="cf38f-200">Typically, this item supports only the CF\_TEXT format and contains the Ready or Busy string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cf38f-201">\_elemento SZDDESYS \_ SYSITEMS</span><span class="sxs-lookup"><span data-stu-id="cf38f-201">SZDDESYS\_ITEM\_SYSITEMS</span></span> | <span data-ttu-id="cf38f-202">Elenco degli elementi supportati nell'argomento di sistema da questo server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-202">A list of the items supported under the System topic by this server.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cf38f-203">\_argomenti sugli elementi di SZDDESYS \_</span><span class="sxs-lookup"><span data-stu-id="cf38f-203">SZDDESYS\_ITEM\_TOPICS</span></span>   | <span data-ttu-id="cf38f-204">Elenco degli argomenti supportati dal server al momento corrente.</span><span class="sxs-lookup"><span data-stu-id="cf38f-204">A list of the topics supported by the server at the current time.</span></span> <span data-ttu-id="cf38f-205">Questo elenco può variare a seconda del momento.</span><span class="sxs-lookup"><span data-stu-id="cf38f-205">(This list can vary from moment to moment.)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="cf38f-206">Questi nomi di elemento sono valori definiti in DDEML. File di intestazione H.</span><span class="sxs-lookup"><span data-stu-id="cf38f-206">These item names are values defined in the DDEML.H header file.</span></span> <span data-ttu-id="cf38f-207">Per ottenere handle di stringa per queste stringhe, un'applicazione deve usare le funzioni di gestione delle stringhe DDEML, così come per qualsiasi altra stringa in un'applicazione DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-207">To obtain string handles to these strings, an application must use the DDEML string-management functions, just as it would for any other string in a DDEML application.</span></span> <span data-ttu-id="cf38f-208">Per ulteriori informazioni sulla gestione delle stringhe, vedere [gestione delle](#string-management)stringhe.</span><span class="sxs-lookup"><span data-stu-id="cf38f-208">For more information about managing strings, see [String Management](#string-management).</span></span>

## <a name="initialization"></a><span data-ttu-id="cf38f-209">Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="cf38f-209">Initialization</span></span>

<span data-ttu-id="cf38f-210">Prima di chiamare qualsiasi altra funzione DDEML, un'applicazione deve chiamare la funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="cf38f-210">Before calling any other DDEML function, an application must call the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="cf38f-211">**DdeInitialize** ottiene un identificatore di istanza per l'applicazione, registra la funzione di callback DDE dell'applicazione con il DDE e specifica i flag di filtro delle transazioni per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="cf38f-211">**DdeInitialize** obtains an instance identifier for the application, registers the application's DDE callback function with the DDE, and specifies the transaction filter flags for the callback function.</span></span>

<span data-ttu-id="cf38f-212">Ogni istanza di un'applicazione o di una DLL deve passare il relativo identificatore di istanza come parametro *idInst* a qualsiasi altra funzione DDEML che la richiede.</span><span class="sxs-lookup"><span data-stu-id="cf38f-212">Each instance of an application or a DLL must pass its instance identifier as the *idInst* parameter to any other DDEML function that requires it.</span></span> <span data-ttu-id="cf38f-213">Lo scopo di più istanze di DDEML è supportare le dll che devono usare il DDEML nello stesso momento in cui viene usato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-213">The purpose of multiple DDEML instances is to support DLLs that must use the DDEML at the same time an application is using it.</span></span> <span data-ttu-id="cf38f-214">Un'applicazione non deve usare più di un'istanza di DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-214">An application must not use more than one instance of the DDEML.</span></span>

<span data-ttu-id="cf38f-215">I *filtri di transazione* ottimizzano le prestazioni del sistema impedendo al DDEML di passare transazioni indesiderate alla funzione di callback DDE dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-215">*Transaction filters* optimize system performance by preventing the DDEML from passing unwanted transactions to the application's DDE callback function.</span></span> <span data-ttu-id="cf38f-216">Un'applicazione imposta i filtri delle transazioni nel parametro [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd*</span><span class="sxs-lookup"><span data-stu-id="cf38f-216">An application sets the transaction filters in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* parameter.</span></span> <span data-ttu-id="cf38f-217">Un'applicazione deve specificare un flag di filtro delle transazioni per ogni tipo di transazione che non elabora nella funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="cf38f-217">An application must specify a transaction filter flag for each type of transaction that it does not process in its callback function.</span></span> <span data-ttu-id="cf38f-218">Un'applicazione può modificare i filtri delle transazioni con una chiamata successiva a **DdeInitialize**.</span><span class="sxs-lookup"><span data-stu-id="cf38f-218">An application can change its transaction filters with a subsequent call to **DdeInitialize**.</span></span> <span data-ttu-id="cf38f-219">Per ulteriori informazioni sulle transazioni, vedere [gestione delle transazioni](transaction-management.md).</span><span class="sxs-lookup"><span data-stu-id="cf38f-219">For more information about transactions, see [Transaction Management](transaction-management.md).</span></span>

<span data-ttu-id="cf38f-220">Nell'esempio seguente viene illustrato come inizializzare un'applicazione per l'utilizzo di DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-220">The following example shows how to initialize an application to use the DDEML.</span></span>


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



<span data-ttu-id="cf38f-221">Un'applicazione deve chiamare la funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) quando non USERÀ più DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-221">An application must call the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function when it is no longer going to use the DDEML.</span></span> <span data-ttu-id="cf38f-222">Questa funzione termina tutte le conversazioni attualmente aperte per l'applicazione e libera le risorse DDEML allocate dal sistema per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-222">This function terminates any conversations currently open for the application and frees the DDEML resources the system allocated for the application.</span></span>

## <a name="callback-function"></a><span data-ttu-id="cf38f-223">Funzione di callback</span><span class="sxs-lookup"><span data-stu-id="cf38f-223">Callback Function</span></span>

<span data-ttu-id="cf38f-224">Un'applicazione che utilizza DDEML deve fornire una funzione di callback che elabora gli eventi DDE che interessano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-224">An application that uses the DDEML must provide a callback function that processes the DDE events affecting the application.</span></span> <span data-ttu-id="cf38f-225">DDEML notifica a un'applicazione questi eventi inviando transazioni alla funzione di callback DDE dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-225">The DDEML notifies an application of such events by sending transactions to the application's DDE callback function.</span></span> <span data-ttu-id="cf38f-226">Le transazioni ricevute da una funzione di callback dipendono dal fatto che il filtro di callback contrassegna l'applicazione specificata in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) e se l'applicazione è un client, un server o entrambi.</span><span class="sxs-lookup"><span data-stu-id="cf38f-226">The transactions a callback function receives depend on which callback filter flags the application specified in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) and whether the application is a client, a server, or both.</span></span> <span data-ttu-id="cf38f-227">Per ulteriori informazioni, vedere [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).</span><span class="sxs-lookup"><span data-stu-id="cf38f-227">For more information, please see [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).</span></span>

<span data-ttu-id="cf38f-228">Nell'esempio seguente viene illustrata la struttura generale di una funzione di callback per una tipica applicazione client.</span><span class="sxs-lookup"><span data-stu-id="cf38f-228">The following example shows the general structure of a callback function for a typical client application.</span></span>


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



<span data-ttu-id="cf38f-229">Il parametro *uType* specifica il tipo di transazione inviato alla funzione di callback da DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-229">The *uType* parameter specifies the transaction type sent to the callback function by the DDEML.</span></span> <span data-ttu-id="cf38f-230">I valori dei parametri rimanenti dipendono dal tipo di transazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-230">The values of the remaining parameters depend on the transaction type.</span></span> <span data-ttu-id="cf38f-231">I tipi di transazione e gli eventi che li generano sono descritti negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="cf38f-231">The transaction types and the events that generate them are described in the following topics.</span></span> <span data-ttu-id="cf38f-232">Per informazioni dettagliate su ogni tipo di transazione, vedere [gestione delle transazioni](transaction-management.md).</span><span class="sxs-lookup"><span data-stu-id="cf38f-232">For detailed information about each transaction type, see [Transaction Management](transaction-management.md).</span></span>

## <a name="string-management"></a><span data-ttu-id="cf38f-233">Gestione delle stringhe</span><span class="sxs-lookup"><span data-stu-id="cf38f-233">String Management</span></span>

<span data-ttu-id="cf38f-234">Per eseguire un'attività DDE, molte funzioni DDEML richiedono l'accesso alle stringhe.</span><span class="sxs-lookup"><span data-stu-id="cf38f-234">To carry out a DDE task, many DDEML functions require access to strings.</span></span> <span data-ttu-id="cf38f-235">Un client, ad esempio, deve specificare un nome di servizio e un nome di argomento quando chiama la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) per richiedere una conversazione con un server.</span><span class="sxs-lookup"><span data-stu-id="cf38f-235">For example, a client must specify a service name and a topic name when it calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function to request a conversation with a server.</span></span> <span data-ttu-id="cf38f-236">Un'applicazione specifica una stringa passando un handle di stringa (HSZ) anziché un puntatore in una funzione DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-236">An application specifies a string by passing a string handle (HSZ) rather than a pointer in a DDEML function.</span></span> <span data-ttu-id="cf38f-237">Un *handle di stringa* è un valore **DWORD** , assegnato dal sistema, che identifica una stringa.</span><span class="sxs-lookup"><span data-stu-id="cf38f-237">A *string handle* is a **DWORD** value, assigned by the system, that identifies a string.</span></span>

<span data-ttu-id="cf38f-238">Un'applicazione può ottenere un handle di stringa per una determinata stringa chiamando la funzione [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) .</span><span class="sxs-lookup"><span data-stu-id="cf38f-238">An application can obtain a string handle to a particular string by calling the [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) function.</span></span> <span data-ttu-id="cf38f-239">Questa funzione registra la stringa con il sistema e restituisce un handle di stringa per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-239">This function registers the string with the system and returns a string handle to the application.</span></span> <span data-ttu-id="cf38f-240">L'applicazione può passare l'handle alle funzioni DDEML che devono accedere alla stringa.</span><span class="sxs-lookup"><span data-stu-id="cf38f-240">The application can pass the handle to DDEML functions that must access the string.</span></span> <span data-ttu-id="cf38f-241">Nell'esempio seguente vengono ottenuti handle di stringa per la stringa dell'argomento di sistema e la stringa del nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="cf38f-241">The following example obtains string handles to the System topic string and the service name string.</span></span>


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



<span data-ttu-id="cf38f-242">Il parametro *idInst* nell'esempio precedente specifica l'identificatore di istanza ottenuto dalla funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="cf38f-242">The *idInst* parameter in the preceding example specifies the instance identifier obtained by the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="cf38f-243">La funzione di callback DDE di un'applicazione riceve uno o più handle di stringa durante la maggior parte delle transazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="cf38f-243">An application's DDE callback function receives one or more string handles during most DDE transactions.</span></span> <span data-ttu-id="cf38f-244">Ad esempio, un server riceve due handle di stringa durante la transazione della [**\_ richiesta XTYP**](xtyp-request.md) : uno identifica una stringa che specifica un nome di argomento e l'altro identifica una stringa che specifica il nome di un elemento.</span><span class="sxs-lookup"><span data-stu-id="cf38f-244">For example, a server receives two string handles during the [**XTYP\_REQUEST**](xtyp-request.md) transaction: one identifies a string specifying a topic name, and the other identifies a string specifying an item name.</span></span> <span data-ttu-id="cf38f-245">Un'applicazione può ottenere la lunghezza della stringa che corrisponde a un handle di stringa e copiare la stringa in un buffer definito dall'applicazione chiamando la funzione [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="cf38f-245">An application can obtain the length of the string that corresponds to a string handle and copy the string to an application-defined buffer by calling the [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) function, as shown in the following example.</span></span>


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



<span data-ttu-id="cf38f-246">Non è possibile eseguire il mapping di un handle di stringa specifico dell'istanza da un handle di stringa a una stringa e viceversa.</span><span class="sxs-lookup"><span data-stu-id="cf38f-246">An instance-specific string handle cannot be mapped from string handle to string and back to string handle.</span></span> <span data-ttu-id="cf38f-247">Ad esempio, sebbene [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crei una stringa da un handle di stringa e quindi [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) crei un handle di stringa da tale stringa, i due handle non sono uguali, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="cf38f-247">For instance, although [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) creates a string from a string handle and then [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) creates a string handle from that string, the two handles are not the same, as shown in the following example.</span></span>


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



<span data-ttu-id="cf38f-248">Per confrontare i valori di due handle di stringa, usare la funzione [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .</span><span class="sxs-lookup"><span data-stu-id="cf38f-248">To compare the values of two string handles, use the [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) function.</span></span>

<span data-ttu-id="cf38f-249">Un handle di stringa passato alla funzione di callback DDE di un'applicazione diventa non valido quando la funzione di callback restituisce.</span><span class="sxs-lookup"><span data-stu-id="cf38f-249">A string handle passed to an application's DDE callback function becomes invalid when the callback function returns.</span></span> <span data-ttu-id="cf38f-250">Un'applicazione può salvare un handle di stringa da utilizzare dopo che la funzione di callback viene restituita utilizzando la funzione [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) .</span><span class="sxs-lookup"><span data-stu-id="cf38f-250">An application can save a string handle for use after the callback function returns by using the [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) function.</span></span>

<span data-ttu-id="cf38f-251">Quando un'applicazione chiama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), il sistema immette la stringa specificata in una tabella di stringhe e genera un handle che usa per accedere alla stringa.</span><span class="sxs-lookup"><span data-stu-id="cf38f-251">When an application calls [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), the system enters the specified string into a string table and generates a handle that it uses to access the string.</span></span> <span data-ttu-id="cf38f-252">Il sistema gestisce anche un conteggio di utilizzo per ogni stringa nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="cf38f-252">The system also maintains a usage count for each string in the string table.</span></span>

<span data-ttu-id="cf38f-253">Quando un'applicazione chiama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) e specifica una stringa già esistente nella tabella, il sistema incrementa il conteggio di utilizzo anziché aggiungere un'altra occorrenza della stringa.</span><span class="sxs-lookup"><span data-stu-id="cf38f-253">When an application calls [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) and specifies a string that already exists in the table, the system increments the usage count rather than adding another occurrence of the string.</span></span> <span data-ttu-id="cf38f-254">Un'applicazione può anche incrementare il conteggio di utilizzo usando [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle). Quando un'applicazione chiama la funzione [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) , il sistema decrementa il conteggio dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="cf38f-254">(An application can also increment the usage count by using [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle).) When an application calls the [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) function, the system decrements the usage count.</span></span>

<span data-ttu-id="cf38f-255">Una stringa viene rimossa dalla tabella quando il conteggio di utilizzo è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="cf38f-255">A string is removed from the table when its usage count equals zero.</span></span> <span data-ttu-id="cf38f-256">Poiché più di un'applicazione può ottenere l'handle per una determinata stringa, un'applicazione non deve liberare un handle di stringa più volte rispetto a quando ha creato o mantenuto l'handle.</span><span class="sxs-lookup"><span data-stu-id="cf38f-256">Because more than one application can obtain the handle to a particular string, an application must not free a string handle more times than it has created or retained the handle.</span></span> <span data-ttu-id="cf38f-257">In caso contrario, l'applicazione può causare la rimozione della stringa dalla tabella, negando ad altre applicazioni l'accesso alla stringa.</span><span class="sxs-lookup"><span data-stu-id="cf38f-257">Otherwise, the application can cause the string to be removed from the table, denying other applications access to the string.</span></span>

<span data-ttu-id="cf38f-258">Le funzioni di gestione delle stringhe DDEML sono basate su Atom Manager e sono soggette alle stesse restrizioni di dimensione degli atomi.</span><span class="sxs-lookup"><span data-stu-id="cf38f-258">The DDEML string-management functions are based on the atom manager and are subject to the same size restrictions as are atoms.</span></span>

## <a name="ddeml-and-threads"></a><span data-ttu-id="cf38f-259">DDEML e thread</span><span class="sxs-lookup"><span data-stu-id="cf38f-259">DDEML and Threads</span></span>

<span data-ttu-id="cf38f-260">La funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registra un'applicazione con DDEML, creando un'istanza di DDEML.</span><span class="sxs-lookup"><span data-stu-id="cf38f-260">The [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function registers an application with the DDEML, creating a DDEML instance.</span></span> <span data-ttu-id="cf38f-261">Un'istanza di DDEML è basata su thread, associata al thread che ha chiamato **DdeInitialize**.</span><span class="sxs-lookup"><span data-stu-id="cf38f-261">A DDEML instance is thread-based, associated with the thread that called **DdeInitialize**.</span></span>

<span data-ttu-id="cf38f-262">Tutte le chiamate di funzione DDEML per gli oggetti appartenenti a un'istanza di DDEML devono essere effettuate dallo stesso thread che ha chiamato [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) per creare l'istanza.</span><span class="sxs-lookup"><span data-stu-id="cf38f-262">All DDEML function calls for objects belonging to a DDEML instance must be made from the same thread that called [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) to create the instance.</span></span> <span data-ttu-id="cf38f-263">Se si chiama una funzione DDEML da un thread diverso, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cf38f-263">If you call a DDEML function from a different thread, the function will fail.</span></span> <span data-ttu-id="cf38f-264">Non è possibile accedere a una conversazione DDEML da un thread diverso da quello che ha allocato la conversazione.</span><span class="sxs-lookup"><span data-stu-id="cf38f-264">You cannot access a DDEML conversation from a thread other than the one that allocated the conversation.</span></span>

 

