---
description: 'Passaggio 1: creazione di un componente transazionale'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Passaggio 1: creazione di un componente transazionale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350931"
---
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="6d8db-103">Passaggio 1: creazione di un componente transazionale</span><span class="sxs-lookup"><span data-stu-id="6d8db-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="6d8db-104">Obiettivi</span><span class="sxs-lookup"><span data-stu-id="6d8db-104">Objectives</span></span>

<span data-ttu-id="6d8db-105">In questo passaggio si apprenderà quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6d8db-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="6d8db-106">Come scrivere un componente transazionale in Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6d8db-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="6d8db-107">Quali sono le impostazioni predefinite per i servizi COM+</span><span class="sxs-lookup"><span data-stu-id="6d8db-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="6d8db-108">Come configurare i servizi COM+</span><span class="sxs-lookup"><span data-stu-id="6d8db-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="6d8db-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d8db-109">Description</span></span>

<span data-ttu-id="6d8db-110">Il componente UpdateAuthorAddress, il componente da creare in questa sezione, aggiorna l'indirizzo di un autore esistente nel database pubs.</span><span class="sxs-lookup"><span data-stu-id="6d8db-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="6d8db-111">Il database pubs è un database di esempio fornito con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d8db-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="6d8db-112">Contiene informazioni sulla pubblicazione, ad esempio nomi di autore, indirizzi e titoli di libri.</span><span class="sxs-lookup"><span data-stu-id="6d8db-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="6d8db-113">Pubs è l'archivio dati usato in questo nozioni di fondo.</span><span class="sxs-lookup"><span data-stu-id="6d8db-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="6d8db-114">Poiché UpdateAuthorAddress aggiorna un archivio dati, è consigliabile includere il lavoro in una transazione, come illustrato nella figura seguente, in modo che quando un client chiama il componente, COM+ avvia automaticamente una transazione e integra il database (Resource Manager) in tale transazione.</span><span class="sxs-lookup"><span data-stu-id="6d8db-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="6d8db-115">Per informazioni dettagliate sulle transazioni in COM+, vedere [transazioni com+](com--transactions.md).</span><span class="sxs-lookup"><span data-stu-id="6d8db-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![Diagramma che mostra una transazione COM+ con UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="6d8db-117">Per rendere UpdateAuthorAddress un componente transazionale, sono necessari i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d8db-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="6d8db-118">È necessario scrivere il componente.</span><span class="sxs-lookup"><span data-stu-id="6d8db-118">The component must be written.</span></span> <span data-ttu-id="6d8db-119">Per una protezione aggiuntiva, viene aggiunta una subroutine che verifica che COM+ abbia creato l'oggetto in una transazione.</span><span class="sxs-lookup"><span data-stu-id="6d8db-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="6d8db-120">Inoltre, la gestione degli errori di base è inclusa nel componente per semplificare il ripristino degli errori.</span><span class="sxs-lookup"><span data-stu-id="6d8db-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="6d8db-121">La verifica delle transazioni e la gestione degli errori migliorano l'affidabilità del componente.</span><span class="sxs-lookup"><span data-stu-id="6d8db-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="6d8db-122">Per un elenco completo del componente UpdateAuthorAddress, vedere il codice di esempio del passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="6d8db-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="6d8db-123">Dopo l'aggiunta del componente a un'applicazione COM+ e l'installazione dell'applicazione, l'attributo Transaction deve essere impostato su **required**, che garantisce che com+ crei ogni oggetto UpdateAuthorAddress in una transazione.</span><span class="sxs-lookup"><span data-stu-id="6d8db-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="6d8db-124">Per istruzioni su come impostare l'attributo Transaction per un componente, vedere [impostazione dell'attributo Transaction](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="6d8db-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="6d8db-125">Impostando l'attributo Transaction su un componente viene definito il modo in cui COM+ crea ogni oggetto per quanto riguarda le transazioni.</span><span class="sxs-lookup"><span data-stu-id="6d8db-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="6d8db-126">I valori degli attributi di transazione vengono **ignorati**, **non supportati**, **supportati**, **necessari** e sono richiesti **nuovi**.</span><span class="sxs-lookup"><span data-stu-id="6d8db-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="6d8db-127">Il valore **obbligatorio** non è uno dei valori di attributo predefiniti di un componente.</span><span class="sxs-lookup"><span data-stu-id="6d8db-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="6d8db-128">COM+ associa il servizio transazione all'attivazione e alla concorrenza JIT (just-in-Time).</span><span class="sxs-lookup"><span data-stu-id="6d8db-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="6d8db-129">Quando si dichiara un componente come transazionale, COM+ impone anche l'attivazione JIT e la protezione della concorrenza (sincronizzazione).</span><span class="sxs-lookup"><span data-stu-id="6d8db-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="6d8db-130">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="6d8db-130">Sample code</span></span>

<span data-ttu-id="6d8db-131">Il componente UpdateAuthorAddress apre una connessione al database pubs, consentendo all'utente di modificare il nome, l'indirizzo o lo stato del contratto di un autore.</span><span class="sxs-lookup"><span data-stu-id="6d8db-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="6d8db-132">Viene inoltre chiamato un secondo componente, illustrato nel [passaggio 2: estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md).</span><span class="sxs-lookup"><span data-stu-id="6d8db-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="6d8db-133">Per utilizzare il codice seguente in un progetto di Microsoft Visual Basic, aprire un nuovo progetto ActiveX.dll e aggiungere i riferimenti alla libreria di Microsoft ActiveX Data Objects e alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="6d8db-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="6d8db-134">Il codice di esempio in questo nozioni di base è a scopo illustrativo e potrebbe non essere il più efficiente per la gestione temporanea e la produzione effettive.</span><span class="sxs-lookup"><span data-stu-id="6d8db-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a><span data-ttu-id="6d8db-135">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="6d8db-135">Summary</span></span>

-   <span data-ttu-id="6d8db-136">COM+ assegna i valori predefiniti dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="6d8db-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="6d8db-137">È possibile riconfigurare la maggior parte degli attributi del servizio.</span><span class="sxs-lookup"><span data-stu-id="6d8db-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="6d8db-138">L'impostazione dell'attributo Transaction di un componente su **required** garantisce che com+ debba creare ogni istanza di tale componente in una transazione, ma non avvii necessariamente una nuova transazione.</span><span class="sxs-lookup"><span data-stu-id="6d8db-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="6d8db-139">La verifica della presenza di una transazione conferma che il valore dell'attributo Transaction del componente non è stato reimpostato inavvertitamente su un valore non transazionale, ad esempio **Ignora** o **non supportato**.</span><span class="sxs-lookup"><span data-stu-id="6d8db-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="6d8db-140">La gestione degli errori rende il componente più affidabile e più semplice da risolvere.</span><span class="sxs-lookup"><span data-stu-id="6d8db-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="6d8db-141">COM+ impone l' [attivazione JIT](com--just-in-time-activation.md) e i servizi di [protezione della concorrenza](com--synchronization.md) per i componenti transazionali.</span><span class="sxs-lookup"><span data-stu-id="6d8db-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="6d8db-142">Quando si chiude la connessione al database, si consente a un altro componente della stessa transazione di riutilizzare la connessione dal pool di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6d8db-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="6d8db-143">Il pool di connessioni non deve essere confuso con il [pool di oggetti](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="6d8db-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d8db-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d8db-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d8db-145">Passaggio 2: estensione di una transazione tra più componenti</span><span class="sxs-lookup"><span data-stu-id="6d8db-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="6d8db-146">Passaggio 3: riutilizzo dei componenti</span><span class="sxs-lookup"><span data-stu-id="6d8db-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="6d8db-147">Attivazione JIT (just-in-Time) COM+</span><span class="sxs-lookup"><span data-stu-id="6d8db-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="6d8db-148">Sincronizzazione COM+</span><span class="sxs-lookup"><span data-stu-id="6d8db-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="6d8db-149">Configurazione di transazioni</span><span class="sxs-lookup"><span data-stu-id="6d8db-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="6d8db-150">Creazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="6d8db-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="6d8db-151">Impostazione dell'attributo Transaction</span><span class="sxs-lookup"><span data-stu-id="6d8db-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



