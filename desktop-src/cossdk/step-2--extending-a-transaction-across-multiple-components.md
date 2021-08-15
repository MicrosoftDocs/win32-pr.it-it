---
description: 'Passaggio 2: Estensione di una transazione tra più componenti'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Passaggio 2: Estensione di una transazione tra più componenti'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aa168eca7bfba29a4b00a6cd24b45d06c7610c76d47a4d6454e77295e57bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915809"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Passaggio 2: Estensione di una transazione tra componenti

## <a name="objectives"></a>Obiettivi

In questo passaggio verranno fornite informazioni sugli elementi seguenti:

-   Flusso della transazione
-   Modalità di voto di più oggetti in una transazione

## <a name="description"></a>Descrizione

[Passaggio 1: Creazione di un](step-1--creating-a-transactional-component.md) componente transazionale illustra come scrivere un componente transazionale semplice che aggiorna le informazioni sull'autore nel database Microsoft SQL Server Pubs. Il passaggio 2 mostra cosa accade quando una transazione viene estesa tra più componenti.

In linea con il modello di programmazione COM+, `UpdateAuthorAddress` chiama un altro componente nel corso del completamento del proprio lavoro. Il secondo componente, `ValidateAuthorAddress` , convalida l'indirizzo dell'autore e restituisce i risultati al chiamante, `UpdateAuthorAddress` .

A differenza del chiamante, `ValidateAuthorAddress` non richiede una transazione, ma può comunque partecipare alla transazione del chiamante. In questo passaggio il valore dell'attributo transaction è impostato su **Supported**, come illustrato nella figura seguente, che estende la transazione esistente al nuovo oggetto .

![Diagramma che illustra l'estensione della transazione esistente al nuovo oggetto .](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

Il **valore dell'attributo** Supported estende (o scorre) una transazione esistente solo quando il chiamante è transazionale. Quando chiama , COM+ esamina innanzitutto il contesto del chiamante `UpdateAuthorAddress` per verificare se è `ValidateAuthorAddress` transazionale. COM+ esamina quindi gli attributi del servizio impostati su e assegna al nuovo oggetto lo stesso identificatore di transazione `ValidateAuthorAddress` assegnato all'oggetto chiamante. Per comprendere meglio questo processo, vedere [Attivazione del contesto](context-activation.md).

Poiché condividono lo stesso identificatore di transazione, entrambi gli oggetti devono completare correttamente il lavoro oppure COM+ interrompe la transazione (annullando le modifiche apportate al database Pubs).

Tutti gli oggetti che partecipano a una transazione votano il commit o l'interruzione della transazione. Il voto viene eseguito in modo esplicito quando si includono istruzioni di voto nel codice, come illustrato nell'estrazione seguente dal codice di esempio del passaggio 1, che crea il `UpdateAuthorAddress` componente:


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



Il voto avviene anche in modo implicito, come avviene nel `ValidateAuthorAddress` componente. A meno che l'oggetto non dichiari diversamente, COM+ presuppone che un oggetto abbia completato correttamente il proprio lavoro, ma che non sia pronto per essere disattivato. COM+ presuppone quanto segue:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Quando `ValidateAuthorAddress` torna al chiamante, COM+ legge il proprio voto come commit. COM+ non conta i voti finché non disattiva l'oggetto radice, che in questo caso è il primo oggetto della `UpdateAuthorAddress` transazione, l'oggetto .

## <a name="sample-code"></a>Codice di esempio

Il `ValidateAuthorAddress` componente esegue un semplice controllo dell'indirizzo dell'autore. Poiché `UpdateAuthorAddress` non vota in modo esplicito, COM+ usa le impostazioni di voto predefinite.


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



## <a name="summary"></a>Riepilogo

-   L'impostazione dell'attributo della transazione di un componente su **Supportato** può comportare la creazione del nuovo oggetto nella transazione dell'oggetto chiamante. COM+ esamina il contesto del chiamante per determinare lo stato transazionale del nuovo oggetto. Se il chiamante è transazionale, COM+ passa la transazione al nuovo oggetto.
-   Tutti gli oggetti che partecipano alla stessa transazione condividono un identificatore di transazione comune, che COM+ legge dal contesto dell'oggetto.
-   Ogni oggetto in una transazione vota indipendentemente dagli altri oggetti. COM+ conta i voti quando l'oggetto radice viene disattivato.
-   È possibile attivare o disattivare il voto della transazione di un oggetto tra commit e interruzione finché COM+ non disattiva l'oggetto o finché COM+ non disattiva l'oggetto radice e termina la transazione. Viene conteggiato solo l'ultima impostazione di voto. Le [**interfacce IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) [**e IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) forniscono metodi che producono risultati di voto simili, come illustrato nella tabella seguente. È possibile usare una delle due interfacce per votare in modo esplicito in una transazione. 

    | [**Metodi di combinazione di IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | [**Metodo equivalente IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>  | [**Setcomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>   | [**Setabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ imposta il voto di un oggetto sull'equivalente di [**EnableCommit,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) a meno che il componente non voti in modo esplicito.
-   Il voto esplicito può ridurre la durata complessiva della transazione e rilasciare blocchi di risorse costosi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Passaggio 1: Creazione di un componente transazionale](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Passaggio 3: Riutilizzo dei componenti](step-3--reusing-components.md)
</dt> <dt>

[Attivazione del contesto](context-activation.md)
</dt> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




