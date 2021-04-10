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
# <a name="step-1-creating-a-transactional-component"></a>Passaggio 1: creazione di un componente transazionale

## <a name="objectives"></a>Obiettivi

In questo passaggio si apprenderà quanto segue:

-   Come scrivere un componente transazionale in Microsoft Visual Basic
-   Quali sono le impostazioni predefinite per i servizi COM+
-   Come configurare i servizi COM+

## <a name="description"></a>Descrizione

Il componente UpdateAuthorAddress, il componente da creare in questa sezione, aggiorna l'indirizzo di un autore esistente nel database pubs. Il database pubs è un database di esempio fornito con Microsoft SQL Server. Contiene informazioni sulla pubblicazione, ad esempio nomi di autore, indirizzi e titoli di libri.

> [!Note]  
> Pubs è l'archivio dati usato in questo nozioni di fondo.

 

Poiché UpdateAuthorAddress aggiorna un archivio dati, è consigliabile includere il lavoro in una transazione, come illustrato nella figura seguente, in modo che quando un client chiama il componente, COM+ avvia automaticamente una transazione e integra il database (Resource Manager) in tale transazione. Per informazioni dettagliate sulle transazioni in COM+, vedere [transazioni com+](com--transactions.md).

![Diagramma che mostra una transazione COM+ con UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Per rendere UpdateAuthorAddress un componente transazionale, sono necessari i passaggi seguenti:

1.  È necessario scrivere il componente. Per una protezione aggiuntiva, viene aggiunta una subroutine che verifica che COM+ abbia creato l'oggetto in una transazione. Inoltre, la gestione degli errori di base è inclusa nel componente per semplificare il ripristino degli errori. La verifica delle transazioni e la gestione degli errori migliorano l'affidabilità del componente. Per un elenco completo del componente UpdateAuthorAddress, vedere il codice di esempio del passaggio 1.
2.  Dopo l'aggiunta del componente a un'applicazione COM+ e l'installazione dell'applicazione, l'attributo Transaction deve essere impostato su **required**, che garantisce che com+ crei ogni oggetto UpdateAuthorAddress in una transazione. Per istruzioni su come impostare l'attributo Transaction per un componente, vedere [impostazione dell'attributo Transaction](setting-the-transaction-attribute.md).
    > [!Note]  
    > Impostando l'attributo Transaction su un componente viene definito il modo in cui COM+ crea ogni oggetto per quanto riguarda le transazioni. I valori degli attributi di transazione vengono **ignorati**, **non supportati**, **supportati**, **necessari** e sono richiesti **nuovi**. Il valore **obbligatorio** non è uno dei valori di attributo predefiniti di un componente.

     

COM+ associa il servizio transazione all'attivazione e alla concorrenza JIT (just-in-Time). Quando si dichiara un componente come transazionale, COM+ impone anche l'attivazione JIT e la protezione della concorrenza (sincronizzazione).

## <a name="sample-code"></a>Codice di esempio

Il componente UpdateAuthorAddress apre una connessione al database pubs, consentendo all'utente di modificare il nome, l'indirizzo o lo stato del contratto di un autore. Viene inoltre chiamato un secondo componente, illustrato nel [passaggio 2: estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md).

Per utilizzare il codice seguente in un progetto di Microsoft Visual Basic, aprire un nuovo progetto ActiveX.dll e aggiungere i riferimenti alla libreria di Microsoft ActiveX Data Objects e alla libreria dei tipi di servizi COM+.

> [!Note]  
> Il codice di esempio in questo nozioni di base è a scopo illustrativo e potrebbe non essere il più efficiente per la gestione temporanea e la produzione effettive.

 


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



## <a name="summary"></a>Riepilogo

-   COM+ assegna i valori predefiniti dell'attributo. È possibile riconfigurare la maggior parte degli attributi del servizio.
-   L'impostazione dell'attributo Transaction di un componente su **required** garantisce che com+ debba creare ogni istanza di tale componente in una transazione, ma non avvii necessariamente una nuova transazione.
-   La verifica della presenza di una transazione conferma che il valore dell'attributo Transaction del componente non è stato reimpostato inavvertitamente su un valore non transazionale, ad esempio **Ignora** o **non supportato**.
-   La gestione degli errori rende il componente più affidabile e più semplice da risolvere.
-   COM+ impone l' [attivazione JIT](com--just-in-time-activation.md) e i servizi di [protezione della concorrenza](com--synchronization.md) per i componenti transazionali.
-   Quando si chiude la connessione al database, si consente a un altro componente della stessa transazione di riutilizzare la connessione dal pool di connessioni. Il pool di connessioni non deve essere confuso con il [pool di oggetti](com--object-pooling.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Passaggio 2: estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Passaggio 3: riutilizzo dei componenti](step-3--reusing-components.md)
</dt> <dt>

[Attivazione JIT (just-in-Time) COM+](com--just-in-time-activation.md)
</dt> <dt>

[Sincronizzazione COM+](com--synchronization.md)
</dt> <dt>

[Configurazione di transazioni](configuring-transactions.md)
</dt> <dt>

[Creazione di applicazioni COM+](creating-com--applications.md)
</dt> <dt>

[Impostazione dell'attributo Transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



