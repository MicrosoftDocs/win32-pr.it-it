---
description: 'Passaggio 2: estensione di una transazione tra più componenti'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Passaggio 2: estensione di una transazione tra più componenti'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350936"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="a51d6-103">Passaggio 2: estensione di una transazione tra i componenti</span><span class="sxs-lookup"><span data-stu-id="a51d6-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="a51d6-104">Obiettivi</span><span class="sxs-lookup"><span data-stu-id="a51d6-104">Objectives</span></span>

<span data-ttu-id="a51d6-105">In questo passaggio si apprenderanno le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a51d6-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="a51d6-106">Flusso transazioni</span><span class="sxs-lookup"><span data-stu-id="a51d6-106">Transaction flow</span></span>
-   <span data-ttu-id="a51d6-107">Voto di più oggetti in una transazione</span><span class="sxs-lookup"><span data-stu-id="a51d6-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="a51d6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a51d6-108">Description</span></span>

<span data-ttu-id="a51d6-109">[Passaggio 1: la creazione di un componente transazionale](step-1--creating-a-transactional-component.md) Mostra come scrivere un semplice componente transazionale che aggiorna le informazioni sull'autore nel database Microsoft SQL Server pubs.</span><span class="sxs-lookup"><span data-stu-id="a51d6-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="a51d6-110">Il passaggio 2 Mostra cosa accade quando una transazione viene estesa tra più componenti.</span><span class="sxs-lookup"><span data-stu-id="a51d6-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="a51d6-111">In conformità con il modello di programmazione COM+, `UpdateAuthorAddress` in viene chiamato un altro componente nel corso del completamento del suo lavoro.</span><span class="sxs-lookup"><span data-stu-id="a51d6-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="a51d6-112">Il secondo componente, `ValidateAuthorAddress` , convalida l'indirizzo dell'autore e restituisce i risultati al chiamante `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="a51d6-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="a51d6-113">A differenza del chiamante, non `ValidateAuthorAddress` richiede una transazione, ma può comunque partecipare alla transazione del chiamante.</span><span class="sxs-lookup"><span data-stu-id="a51d6-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="a51d6-114">In questo passaggio, il valore dell'attributo Transaction è impostato su **supported**, come illustrato nella figura seguente, che estende la transazione esistente al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a51d6-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![Diagramma che mostra l'estensione della transazione esistente al nuovo oggetto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="a51d6-116">Il valore dell'attributo **supportato** estende (o scorre) una transazione esistente solo quando il chiamante è transazionale.</span><span class="sxs-lookup"><span data-stu-id="a51d6-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="a51d6-117">Quando `UpdateAuthorAddress` chiama `ValidateAuthorAddress` , com+ esamina prima di tutto il contesto del chiamante per verificare se è transazionale.</span><span class="sxs-lookup"><span data-stu-id="a51d6-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="a51d6-118">COM+ esamina quindi gli attributi del servizio impostati su `ValidateAuthorAddress` e assegna al nuovo oggetto lo stesso identificatore di transazione assegnato all'oggetto chiamante.</span><span class="sxs-lookup"><span data-stu-id="a51d6-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="a51d6-119">Per comprendere meglio questo processo, vedere [attivazione del contesto](context-activation.md).</span><span class="sxs-lookup"><span data-stu-id="a51d6-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="a51d6-120">Poiché condividono lo stesso identificatore di transazione, è necessario che entrambi gli oggetti completino correttamente il proprio lavoro oppure COM+ interrompa la transazione (annullando le modifiche apportate al database pubs).</span><span class="sxs-lookup"><span data-stu-id="a51d6-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="a51d6-121">Tutti gli oggetti che partecipano a una transazione votano per eseguire il commit o interrompere la transazione.</span><span class="sxs-lookup"><span data-stu-id="a51d6-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="a51d6-122">Il voto viene eseguito in modo esplicito quando si includono le istruzioni per il voto nel codice, come illustrato nell'estrazione seguente dal codice di esempio Step 1, che crea il `UpdateAuthorAddress` componente:</span><span class="sxs-lookup"><span data-stu-id="a51d6-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="a51d6-123">Il voto viene inoltre eseguito in modo implicito, come avviene nel `ValidateAuthorAddress` componente.</span><span class="sxs-lookup"><span data-stu-id="a51d6-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="a51d6-124">A meno che l'oggetto non dichiari diversamente, COM+ presuppone che un oggetto abbia completato il proprio lavoro, ma che non è pronto per essere disattivato.</span><span class="sxs-lookup"><span data-stu-id="a51d6-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="a51d6-125">COM+ fa il presupposto seguente:</span><span class="sxs-lookup"><span data-stu-id="a51d6-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="a51d6-126">Quando viene `ValidateAuthorAddress` restituito al chiamante, com+ legge il voto come commit.</span><span class="sxs-lookup"><span data-stu-id="a51d6-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="a51d6-127">COM+ non conta i voti fino a quando non disattiva l'oggetto radice, ovvero il primo oggetto nella transazione, in questo caso l' `UpdateAuthorAddress` oggetto.</span><span class="sxs-lookup"><span data-stu-id="a51d6-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="a51d6-128">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="a51d6-128">Sample code</span></span>

<span data-ttu-id="a51d6-129">Il `ValidateAuthorAddress` componente esegue una semplice verifica dell'indirizzo dell'autore.</span><span class="sxs-lookup"><span data-stu-id="a51d6-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="a51d6-130">Poiché non `UpdateAuthorAddress` vota in modo esplicito, com+ utilizza le impostazioni di voto predefinite.</span><span class="sxs-lookup"><span data-stu-id="a51d6-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="a51d6-131">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a51d6-131">Summary</span></span>

-   <span data-ttu-id="a51d6-132">L'impostazione dell'attributo Transaction di un componente su **supported** può comportare la creazione del nuovo oggetto nella transazione dell'oggetto chiamante.</span><span class="sxs-lookup"><span data-stu-id="a51d6-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="a51d6-133">COM+ esamina il contesto del chiamante per determinare lo stato transazionale del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a51d6-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="a51d6-134">Se il chiamante è transazionale, COM+ trasmette la transazione al nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a51d6-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="a51d6-135">Tutti gli oggetti che partecipano alla stessa transazione condividono un identificatore di transazione comune, che viene letto da COM+ dal contesto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a51d6-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="a51d6-136">Ogni oggetto in una transazione Vota indipendentemente da altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="a51d6-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="a51d6-137">COM+ conta i voti quando l'oggetto radice viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="a51d6-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="a51d6-138">È possibile attivare o disattivare il voto di transazione di un oggetto tra commit e Abort fino a quando COM+ disattiva l'oggetto o fino a quando COM+ non disattiva l'oggetto radice e termina la transazione.</span><span class="sxs-lookup"><span data-stu-id="a51d6-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="a51d6-139">Viene conteggiata solo l'ultima impostazione di voto.</span><span class="sxs-lookup"><span data-stu-id="a51d6-139">Only the last vote setting counts.</span></span> <span data-ttu-id="a51d6-140">Le interfacce [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) e [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) forniscono metodi e producono risultati di voto simili, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a51d6-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="a51d6-141">È possibile utilizzare una delle due interfacce per votare in modo esplicito in una transazione.</span><span class="sxs-lookup"><span data-stu-id="a51d6-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="a51d6-142">Metodi di combinazione [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="a51d6-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="a51d6-143">Metodo equivalente [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="a51d6-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="a51d6-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="a51d6-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="a51d6-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="a51d6-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="a51d6-146">**SetComplete**</span><span class="sxs-lookup"><span data-stu-id="a51d6-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="a51d6-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**</span><span class="sxs-lookup"><span data-stu-id="a51d6-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="a51d6-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="a51d6-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="a51d6-149">**EnableCommit**</span><span class="sxs-lookup"><span data-stu-id="a51d6-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="a51d6-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TXABORT**</span><span class="sxs-lookup"><span data-stu-id="a51d6-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="a51d6-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="a51d6-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="a51d6-152">**SetAbort**</span><span class="sxs-lookup"><span data-stu-id="a51d6-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="a51d6-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TXABORT**</span><span class="sxs-lookup"><span data-stu-id="a51d6-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="a51d6-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="a51d6-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="a51d6-155">**DisableCommit**</span><span class="sxs-lookup"><span data-stu-id="a51d6-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="a51d6-156">COM+ imposta il voto di un oggetto sull'equivalente di [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , a meno che il componente non voti esplicitamente.</span><span class="sxs-lookup"><span data-stu-id="a51d6-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="a51d6-157">Il voto in modo esplicito può ridurre la durata complessiva della transazione e rilasciare blocchi di risorse costosi.</span><span class="sxs-lookup"><span data-stu-id="a51d6-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a51d6-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a51d6-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a51d6-159">Passaggio 1: creazione di un componente transazionale</span><span class="sxs-lookup"><span data-stu-id="a51d6-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="a51d6-160">Passaggio 3: riutilizzo dei componenti</span><span class="sxs-lookup"><span data-stu-id="a51d6-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="a51d6-161">Attivazione del contesto</span><span class="sxs-lookup"><span data-stu-id="a51d6-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="a51d6-162">Gestione delle transazioni automatiche in COM+</span><span class="sxs-lookup"><span data-stu-id="a51d6-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




