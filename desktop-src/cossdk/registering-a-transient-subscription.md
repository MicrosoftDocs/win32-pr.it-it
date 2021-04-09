---
description: Impossibile impostare le sottoscrizioni temporanee utilizzando lo strumento di amministrazione Servizi componenti. Per creare o aggiornare una sottoscrizione temporanea, è necessario utilizzare le interfacce amministrative COM+.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrazione di una sottoscrizione temporanea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126705"
---
# <a name="registering-a-transient-subscription"></a><span data-ttu-id="dc314-104">Registrazione di una sottoscrizione temporanea</span><span class="sxs-lookup"><span data-stu-id="dc314-104">Registering a Transient Subscription</span></span>

<span data-ttu-id="dc314-105">Le sottoscrizioni temporanee richiedono un evento per un oggetto Sottoscrittore specifico già esistente.</span><span class="sxs-lookup"><span data-stu-id="dc314-105">Transient subscriptions request an event for a specific subscriber object that already exists.</span></span> <span data-ttu-id="dc314-106">Le sottoscrizioni temporanee vengono archiviate nel catalogo COM+, ma la sottoscrizione viene eliminata se il sistema operativo o il sistema operativo viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="dc314-106">Transient subscriptions are stored in the COM+ catalog, but the subscription is deleted if the event system or operating system is stopped.</span></span> <span data-ttu-id="dc314-107">Diversamente dalle sottoscrizioni permanenti, le sottoscrizioni temporanee sono associate a un determinato oggetto e vengono archiviate solo nel sistema di eventi.</span><span class="sxs-lookup"><span data-stu-id="dc314-107">Unlike persistent subscriptions, transient subscriptions are tied to a particular object and are stored only in the event system.</span></span> <span data-ttu-id="dc314-108">Se si verifica un problema con il sistema di eventi o il sistema operativo, la sottoscrizione scompare.</span><span class="sxs-lookup"><span data-stu-id="dc314-108">If there is a problem with the event system or operating system, the subscription disappears.</span></span> <span data-ttu-id="dc314-109">Le sottoscrizioni temporanee possono essere più efficienti rispetto alle sottoscrizioni persistenti, ma è necessario gestire i cicli di vita degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="dc314-109">Transient subscriptions can be more efficient than persistent subscriptions, but you must manage their object life cycles.</span></span>

<span data-ttu-id="dc314-110">Impossibile impostare le sottoscrizioni temporanee utilizzando lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="dc314-110">Transient subscriptions cannot be set by using the Component Services administration tool.</span></span> <span data-ttu-id="dc314-111">Per creare o aggiornare una sottoscrizione temporanea, è necessario utilizzare le interfacce amministrative COM+.</span><span class="sxs-lookup"><span data-stu-id="dc314-111">You must use the COM+ administrative interfaces to create or update a transient subscription.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="dc314-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dc314-112">Visual Basic</span></span>

<span data-ttu-id="dc314-113">Nella procedura seguente viene descritto come creare una sottoscrizione temporanea utilizzando Microsoft Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dc314-113">The following procedure describes how to create a transient subscription using Microsoft Visual Basic:</span></span>

1.  <span data-ttu-id="dc314-114">Specificare una sottoscrizione come temporanea aggiungendo una nuova voce alla raccolta [**TransientSubscriptions**](transientsubscriptions.md) e impostando la proprietà SubscriberInterface sull'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) dell'oggetto Subscriber.</span><span class="sxs-lookup"><span data-stu-id="dc314-114">Specify a subscription as transient by adding a new entry to the [**TransientSubscriptions**](transientsubscriptions.md) collection and setting the SubscriberInterface property to the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface of the subscriber object.</span></span> <span data-ttu-id="dc314-115">Gli eventi COM+ non creano una nuova istanza dell'oggetto Sottoscrittore durante la generazione di un evento, ma utilizzano invece l'istanza specificata.</span><span class="sxs-lookup"><span data-stu-id="dc314-115">COM+ Events does not create a new instance of the subscriber object when firing an event but instead uses the instance you specify.</span></span> <span data-ttu-id="dc314-116">Gli eventi COM+ contengono un conteggio dei riferimenti per l'oggetto Sottoscrittore fino a quando la sottoscrizione non viene rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dc314-116">COM+ Events holds a reference count for the subscriber object until the subscription is removed from the system.</span></span>
2.  <span data-ttu-id="dc314-117">Creare un'applicazione server COM+ (un file con estensione exe, dll o ocx) con un oggetto che implementa le interfacce o i metodi a cui si desidera eseguire la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="dc314-117">Create a COM+ server application (an .exe, a .dll, or an .ocx file) with an object that implements the interfaces or methods you want to subscribe to.</span></span>
3.  <span data-ttu-id="dc314-118">Creare la sottoscrizione temporanea usando il codice seguente, passando il CLSID dell'oggetto classe di [evento](the-com--event-class-object.md) e l'istanza dell'oggetto Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="dc314-118">Create your transient subscription using the following code, by passing in the CLSID of the [event class](the-com--event-class-object.md) object and the instance of the subscriber object.</span></span> <span data-ttu-id="dc314-119">Utilizzando lo strumento di amministrazione Servizi componenti, è possibile ottenere la proprietà EventCLSID facendo clic con il pulsante destro del mouse sul componente COM+, selezionando **Proprietà** e selezionando la scheda **generale** .</span><span class="sxs-lookup"><span data-stu-id="dc314-119">Using the Component Services administrative tool, you can get the EventCLSID property by right-clicking the COM+ component, selecting **Properties**, and selecting the **General** tab.</span></span>

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

<span data-ttu-id="dc314-120">Nell'esempio seguente viene illustrato come chiamare la funzione CreateTransientSubscription per sottoscrivere un'interfaccia denominata IStockTicker, che dispone di un metodo denominato UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="dc314-120">The following example illustrates how to call the CreateTransientSubscription function to subscribe to an interface called IStockTicker, which has a method called UpdateStock.</span></span>

1.  <span data-ttu-id="dc314-121">Creare una classe di evento che supporta l'interfaccia IStockTicker, che ha un metodo, UpdateStock.</span><span class="sxs-lookup"><span data-stu-id="dc314-121">Create an event class that supports the interface IStockTicker, which has one method, UpdateStock.</span></span>
2.  <span data-ttu-id="dc314-122">Nel progetto Sottoscrittore aggiungere una classe che implementi l'interfaccia IStockTicker.</span><span class="sxs-lookup"><span data-stu-id="dc314-122">In your subscriber project, add a class that implements the IStockTicker interface.</span></span>
3.  <span data-ttu-id="dc314-123">Quando si vuole sottoscrivere, eseguire il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="dc314-123">When you want to subscribe execute the following code:</span></span>

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

<span data-ttu-id="dc314-124">La funzione CreateTransientSubscription restituisce una stringa, ovvero un GUID che può essere utilizzato come handle o cookie per revocare la sottoscrizione in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="dc314-124">The CreateTransientSubscription function returns a string, which is a GUID that can be used as a handle or a cookie to revoke the subscription later.</span></span> <span data-ttu-id="dc314-125">Per rimuovere la sottoscrizione, chiamare il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) di [**COMAdminCatalogCollection**](comadmincatalogcollection.md) sulla raccolta [**TransientSubscriptions**](transientsubscriptions.md) , passando l'indice corrispondente alla sottoscrizione con il GUID ricevuto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="dc314-125">To remove the subscription, call the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of [**COMAdminCatalogCollection**](comadmincatalogcollection.md) on the [**TransientSubscriptions**](transientsubscriptions.md) collection, passing in the index corresponding to the subscription with the GUID previously received.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc314-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc314-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc314-127">Registrazione di una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="dc314-127">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 
