---
description: 'Passaggio 3: riutilizzo dei componenti'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Passaggio 3: riutilizzo dei componenti'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566930"
---
# <a name="step-3-reusing-components"></a><span data-ttu-id="fc2e8-103">Passaggio 3: riutilizzo dei componenti</span><span class="sxs-lookup"><span data-stu-id="fc2e8-103">Step 3: Reusing Components</span></span>

## <a name="objectives"></a><span data-ttu-id="fc2e8-104">Obiettivi</span><span class="sxs-lookup"><span data-stu-id="fc2e8-104">Objectives</span></span>

<span data-ttu-id="fc2e8-105">In questo passaggio si apprenderanno le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc2e8-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="fc2e8-106">Componenti riutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-106">Reusable components.</span></span>
-   <span data-ttu-id="fc2e8-107">Come pianificare la riusabilità.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-107">How to plan for reusability.</span></span>

## <a name="description"></a><span data-ttu-id="fc2e8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc2e8-108">Description</span></span>

<span data-ttu-id="fc2e8-109">Due parti precedenti di questo nozioni di base sui servizi COM+, [passaggio 1: creazione di un componente transazionale](step-1--creating-a-transactional-component.md) e [passaggio 2: l'estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md) Mostra come scrivere un componente che chiama un secondo componente per facilitare il completamento del lavoro, aggiornando le informazioni sull'autore nel database Microsoft SQL Server pubs; tutte le operazioni sono protette da un'unica transazione.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-109">Two previous parts of this COM+ services primer, [Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) and [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md) show how to write one component that calls a second component to assist in completing some work, updating author information in the Microsoft SQL Server Pubs database; all work is protected by a single transaction.</span></span> <span data-ttu-id="fc2e8-110">I componenti di esempio incentrati sul lavoro di aggiornamento dei dati di un autore e la verifica dell'indirizzo dell'autore e l'elaborazione delle transazioni, l' [attivazione JIT](com--just-in-time-activation.md)e la [protezione della concorrenza](com--synchronization.md)fornite da com+.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-110">The sample components focused on the work of updating an author's data and verifying the author's address, and COM+ provided transaction processing, [JIT activation](com--just-in-time-activation.md), and [concurrency protection](com--synchronization.md).</span></span>

<span data-ttu-id="fc2e8-111">In questo passaggio viene illustrato come riutilizzare i componenti creati nei passaggi 1 e 2 e vengono esaminati i metodi per la progettazione di tali componenti.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-111">This step demonstrates how to reuse the components created in steps 1 and 2 and looks at what this means to the design of those components.</span></span> <span data-ttu-id="fc2e8-112">Come illustrato nella figura seguente, ciò significa creare un nuovo componente, `AddNewAuthor` , che aggiunge nuovi autori al database chiamando `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="fc2e8-112">As shown in the following illustration, this means creating a new component, `AddNewAuthor`, that adds new authors to the database by calling `UpdateAuthorAddress`.</span></span>

![Diagramma che mostra il flusso quando si riutilizzano i componenti.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

<span data-ttu-id="fc2e8-114">Oltre a riutilizzare la funzionalità del componente esistente, `AddNewAuthor` chiama un altro nuovo componente denominato `ValidateAuthorName` .</span><span class="sxs-lookup"><span data-stu-id="fc2e8-114">In addition to reusing existing component functionality, `AddNewAuthor` calls another new component called `ValidateAuthorName`.</span></span> <span data-ttu-id="fc2e8-115">Come illustrato nella figura precedente, `ValidateAuthorName` è non transazionale.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-115">As the preceding illustration shows, `ValidateAuthorName` is non-transactional.</span></span> <span data-ttu-id="fc2e8-116">Il valore dell'attributo Transaction per questo componente viene lasciato con l'impostazione predefinita (**non supportata**) per escluderne il lavoro dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-116">The transaction attribute value for this component is left at its default setting (**Not Supported**) to exclude its work from the transaction.</span></span> <span data-ttu-id="fc2e8-117">Come illustrato nel codice di esempio Step 3, `ValidateAuthorName` esegue query di sola lettura sul database e l'errore di questa attività secondaria non dovrebbe essere in grado di interrompere la transazione.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-117">As shown in the step 3 sample code, `ValidateAuthorName` performs read-only queries on the database, and the failure of this minor task should not have the potential to abort the transaction.</span></span> <span data-ttu-id="fc2e8-118">Tuttavia, il valore dell'attributo Transaction del `AddNewAuthor` componente viene impostato su **required**.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-118">However, the transaction attribute value of the `AddNewAuthor` component is set to **Required**.</span></span>

<span data-ttu-id="fc2e8-119">I `AddNewAuthor` `UpdateAuthorAddress` componenti, e `ValidateAuthorAddress` tutti votano nella transazione.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-119">The `AddNewAuthor`, `UpdateAuthorAddress`, and `ValidateAuthorAddress` components all vote in the transaction.</span></span> <span data-ttu-id="fc2e8-120">In questa transazione, `AddNewAuthor` è l'oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-120">In this transaction, `AddNewAuthor` is the root object.</span></span> <span data-ttu-id="fc2e8-121">COM+ rende sempre il primo oggetto creato nella transazione come oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-121">COM+ always makes the first object created in the transaction the root object.</span></span>

<span data-ttu-id="fc2e8-122">In questo esempio, il riutilizzo del `UpdateAuthorAddress` componente è facile: com + recapita automaticamente i servizi previsti.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-122">In this example, reusing the `UpdateAuthorAddress` component is easy—COM+ automatically delivers the expected services.</span></span> <span data-ttu-id="fc2e8-123">Tuttavia, i risultati sarebbero diversi se il valore dell'attributo Transaction del `UpdateAuthorAddress` componente era inizialmente impostato su **requires New** anziché **required**.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-123">However, the results would be different if the transaction attribute value of the `UpdateAuthorAddress` component were initially set to **Requires New** instead of **Required**.</span></span> <span data-ttu-id="fc2e8-124">In superficie, entrambe le impostazioni appaiono simili; entrambi garantiscono una transazione.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-124">On the surface, both settings appear similar; both guarantee a transaction.</span></span> <span data-ttu-id="fc2e8-125">**Richiede New**, tuttavia, avvia sempre una nuova transazione, mentre **required** avvia una nuova transazione solo quando il chiamante dell'oggetto è non transazionale.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-125">**Requires New**, however, always starts a new transaction, while **Required** starts a new transaction only when the object's caller is non-transactional.</span></span> <span data-ttu-id="fc2e8-126">È possibile osservare da quanto è importante configurare `UpdateAuthorAddress` con attenzione e ponderatamente.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-126">You can see from this how important it was to configure `UpdateAuthorAddress` carefully and thoughtfully.</span></span> <span data-ttu-id="fc2e8-127">In caso contrario, COM+ potrebbe avere interpretato la richiesta di servizio in modo diverso, generando due transazioni non correlate, come illustrato nella figura seguente, anziché una.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-127">Otherwise, COM+ might have interpreted the service request differently, generating two unrelated transactions, as shown in the following illustration, instead of one.</span></span>

![Diagramma che mostra il flusso quando si riutilizzano i componenti con "requires New".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> <span data-ttu-id="fc2e8-129">Quando si riutilizzano i componenti, assicurarsi che i servizi siano configurati in modo da supportare il risultato desiderato.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-129">When you reuse components, make sure the services are configured to support your desired outcome.</span></span>

 

## <a name="sample-code"></a><span data-ttu-id="fc2e8-130">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="fc2e8-130">Sample code</span></span>

<span data-ttu-id="fc2e8-131">Il componente AddNewAuthor esegue aggiunte batch di nuovi autori consentendo all'oggetto di rimanere attivo fino a quando il client non rilascia il riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-131">The AddNewAuthor component performs batch additions of new authors by allowing the object to remain active until the client releases its reference to the object.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



<span data-ttu-id="fc2e8-132">Il `ValidateAuthorName` componente convalida i nomi di autore prima `AddNewAuthor` di aggiungere il nome al database.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-132">The `ValidateAuthorName` component validates author names before `AddNewAuthor` adds the name to the database.</span></span> <span data-ttu-id="fc2e8-133">Questo componente genera un errore al chiamante se si verifica un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-133">This component throws an error back to its caller if something unexpected happens.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a><span data-ttu-id="fc2e8-134">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="fc2e8-134">Summary</span></span>

-   <span data-ttu-id="fc2e8-135">In alcuni casi non si vuole che un componente voti nella transazione.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-135">There are times when you don't want a component to vote in the transaction.</span></span>
-   <span data-ttu-id="fc2e8-136">COM+ non impone l'attivazione JIT o la protezione della concorrenza su componenti non transazionali.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-136">COM+ does not enforce JIT activation or concurrency protection on non-transactional components.</span></span> <span data-ttu-id="fc2e8-137">Questi servizi possono essere configurati separatamente.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-137">You may configure these services separately.</span></span>
-   <span data-ttu-id="fc2e8-138">La configurazione di un componente chiamante influiscono sul modo in cui COM+ interpreta le richieste di servizio del componente chiamato.</span><span class="sxs-lookup"><span data-stu-id="fc2e8-138">A calling component's configuration affects how COM+ interprets the service requests of the called component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc2e8-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc2e8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc2e8-140">Passaggio 1: creazione di un componente transazionale</span><span class="sxs-lookup"><span data-stu-id="fc2e8-140">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="fc2e8-141">Passaggio 2: estensione di una transazione tra più componenti</span><span class="sxs-lookup"><span data-stu-id="fc2e8-141">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="fc2e8-142">Configurazione di transazioni</span><span class="sxs-lookup"><span data-stu-id="fc2e8-142">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="fc2e8-143">Progettazione per la scalabilità</span><span class="sxs-lookup"><span data-stu-id="fc2e8-143">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> </dl>

 

 



