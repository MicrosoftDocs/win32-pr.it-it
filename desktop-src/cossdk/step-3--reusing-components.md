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
# <a name="step-3-reusing-components"></a>Passaggio 3: riutilizzo dei componenti

## <a name="objectives"></a>Obiettivi

In questo passaggio si apprenderanno le informazioni seguenti:

-   Componenti riutilizzabili.
-   Come pianificare la riusabilità.

## <a name="description"></a>Descrizione

Due parti precedenti di questo nozioni di base sui servizi COM+, [passaggio 1: creazione di un componente transazionale](step-1--creating-a-transactional-component.md) e [passaggio 2: l'estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md) Mostra come scrivere un componente che chiama un secondo componente per facilitare il completamento del lavoro, aggiornando le informazioni sull'autore nel database Microsoft SQL Server pubs; tutte le operazioni sono protette da un'unica transazione. I componenti di esempio incentrati sul lavoro di aggiornamento dei dati di un autore e la verifica dell'indirizzo dell'autore e l'elaborazione delle transazioni, l' [attivazione JIT](com--just-in-time-activation.md)e la [protezione della concorrenza](com--synchronization.md)fornite da com+.

In questo passaggio viene illustrato come riutilizzare i componenti creati nei passaggi 1 e 2 e vengono esaminati i metodi per la progettazione di tali componenti. Come illustrato nella figura seguente, ciò significa creare un nuovo componente, `AddNewAuthor` , che aggiunge nuovi autori al database chiamando `UpdateAuthorAddress` .

![Diagramma che mostra il flusso quando si riutilizzano i componenti.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

Oltre a riutilizzare la funzionalità del componente esistente, `AddNewAuthor` chiama un altro nuovo componente denominato `ValidateAuthorName` . Come illustrato nella figura precedente, `ValidateAuthorName` è non transazionale. Il valore dell'attributo Transaction per questo componente viene lasciato con l'impostazione predefinita (**non supportata**) per escluderne il lavoro dalla transazione. Come illustrato nel codice di esempio Step 3, `ValidateAuthorName` esegue query di sola lettura sul database e l'errore di questa attività secondaria non dovrebbe essere in grado di interrompere la transazione. Tuttavia, il valore dell'attributo Transaction del `AddNewAuthor` componente viene impostato su **required**.

I `AddNewAuthor` `UpdateAuthorAddress` componenti, e `ValidateAuthorAddress` tutti votano nella transazione. In questa transazione, `AddNewAuthor` è l'oggetto radice. COM+ rende sempre il primo oggetto creato nella transazione come oggetto radice.

In questo esempio, il riutilizzo del `UpdateAuthorAddress` componente è facile: com + recapita automaticamente i servizi previsti. Tuttavia, i risultati sarebbero diversi se il valore dell'attributo Transaction del `UpdateAuthorAddress` componente era inizialmente impostato su **requires New** anziché **required**. In superficie, entrambe le impostazioni appaiono simili; entrambi garantiscono una transazione. **Richiede New**, tuttavia, avvia sempre una nuova transazione, mentre **required** avvia una nuova transazione solo quando il chiamante dell'oggetto è non transazionale. È possibile osservare da quanto è importante configurare `UpdateAuthorAddress` con attenzione e ponderatamente. In caso contrario, COM+ potrebbe avere interpretato la richiesta di servizio in modo diverso, generando due transazioni non correlate, come illustrato nella figura seguente, anziché una.

![Diagramma che mostra il flusso quando si riutilizzano i componenti con "requires New".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Quando si riutilizzano i componenti, assicurarsi che i servizi siano configurati in modo da supportare il risultato desiderato.

 

## <a name="sample-code"></a>Codice di esempio

Il componente AddNewAuthor esegue aggiunte batch di nuovi autori consentendo all'oggetto di rimanere attivo fino a quando il client non rilascia il riferimento all'oggetto.


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



Il `ValidateAuthorName` componente convalida i nomi di autore prima `AddNewAuthor` di aggiungere il nome al database. Questo componente genera un errore al chiamante se si verifica un evento imprevisto.


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



## <a name="summary"></a>Riepilogo

-   In alcuni casi non si vuole che un componente voti nella transazione.
-   COM+ non impone l'attivazione JIT o la protezione della concorrenza su componenti non transazionali. Questi servizi possono essere configurati separatamente.
-   La configurazione di un componente chiamante influiscono sul modo in cui COM+ interpreta le richieste di servizio del componente chiamato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Passaggio 1: creazione di un componente transazionale](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Passaggio 2: estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Configurazione di transazioni](configuring-transactions.md)
</dt> <dt>

[Progettazione per la scalabilità](designing-for-scalability.md)
</dt> </dl>

 

 



