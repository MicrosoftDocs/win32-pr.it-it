---
description: Utilizzo di componenti non transazionali in una transazione
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Utilizzo di componenti non transazionali in una transazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748991"
---
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="96925-103">Utilizzo di componenti non transazionali in una transazione</span><span class="sxs-lookup"><span data-stu-id="96925-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="96925-104">Spesso è utile inserire componenti non transazionali in una transazione per sfruttare le [proprietà ACID](acid-properties.md) delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="96925-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="96925-105">Se, ad esempio, si dispone di componenti legacy non transazionali utilizzati per aggiornare le password in una rete, è possibile inserire tali componenti in una transazione per garantire la coerenza degli aggiornamenti delle password in rete.</span><span class="sxs-lookup"><span data-stu-id="96925-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="96925-106">L' *oggetto di contesto di transazione* è un oggetto generico che consente ai client non transazionali di combinare il lavoro di più oggetti com in un'unica transazione, senza che sia necessario sviluppare un nuovo componente specifico a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="96925-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="96925-107">A differenza di una transazione automatica, l'oggetto contesto di transazione richiede che il client Esegui il commit o l'interruzione esplicita della transazione.</span><span class="sxs-lookup"><span data-stu-id="96925-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="96925-108">Per impostazione predefinita, il valore dell'attributo Transaction dell'oggetto del contesto di transazione è impostato su Required.</span><span class="sxs-lookup"><span data-stu-id="96925-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="96925-109">COM+ interrompe la transazione se il client rilascia l'oggetto di contesto della transazione senza emettere esplicitamente una chiamata di commit o di interruzione.</span><span class="sxs-lookup"><span data-stu-id="96925-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="96925-110">Nell'esempio di Visual Basic seguente viene illustrato il modo in cui un client non transazionale può comporre il lavoro eseguito da più di un oggetto in un'unica transazione:</span><span class="sxs-lookup"><span data-stu-id="96925-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="96925-111">Limitazioni dell'oggetto del contesto di transazione</span><span class="sxs-lookup"><span data-stu-id="96925-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="96925-112">Di seguito sono riportate alcune importanti limitazioni relative all'oggetto di contesto di transazione:</span><span class="sxs-lookup"><span data-stu-id="96925-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="96925-113">Quando si utilizza un oggetto di contesto di transazione, la logica dell'applicazione che combina il lavoro di più oggetti in una singola transazione è associata a un'implementazione client non transazionale specifica e alcuni vantaggi derivanti dall'utilizzo di componenti COM andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="96925-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="96925-114">I vantaggi perduti includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="96925-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="96925-115">Possibilità di riusare la logica dell'applicazione come parte di una transazione ancora più grande</span><span class="sxs-lookup"><span data-stu-id="96925-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="96925-116">Imposizione della sicurezza dichiarativa</span><span class="sxs-lookup"><span data-stu-id="96925-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="96925-117">Flessibilità per l'esecuzione remota della logica dal client</span><span class="sxs-lookup"><span data-stu-id="96925-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="96925-118">L'oggetto del contesto di transazione viene eseguito in-process con il client non transazionale, il che significa che COM+ deve essere disponibile nel computer client non transazionale.</span><span class="sxs-lookup"><span data-stu-id="96925-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="96925-119">Questo potrebbe non essere un problema, ad esempio, quando l'oggetto di contesto di transazione viene utilizzato da una pagina di pagine ASP (Active Server) in esecuzione nello stesso server di COM+.</span><span class="sxs-lookup"><span data-stu-id="96925-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="96925-120">Non viene ottenuto un contesto per il client non transazionale quando si crea un oggetto di contesto di transazione.</span><span class="sxs-lookup"><span data-stu-id="96925-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="96925-121">Il lavoro transazionale può essere eseguito solo indirettamente, tramite oggetti COM creati utilizzando l'oggetto di contesto della transazione.</span><span class="sxs-lookup"><span data-stu-id="96925-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="96925-122">In particolare, il client non transazionale non può utilizzare i dispenser di risorse COM+ (ad esempio ODBC) e includere il lavoro nella transazione.</span><span class="sxs-lookup"><span data-stu-id="96925-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="96925-123">Ad esempio, gli sviluppatori possono avere familiarità con la sintassi seguente per eseguire il lavoro transazionale nei sistemi di database relazionali:</span><span class="sxs-lookup"><span data-stu-id="96925-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="96925-124">L'utilizzo di un oggetto di contesto di transazione in modo analogo non restituisce il risultato desiderato:</span><span class="sxs-lookup"><span data-stu-id="96925-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="96925-125">La chiamata a DoWork in questo esempio non è integrata in una transazione.</span><span class="sxs-lookup"><span data-stu-id="96925-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="96925-126">È invece necessario compilare un componente COM che chiama DoWork, creare un'istanza dell'oggetto di tale componente utilizzando l'oggetto di contesto della transazione e quindi chiamare tale oggetto dal client non transazionale affinché il lavoro faccia parte della transazione controllata dal client.</span><span class="sxs-lookup"><span data-stu-id="96925-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



