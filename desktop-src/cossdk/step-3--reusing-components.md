---
description: 'Passaggio 3: Riutilizzo dei componenti'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Passaggio 3: Riutilizzo dei componenti'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf500746e7c9052a421691299903437e129108405b49c7753a841e8ca505518
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895812"
---
# <a name="step-3-reusing-components"></a>Passaggio 3: Riutilizzo dei componenti

## <a name="objectives"></a>Obiettivi

In questo passaggio verranno fornite informazioni sugli elementi seguenti:

-   Componenti riutilizzabili.
-   Come pianificare la riutilizzabilità.

## <a name="description"></a>Descrizione

Due parti precedenti di questo primer di servizi COM+, [Passaggio 1:](step-1--creating-a-transactional-component.md) Creazione di un componente transazionale e Passaggio [2:](step-2--extending-a-transaction-across-multiple-components.md) Estensione di una transazione tra più componenti, illustrano come scrivere un componente che chiama un secondo componente per facilitare il completamento di alcune operazioni, l'aggiornamento delle informazioni sull'autore nel database pubs di Microsoft SQL Server. tutto il lavoro è protetto da una singola transazione. I componenti di esempio sono incentrati sul lavoro di aggiornamento dei dati di un autore e verifica dell'indirizzo dell'autore e sull'elaborazione delle transazioni fornita da COM+, attivazione [JIT](com--just-in-time-activation.md)e protezione della [concorrenza.](com--synchronization.md)

Questo passaggio illustra come riutilizzare i componenti creati nei passaggi 1 e 2 e esamina cosa significa per la progettazione di tali componenti. Come illustrato nella figura seguente, ciò significa creare un nuovo componente, , che aggiunge `AddNewAuthor` nuovi autori al database chiamando `UpdateAuthorAddress` .

![Diagramma che mostra il flusso durante il riutilizzo dei componenti.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

Oltre a riutilizzare le funzionalità dei componenti esistenti, `AddNewAuthor` chiama un altro nuovo componente denominato `ValidateAuthorName` . Come illustrato nella figura precedente, `ValidateAuthorName` non è transazionale. Il valore dell'attributo della transazione per questo componente viene lasciato nell'impostazione predefinita (**Non** supportato ) per escludere il lavoro dalla transazione. Come illustrato nel codice di esempio del passaggio 3, esegue query di sola lettura sul database e l'errore di questa attività secondaria non deve avere la possibilità di `ValidateAuthorName` interrompere la transazione. Tuttavia, il valore dell'attributo transaction del `AddNewAuthor` componente è impostato su **Required**.

I `AddNewAuthor` componenti , e `UpdateAuthorAddress` `ValidateAuthorAddress` votano tutti nella transazione. In questa transazione è `AddNewAuthor` l'oggetto radice. COM+ rende sempre il primo oggetto creato nella transazione l'oggetto radice.

In questo esempio il riutilizzo del `UpdateAuthorAddress` componente è semplice: COM+ fornisce automaticamente i servizi previsti. Tuttavia, i risultati sarebbero diversi se il valore dell'attributo della transazione del componente fosse inizialmente impostato su Requires `UpdateAuthorAddress` **New** invece di **Required**. In superficie, entrambe le impostazioni appaiono simili. entrambi garantiscono una transazione. **Richiede New**, tuttavia, avvia sempre una nuova transazione, mentre **Required** avvia una nuova transazione solo quando il chiamante dell'oggetto è non transazionale. È possibile vedere da questo aspetto quanto fosse importante configurare con attenzione `UpdateAuthorAddress` e attenzione. In caso contrario, COM+ potrebbe aver interpretato la richiesta di servizio in modo diverso, generando due transazioni non correlate, come illustrato nella figura seguente, anziché una.

![Diagramma che mostra il flusso durante il riutilizzo dei componenti con "Richiede nuovo".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Quando si riutilizzano i componenti, assicurarsi che i servizi siano configurati per supportare il risultato desiderato.

 

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



Il `ValidateAuthorName` componente convalida i nomi degli autori prima di aggiungere il nome al `AddNewAuthor` database. Questo componente genera un errore al chiamante se si verifica qualcosa di imprevisto.


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

-   A volte non si vuole che un componente voti nella transazione.
-   COM+ non applica l'attivazione JIT o la protezione della concorrenza nei componenti non transazionali. È possibile configurare questi servizi separatamente.
-   La configurazione di un componente chiamante influisce sul modo in cui COM+ interpreta le richieste di servizio del componente chiamato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Passaggio 1: Creazione di un componente transazionale](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Passaggio 2: Estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Configurazione delle transazioni](configuring-transactions.md)
</dt> <dt>

[Progettazione per la scalabilità](designing-for-scalability.md)
</dt> </dl>

 

 



