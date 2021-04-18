---
description: Panoramica del modello a cascata per la classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Modello di RealTimeStylus a cascata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550372"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="1c223-103">Modello di RealTimeStylus a cascata</span><span class="sxs-lookup"><span data-stu-id="1c223-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="1c223-104">Il modello di tipo [**RealTimeStylus**](realtimestylus-class.md) a cascata consente di usare due oggetti **RealTimeStylus** , ognuno in esecuzione su un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="1c223-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="1c223-105">Con questo modello si associa un oggetto **RealTimeStylus** secondario a un oggetto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="1c223-106">L'oggetto **RealTimeStylus** secondario è associato come unico plug-in asincrono nella raccolta di plug-in asincrona dell'oggetto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="1c223-107">Il modello di [**RealTimeStylus**](realtimestylus-class.md) a cascata può essere utile negli scenari seguenti.</span><span class="sxs-lookup"><span data-stu-id="1c223-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="1c223-108">È possibile aggiungere determinate attività che possono essere richieste dal punto di vista del calcolo, pur continuando a richiedere l'accesso in tempo reale al flusso di dati della penna del tablet, ad esempio il riconoscimento dei movimenti a più tratti, alla raccolta di plug-in sincrona dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario.</span><span class="sxs-lookup"><span data-stu-id="1c223-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="1c223-109">È possibile distribuire il carico di calcolo dei plug-in sincroni su due thread, riducendo i ritardi nella raccolta di input penna in alcuni Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="1c223-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="1c223-110">Il diagramma seguente illustra il flusso dei dati della penna del Tablet PC tramite due oggetti [**RealTimeStylus**](realtimestylus-class.md) a cascata e le relative raccolte di plug-in.</span><span class="sxs-lookup"><span data-stu-id="1c223-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![illustrazione che mostra il flusso di dati RealTimeStylus a cascata](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="1c223-112">In questo diagramma il cerchio con lettera "A" rappresenta i dati della penna del tablet che sono già stati elaborati dagli oggetti [**RealTimeStylus**](realtimestylus-class.md) primari e secondari ed è stato inserito nella coda di output dell'oggetto **RealTimeStylus** secondario.</span><span class="sxs-lookup"><span data-stu-id="1c223-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="1c223-113">La lettera "B" del cerchio rappresenta i dati della penna del tablet che sono già stati elaborati dall'oggetto **RealTimeStylus** primario e aggiunti alla coda di output dell'oggetto **RealTimeStylus** primario e che non sono ancora stati inviati all'oggetto **RealTimeStylus** secondario.</span><span class="sxs-lookup"><span data-stu-id="1c223-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="1c223-114">La lettera "C" del cerchio rappresenta i dati della penna del tablet attualmente elaborati dall'oggetto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="1c223-115">Viene inviato alla raccolta di plug-in sincrono e inserito nella coda di output.</span><span class="sxs-lookup"><span data-stu-id="1c223-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="1c223-116">Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.</span><span class="sxs-lookup"><span data-stu-id="1c223-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="1c223-117">Vincoli</span><span class="sxs-lookup"><span data-stu-id="1c223-117">Constraints</span></span>

<span data-ttu-id="1c223-118">Se si usa il costruttore [**RealTimeStylus**](realtimestylus-class.md) predefinito, si crea un oggetto **RealTimeStylus** che può accettare solo input da un altro oggetto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="1c223-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="1c223-119">Nell'elenco seguente vengono descritti i vincoli associati all'utilizzo del modello [**RealTimeStylus**](realtimestylus-class.md) a cascata.</span><span class="sxs-lookup"><span data-stu-id="1c223-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="1c223-120">È possibile utilizzare solo due oggetti [**RealTimeStylus**](realtimestylus-class.md) , un oggetto **RealTimeStylus** primario e un oggetto **RealTimeStylus** secondario.</span><span class="sxs-lookup"><span data-stu-id="1c223-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="1c223-121">È necessario creare l'oggetto [**RealTimeStylus**](realtimestylus-class.md) primario con un costruttore che utilizza il parametro **attachedControl** o *handle* .</span><span class="sxs-lookup"><span data-stu-id="1c223-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="1c223-122">L'oggetto **RealTimeStylus** secondario deve essere creato con il costruttore senza argomenti.</span><span class="sxs-lookup"><span data-stu-id="1c223-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="1c223-123">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario deve essere l'unico plug-in asincrono nella raccolta di plug-in asincrona dell'oggetto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="1c223-124">Un oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario può essere associato a un solo oggetto **RealTimeStylus** primario alla volta.</span><span class="sxs-lookup"><span data-stu-id="1c223-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="1c223-125">Se viene aggiunto a un secondo oggetto **RealTimeStylus** primario, il metodo [Add](/previous-versions/ms824814(v=msdn.10)) genera un'eccezione e l'oggetto **RealTimeStylus** secondario non è associato al secondo oggetto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="1c223-126">Il comportamento di alcuni membri dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario viene modificato.</span><span class="sxs-lookup"><span data-stu-id="1c223-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="1c223-127">Nella tabella seguente viene descritto il comportamento modificato di questi membri.</span><span class="sxs-lookup"><span data-stu-id="1c223-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="1c223-128">Membro</span><span class="sxs-lookup"><span data-stu-id="1c223-128">Member</span></span></th>
    <th><span data-ttu-id="1c223-129">Comportamento</span><span class="sxs-lookup"><span data-stu-id="1c223-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="1c223-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="1c223-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="1c223-131">Questo metodo restituisce le informazioni dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="1c223-132">Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, questo metodo restituisce il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c223-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="1c223-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="1c223-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="1c223-134">Questo metodo genera un'eccezione <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="1c223-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="1c223-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span><span class="sxs-lookup"><span data-stu-id="1c223-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="1c223-136">Questo metodo restituisce le informazioni dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="1c223-137">Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, questo metodo restituisce una matrice vuota.</span><span class="sxs-lookup"><span data-stu-id="1c223-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="1c223-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span><span class="sxs-lookup"><span data-stu-id="1c223-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="1c223-139">Se si recupera questa proprietà, le informazioni vengono restituite dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="1c223-140">Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, il recupero di questa proprietà restituisce il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c223-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="1c223-141">L'impostazione di questa proprietà genera un'eccezione <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="1c223-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="1c223-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span><span class="sxs-lookup"><span data-stu-id="1c223-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="1c223-143">Se si recupera questa proprietà, le informazioni vengono restituite dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="1c223-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="1c223-144">Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, il recupero di questa proprietà restituisce il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c223-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="1c223-145">L'impostazione di questa proprietà genera un'eccezione <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="1c223-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="1c223-146">Si prevede che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) padre smetta di funzionare quando viene eliminato il metodo **RealTimeStylus** figlio.</span><span class="sxs-lookup"><span data-stu-id="1c223-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 
