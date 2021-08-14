---
description: 'Passaggio 1: Creazione di un componente transazionale'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Passaggio 1: Creazione di un componente transazionale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f5c87fb5c5f615ee04a3233f1a563d5ae5230e4dd18908c78e94092ff0f5c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305411"
---
# <a name="step-1-creating-a-transactional-component"></a>Passaggio 1: Creazione di un componente transazionale

## <a name="objectives"></a>Obiettivi

In questo passaggio si apprenderà quanto segue:

-   Come scrivere un componente transazionale in Microsoft Visual Basic
-   Impostazioni predefinite per i servizi COM+
-   Come configurare i servizi COM+

## <a name="description"></a>Descrizione

Il componente UpdateAuthorAddress, il componente da creare in questa sezione, aggiorna l'indirizzo di un autore esistente nel database Pubs. Il database Pubs è un database di esempio fornito con Microsoft SQL Server. Contiene informazioni di pubblicazione, ad esempio nomi di autori, indirizzi e titoli di libri.

> [!Note]  
> Pubs è l'archivio dati usato in questa prima pagina.

 

Poiché UpdateAuthorAddress aggiorna un archivio dati, è consigliabile includere il lavoro in una transazione, come illustrato nella figura seguente, in modo che quando un client chiama il componente, COM+ avvia automaticamente una transazione e integra il database (gestione risorse) in tale transazione. Per informazioni dettagliate sulle transazioni in COM+, vedere [Transazioni COM+.](com--transactions.md)

![Diagramma che mostra una transazione COM+ con UpdateAuthorAddress.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Per rendere UpdateAuthorAddress un componente transazionale, sono necessari i passaggi seguenti:

1.  Il componente deve essere scritto. Per una protezione aggiuntiva, viene aggiunta una subroutine, verificando che COM+ ha creato l'oggetto in una transazione. Inoltre, la gestione degli errori di base è inclusa nel componente per semplificare il ripristino degli errori. La verifica delle transazioni e la gestione degli errori migliorano l'affidabilità del componente. Per un elenco completo del componente UpdateAuthorAddress, vedere il codice di esempio del passaggio 1.
2.  Dopo aver aggiunto il componente a un'applicazione COM+ e aver installato l'applicazione, l'attributo della transazione deve essere impostato su **Required,** che garantisce che COM+ crei ogni oggetto UpdateAuthorAddress in una transazione. Per istruzioni su come impostare l'attributo della transazione per un componente, vedere [Impostazione dell'attributo transaction](setting-the-transaction-attribute.md).
    > [!Note]  
    > L'impostazione dell'attributo transaction in un componente definisce il modo in cui COM+ crea ogni oggetto in relazione alle transazioni. I valori degli attributi della **transazione** sono **Ignorato**, Non supportato , **Supportato**, **Obbligatorio** **e Richiede nuovo**. Il **valore** Required non è uno dei valori di attributo predefiniti di un componente.

     

COM+ associa il servizio di transazione con l'attivazione e la concorrenza JIT (Just-In-Time). Quando si dichiara un componente come transazionale, COM+ applica anche l'attivazione JIT e la protezione della concorrenza (sincronizzazione).

## <a name="sample-code"></a>Codice di esempio

Il componente UpdateAuthorAddress apre una connessione al database Pubs, consentendo all'utente di modificare il nome, l'indirizzo o lo stato del contratto di un autore. Chiama anche un secondo componente, descritto in [Passaggio 2: Estensione di una transazione tra più componenti.](step-2--extending-a-transaction-across-multiple-components.md)

Per usare il codice seguente in un progetto di Microsoft Visual Basic, aprire un nuovo progetto ActiveX.dll e aggiungere riferimenti alla libreria degli oggetti dati di Microsoft ActiveX e alla libreria dei tipi dei servizi COM+.

> [!Note]  
> Il codice di esempio in questa nozioni di base è a scopo illustrativo e potrebbe non essere il più efficiente per la gestione temporanea e la produzione effettive.

 


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

-   COM+ assegna valori di attributo predefiniti. È possibile riconfigurare la maggior parte degli attributi del servizio.
-   L'impostazione dell'attributo transaction di un componente su **Required** garantisce che COM+ deve creare ogni istanza di tale componente in una transazione, ma non avvia necessariamente una nuova transazione.
-   La verifica della presenza di una transazione conferma che il valore dell'attributo della transazione del componente non è stato inavvertitamente reimpostato su un valore non transazionale, ad esempio **Ignora** o Non **supportato.**
-   La gestione degli errori rende il componente più affidabile e più facile da risolvere.
-   COM+ applica [l'attivazione JIT](com--just-in-time-activation.md) e [i servizi di protezione della concorrenza](com--synchronization.md) per i componenti transazionali.
-   La chiusura della connessione al database al termine dell'operazione consente a un altro componente nella stessa transazione di riutilizzare la connessione dal pool di connessioni. Il pool di connessioni non deve essere confuso con il [pool di oggetti.](com--object-pooling.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Passaggio 2: Estensione di una transazione tra più componenti](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Passaggio 3: Riutilizzo dei componenti](step-3--reusing-components.md)
</dt> <dt>

[Attivazione JUST-In-Time COM+](com--just-in-time-activation.md)
</dt> <dt>

[Sincronizzazione COM+](com--synchronization.md)
</dt> <dt>

[Configurazione delle transazioni](configuring-transactions.md)
</dt> <dt>

[Creazione di applicazioni COM+](creating-com--applications.md)
</dt> <dt>

[Impostazione dell'attributo transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



