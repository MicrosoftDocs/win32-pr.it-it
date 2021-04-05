---
title: Pubblicazione con i punti di connessione del servizio
description: Lo schema Active Directory definisce una classe di oggetti serviceConnectionPoint (SCP) per semplificare la pubblicazione di dati specifici del servizio nella directory da parte di un servizio.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Pubblicazione con i punti di connessione del servizio AD
- Active Directory punti di connessione del servizio
- Active Directory punti di connessione del servizio, pubblicazione con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707576"
---
# <a name="publishing-with-service-connection-points"></a><span data-ttu-id="4fa46-106">Pubblicazione con i punti di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="4fa46-106">Publishing with Service Connection Points</span></span>

<span data-ttu-id="4fa46-107">Lo schema Active Directory definisce una classe di oggetti **serviceConnectionPoint** (SCP) per semplificare la pubblicazione di dati specifici del servizio nella directory da parte di un servizio.</span><span class="sxs-lookup"><span data-stu-id="4fa46-107">The Active Directory Schema defines a **serviceConnectionPoint** (SCP) object class to make it easy for a service to publish service-specific data in the directory.</span></span> <span data-ttu-id="4fa46-108">I client del servizio usano i dati in un SCP per individuare, connettersi e autenticare un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fa46-108">Clients of the service use the data in an SCP to locate, connect to, and authenticate an instance of your service.</span></span>

<span data-ttu-id="4fa46-109">In questa sezione viene fornita una panoramica dei punti di connessione del servizio e degli esempi di codice in cui viene illustrato come un'applicazione client/di servizio utilizza convergenza.</span><span class="sxs-lookup"><span data-stu-id="4fa46-109">This section provides an overview of service connection points and code examples that show how a client/service application uses SCPs.</span></span>

<span data-ttu-id="4fa46-110">L'esempio di codice segue questa procedura per implementare la pubblicazione del servizio con convergenza.</span><span class="sxs-lookup"><span data-stu-id="4fa46-110">The code example follows these steps to implement service publication with SCPs.</span></span>

<span data-ttu-id="4fa46-111">Per ulteriori informazioni e un esempio di codice che esegue questi passaggi, vedere [creazione di un punto di connessione del servizio](creating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="4fa46-111">For more information and a code example that performs these steps, see [Creating a Service Connection Point](creating-a-service-connection-point.md).</span></span>

<span data-ttu-id="4fa46-112">**Per creare convergenza nella directory durante l'installazione del servizio**</span><span class="sxs-lookup"><span data-stu-id="4fa46-112">**To create SCPs in the directory at service installation**</span></span>

1.  <span data-ttu-id="4fa46-113">Eseguire l'associazione all'oggetto computer per il computer host in cui è installata l'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fa46-113">Bind to the computer object for the host computer on which the service instance is installed.</span></span>
2.  <span data-ttu-id="4fa46-114">Creare un oggetto SCP come figlio dell'oggetto computer, specificando i valori iniziali per gli attributi di SCP.</span><span class="sxs-lookup"><span data-stu-id="4fa46-114">Create an SCP object as a child of the computer object, specifying the initial values for the attributes of the SCP.</span></span>
3.  <span data-ttu-id="4fa46-115">Impostare le voci di controllo di accesso (ACE) nel descrittore di sicurezza dell'oggetto SCP per consentire al servizio di modificare le proprietà SCP in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4fa46-115">Set access control entries (ACEs) in the security descriptor of the SCP object to enable the service to modify SCP properties at run time.</span></span>
4.  <span data-ttu-id="4fa46-116">Memorizzare nella cache il **objectGUID** del SCP nel registro di sistema del computer host del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fa46-116">Cache the **objectGUID** of the SCP in the registry on the service's host computer.</span></span>

<span data-ttu-id="4fa46-117">Per ulteriori informazioni e un esempio di codice che esegue questi passaggi, vedere [aggiornamento di un punto di connessione del servizio](updating-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="4fa46-117">For more information and a code example that performs these steps, see [Updating a Service Connection Point](updating-a-service-connection-point.md).</span></span>

<span data-ttu-id="4fa46-118">**Per aggiornare gli attributi SCP all'avvio del servizio**</span><span class="sxs-lookup"><span data-stu-id="4fa46-118">**To update the SCP attributes at service startup**</span></span>

1.  <span data-ttu-id="4fa46-119">Recuperare **objectGUID** dal registro di sistema e usarlo per l'associazione al SCP.</span><span class="sxs-lookup"><span data-stu-id="4fa46-119">Retrieve the **objectGUID** from the registry and use it to bind to the SCP.</span></span>
2.  <span data-ttu-id="4fa46-120">Recuperare gli attributi, ad esempio **serviceDNSName** e **SERVICEBINDINGINFORMATION**, dal SCP.</span><span class="sxs-lookup"><span data-stu-id="4fa46-120">Retrieve attributes, such as **serviceDNSName** and **serviceBindingInformation**, from the SCP.</span></span> <span data-ttu-id="4fa46-121">Confrontare questi valori con i valori correnti e aggiornare SCP se necessario.</span><span class="sxs-lookup"><span data-stu-id="4fa46-121">Compare these values to the current values and update the SCP if necessary.</span></span>

<span data-ttu-id="4fa46-122">Per ulteriori informazioni e un esempio di codice che esegue questi passaggi, vedere [modalità di individuazione e utilizzo di un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md)da parte dei client.</span><span class="sxs-lookup"><span data-stu-id="4fa46-122">For more information and a code example that performs these steps, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="4fa46-123">**Per trovare e usare un SCP da un'applicazione client**</span><span class="sxs-lookup"><span data-stu-id="4fa46-123">**To find and use an SCP by a client application**</span></span>

1.  <span data-ttu-id="4fa46-124">Eseguire l'associazione al catalogo globale e cercare gli oggetti con un attributo **Keywords** corrispondente al GUID del prodotto del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fa46-124">Bind to the Global Catalog and search for objects with a **keywords** attribute that matches the service's product GUID.</span></span> <span data-ttu-id="4fa46-125">Ogni oggetto trovato è un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fa46-125">Each object found is an instance of the service.</span></span> <span data-ttu-id="4fa46-126">Selezionare un'istanza e recuperare il nome distinto del SCP.</span><span class="sxs-lookup"><span data-stu-id="4fa46-126">Select an instance and retrieve the distinguished name of the SCP.</span></span>
2.  <span data-ttu-id="4fa46-127">Usare il nome distinto per l'associazione all'SCP.</span><span class="sxs-lookup"><span data-stu-id="4fa46-127">Use the distinguished name to bind to the SCP.</span></span>
3.  <span data-ttu-id="4fa46-128">Recuperare i valori di diversi attributi da SCP, ad esempio **serviceDNSName** e **serviceBindingInformation**.</span><span class="sxs-lookup"><span data-stu-id="4fa46-128">Retrieve the values of various attributes from the SCP, such as **serviceDNSName** and **serviceBindingInformation**.</span></span> <span data-ttu-id="4fa46-129">Usare questi valori per connettersi all'istanza del servizio e autenticarla.</span><span class="sxs-lookup"><span data-stu-id="4fa46-129">Use these values to connect to and authenticate the service instance.</span></span>

<span data-ttu-id="4fa46-130">Per ulteriori informazioni sui ruoli che possono creare e aggiornare un SCP, vedere [problemi di protezione per la pubblicazione del servizio](security-issues-for-service-publication.md).</span><span class="sxs-lookup"><span data-stu-id="4fa46-130">For more information about what roles can create and update an SCP, see [Security Issues for Service Publication](security-issues-for-service-publication.md).</span></span>

<span data-ttu-id="4fa46-131">Per ulteriori informazioni sulla creazione di un punto di connessione del [servizio, vedere la posizione in cui creare un punto di connessione del servizio](where-to-create-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="4fa46-131">For more information about where to create an SCP, see [Where to Create a Service Connection Point](where-to-create-a-service-connection-point.md).</span></span>

<span data-ttu-id="4fa46-132">Per altre informazioni sul tipo di dati da archiviare in un SCP, vedere [proprietà del punto di connessione del servizio](service-connection-point-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4fa46-132">For more information about the kind of data to store in an SCP, see [Service Connection Point Properties](service-connection-point-properties.md).</span></span>

<span data-ttu-id="4fa46-133">Per ulteriori informazioni sull'interazione tra un programma di installazione del servizio e il servizio per mantenere i dati correnti in un SCP, vedere [creazione e gestione di un punto di connessione del servizio](creating-and-maintaining-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="4fa46-133">For more information about how a service installer and the service work together to maintain current data in an SCP, see [Creating and Maintaining a Service Connection Point](creating-and-maintaining-a-service-connection-point.md).</span></span>

 

 




