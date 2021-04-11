---
description: Lo scopo del wrapper fornitore è incapsulare e utilizzare le interfacce COM di basso livello (fornite dai produttori di smart card) per una particolare smart card. Queste interfacce non vengono fornite da Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Provider di servizi wrapper fornitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128906"
---
# <a name="vendor-wrapper-service-provider"></a><span data-ttu-id="3a9fb-104">Provider di servizi wrapper fornitore</span><span class="sxs-lookup"><span data-stu-id="3a9fb-104">Vendor Wrapper Service Provider</span></span>

<span data-ttu-id="3a9fb-105">Lo scopo del wrapper fornitore è incapsulare e utilizzare le interfacce COM di basso livello (fornite dai produttori di smart card) per una particolare smart card.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-105">The purpose of the vendor wrapper is to encapsulate and use the low-level COM interfaces (supplied by the smart card manufacturers) for a particular smart card.</span></span> <span data-ttu-id="3a9fb-106">Queste interfacce non vengono fornite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-106">These interfaces are not supplied by Microsoft.</span></span>

![wrapper fornitore](images/scspart1.png)

<span data-ttu-id="3a9fb-108">Come descritto nella parte 6 della *specifica di interoperabilità per i sistemi ICCS e personal computer* (vedere le specifiche all'indirizzo [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ), la funzionalità esposta da questo wrapper è più semplice da usare rispetto alla funzionalità di quattro provider di servizi distinti.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-108">As described in part 6 of the *Interoperability Specification for ICCs and Personal Computer Systems* (see specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)), the functionality exposed by this wrapper is easier to use than the functionality of four separate service providers.</span></span> <span data-ttu-id="3a9fb-109">Le funzionalità del wrapper possono essere divise in quattro aree principali:</span><span class="sxs-lookup"><span data-stu-id="3a9fb-109">The wrapper's functionality can be divided into four main areas:</span></span>

-   <span data-ttu-id="3a9fb-110">Servizi di autenticazione con smart card, ad esempio richiedere l'autenticazione della carta e della richiesta.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-110">Smart card authentication services, such as get challenge and card authentication.</span></span>
-   <span data-ttu-id="3a9fb-111">Accesso ai file di smart card o file system servizi, ad esempio apertura, chiusura, lettura e scrittura.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-111">Smart card file access or file system services, such as open, close, read, and write.</span></span>
-   <span data-ttu-id="3a9fb-112">Gestione delle smart card, ad esempio collegamento e scollegamento.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-112">Smart card management, such as attach and detach.</span></span>
-   <span data-ttu-id="3a9fb-113">Servizi di verifica della smart card, ad esempio la verifica e la modifica del codice.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-113">Smart card verification services, such as verify and change code.</span></span>

> [!Note]  
> <span data-ttu-id="3a9fb-114">Questa specifica potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-114">This specification may not be available in some languages and countries or regions.</span></span>

 

<span data-ttu-id="3a9fb-115">La funzionalità è specifica per il tipo di scheda usato (le funzioni supportate dalla scheda, i protocolli e così via) e saranno diverse per ogni scheda.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-115">The functionality is specific to the type of card being used (which functions the card supports, protocols, and so on) and will be different for each card.</span></span>

<span data-ttu-id="3a9fb-116">Il wrapper di esempio Microsoft SCardCOM utilizza la libreria COM ATL per implementare un wrapper semplice e il layout di un modello per altri wrapper.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-116">The Microsoft SCardCOM example wrapper uses the ATL COM library to implement a simple wrapper and lay down a template for other wrappers.</span></span> <span data-ttu-id="3a9fb-117">Implementa le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-117">It implements the following interfaces.</span></span>



| <span data-ttu-id="3a9fb-118">Interfaccia o oggetto</span><span class="sxs-lookup"><span data-stu-id="3a9fb-118">Interface or object</span></span>                                     | <span data-ttu-id="3a9fb-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a9fb-119">Description</span></span>                         |
|---------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="3a9fb-120">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="3a9fb-120">**ISCardAuth**</span></span>](iscardauth.md)<br/>             | <span data-ttu-id="3a9fb-121">Servizi di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-121">Authentication services.</span></span><br/> |
| [<span data-ttu-id="3a9fb-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="3a9fb-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md)<br/> | <span data-ttu-id="3a9fb-123">Servizi del file System.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-123">File system services.</span></span><br/>    |
| [<span data-ttu-id="3a9fb-124">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="3a9fb-124">**ISCardManage**</span></span>](iscardmanage.md)<br/>         | <span data-ttu-id="3a9fb-125">Servizi di gestione.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-125">Management services.</span></span><br/>     |
| [<span data-ttu-id="3a9fb-126">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="3a9fb-126">**ISCardVerify**</span></span>](iscardverify.md)<br/>         | <span data-ttu-id="3a9fb-127">Servizi di verifica.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-127">Verification services.</span></span><br/>   |



 

> [!Note]  
> <span data-ttu-id="3a9fb-128">L'esempio SCardCOM viene fornito solo come esempio di implementazione delle interfacce wrapper.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-128">The SCardCOM example is provided only as an example of implementing the wrapper interfaces.</span></span> <span data-ttu-id="3a9fb-129">Per evitare conflitti tra i nomi di DLL e altri fornitori, non è necessario usare SCardCOM.dll come nome di qualsiasi DLL creata.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-129">To prevent DLL name collision with other vendors, you must not use SCardCOM.dll as the name of any DLLs you create.</span></span>

 

<span data-ttu-id="3a9fb-130">Di seguito è riportato un tipico utilizzo del wrapper fornitore.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-130">Following is a typical use of the vendor wrapper.</span></span> <span data-ttu-id="3a9fb-131">In questo esempio viene utilizzata l'interfaccia [**ISCardManage**](iscardmanage.md) per creare istanze delle interfacce che verranno incapsulate nel provider di servizi e nell'interfaccia [**ISCardVerify**](iscardverify.md) per verificarne il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-131">This example uses the [**ISCardManage**](iscardmanage.md) interface to create instances of the interfaces that will be wrapped into the service provider and the [**ISCardVerify**](iscardverify.md) interface to verify their operation.</span></span>

<span data-ttu-id="3a9fb-132">**Per compilare un provider di servizi wrapper**</span><span class="sxs-lookup"><span data-stu-id="3a9fb-132">**To build a wrapper service provider**</span></span>

1.  <span data-ttu-id="3a9fb-133">Creare un'istanza dell'interfaccia [**ISCardManage**](iscardmanage.md) .</span><span class="sxs-lookup"><span data-stu-id="3a9fb-133">Create an instance of the [**ISCardManage**](iscardmanage.md) interface.</span></span> <span data-ttu-id="3a9fb-134">Usare questa interfaccia per creare un'istanza di interfacce obbligatorie (ad esempio, [**ISCardFileAccess**](iscardfileaccess.md) o [**ISCardVerify**](iscardverify.md)).</span><span class="sxs-lookup"><span data-stu-id="3a9fb-134">Use this interface to create an instance of required interfaces (for example, [**ISCardFileAccess**](iscardfileaccess.md) or [**ISCardVerify**](iscardverify.md)).</span></span> <span data-ttu-id="3a9fb-135">Quando si creano queste interfacce, verranno create anche le interfacce COM di basso livello corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-135">When creating these interfaces, any corresponding low-level COM interfaces would also be created.</span></span>
2.  <span data-ttu-id="3a9fb-136">Collegare/connettersi a una scheda tramite il metodo [**ISCardManage**](iscardmanage.md) appropriato.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-136">Attach/connect to a card through the appropriate [**ISCardManage**](iscardmanage.md) method.</span></span>
3.  <span data-ttu-id="3a9fb-137">Eseguire le operazioni necessarie tramite il metodo [**ISCardVerify**](iscardverify.md) appropriato, che può chiamare più metodi e interfacce com di basso livello per il completamento.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-137">Perform required operations through the appropriate [**ISCardVerify**](iscardverify.md) method (which may call multiple low-level COM interfaces and methods to complete).</span></span>
4.  <span data-ttu-id="3a9fb-138">Ripetere l'operazione per altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-138">Repeat for other operations.</span></span>
5.  <span data-ttu-id="3a9fb-139">Rilasciare al termine.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-139">Release when complete.</span></span>

<span data-ttu-id="3a9fb-140">Il nome dell'interfaccia COM e l'identificatore di interfaccia (GUID) non devono essere modificati rispetto a quelli usati nel codice o nel wrapper di esempio.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-140">The COM interface name and interface identifier (GUID) should not change from those used in the code or example wrapper.</span></span> <span data-ttu-id="3a9fb-141">Tuttavia, il GUID della classe (ovvero, in cui risiede un'implementazione effettiva di un'interfaccia) deve essere modificato da quelli utilizzati.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-141">However, the class GUID (that is, where an actual implementation of an interface resides) must be changed from those used.</span></span> <span data-ttu-id="3a9fb-142">Questa operazione è particolarmente importante quando si implementa un wrapper fornitore.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-142">This is especially important when implementing a vendor wrapper.</span></span> <span data-ttu-id="3a9fb-143">Un esempio potrebbe essere l'utilizzo di più wrapper fornitore in un particolare computer.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-143">One example would be using multiple vendor wrappers on a particular computer.</span></span> <span data-ttu-id="3a9fb-144">Questi wrapper devono implementare le stesse interfacce COM, ma utilizzeranno sempre strategie di implementazione diverse.</span><span class="sxs-lookup"><span data-stu-id="3a9fb-144">These wrappers should implement the same COM interfaces, but will always use different implementation strategies.</span></span> <span data-ttu-id="3a9fb-145">Sono pertanto necessarie classi diverse (e ID di classe).</span><span class="sxs-lookup"><span data-stu-id="3a9fb-145">Therefore, different classes (and class IDs) are required.</span></span>

 

 




