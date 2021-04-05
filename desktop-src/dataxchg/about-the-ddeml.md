---
title: Informazioni su DDEML
description: In questo argomento viene illustrato lo scambio dinamico di dati.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), informazioni
- DDE (Dynamic Data Exchange), informazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), informazioni
- DDEML (libreria di gestione Dynamic Data Exchange), informazioni
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516087"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="2eef1-111">Informazioni su DDEML</span><span class="sxs-lookup"><span data-stu-id="2eef1-111">About the DDEML</span></span>

<span data-ttu-id="2eef1-112">Dynamic Data Exchange (DDE) differisce dal meccanismo di trasferimento dei dati degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="2eef1-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="2eef1-113">Una differenza consiste nel fatto che gli Appunti vengono quasi sempre usati come risposta monouso a un'azione specifica da parte dell'utente, ad esempio facendo clic su **Incolla** da un menu.</span><span class="sxs-lookup"><span data-stu-id="2eef1-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="2eef1-114">Sebbene il DDE possa essere avviato anche da un utente, in genere continua senza ulteriore coinvolgimento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2eef1-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="2eef1-115">La libreria di gestione Dynamic Data Exchange (DDEML) fornisce un'interfaccia che semplifica l'attività di aggiunta della funzionalità DDE a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2eef1-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="2eef1-116">Anziché inviare, inviare ed elaborare direttamente i messaggi DDE, un'applicazione utilizza le funzioni fornite da DDEML per gestire le conversazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="2eef1-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="2eef1-117">Una conversazione DDE è l'interazione tra applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="2eef1-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="2eef1-118">Il DDEML fornisce anche un mezzo per gestire le stringhe e i dati condivisi tra le applicazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="2eef1-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="2eef1-119">Anziché utilizzare gli atomi e i puntatori agli oggetti Shared Memory, le applicazioni DDE creano e scambiano handle di stringa, che identificano le stringhe e gli handle di dati, che identificano gli oggetti DDE.</span><span class="sxs-lookup"><span data-stu-id="2eef1-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="2eef1-120">DDEML fornisce una funzione ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) che consente a un'applicazione server di registrare i nomi di servizio supportati.</span><span class="sxs-lookup"><span data-stu-id="2eef1-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="2eef1-121">I nomi dei servizi vengono quindi trasmessi ad altre applicazioni nel sistema, che usano i nomi per connettersi al server.</span><span class="sxs-lookup"><span data-stu-id="2eef1-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="2eef1-122">Il DDEML garantisce inoltre la compatibilità tra applicazioni DDE richiedendo loro di implementare il protocollo DDE in modo coerente.</span><span class="sxs-lookup"><span data-stu-id="2eef1-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="2eef1-123">Le applicazioni esistenti che utilizzano il protocollo DDE basato su messaggi sono completamente compatibili con quelle che utilizzano DDEML; ovvero, un'applicazione che utilizza un DDE basato su messaggi può stabilire conversazioni ed eseguire transazioni con le applicazioni utilizzando DDEML.</span><span class="sxs-lookup"><span data-stu-id="2eef1-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="2eef1-124">Anziché utilizzare i messaggi DDE nella nuova applicazione, sfruttare i vantaggi offerti da DDEML e dai numerosi miglioramenti offerti.</span><span class="sxs-lookup"><span data-stu-id="2eef1-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="2eef1-125">Per usare DDEML, è necessario includere il DDEML. File di intestazione H nei file di origine, collegamento con USER32. File LIB e assicurarsi che il file di DDEML.DLL si trovi nel percorso del sistema.</span><span class="sxs-lookup"><span data-stu-id="2eef1-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="2eef1-126">Ogni volta che una funzione DDEML ha esito negativo, un'applicazione può chiamare la funzione [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) per determinare la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2eef1-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="2eef1-127">**DdeGetLastError** restituisce un valore di errore che specifica la ragione dell'errore più recente.</span><span class="sxs-lookup"><span data-stu-id="2eef1-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




