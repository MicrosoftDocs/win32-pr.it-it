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
# <a name="step-2-extending-a-transaction-across-components"></a>Passaggio 2: estensione di una transazione tra i componenti

## <a name="objectives"></a>Obiettivi

In questo passaggio si apprenderanno le informazioni seguenti:

-   Flusso transazioni
-   Voto di più oggetti in una transazione

## <a name="description"></a>Descrizione

[Passaggio 1: la creazione di un componente transazionale](step-1--creating-a-transactional-component.md) Mostra come scrivere un semplice componente transazionale che aggiorna le informazioni sull'autore nel database Microsoft SQL Server pubs. Il passaggio 2 Mostra cosa accade quando una transazione viene estesa tra più componenti.

In conformità con il modello di programmazione COM+, `UpdateAuthorAddress` in viene chiamato un altro componente nel corso del completamento del suo lavoro. Il secondo componente, `ValidateAuthorAddress` , convalida l'indirizzo dell'autore e restituisce i risultati al chiamante `UpdateAuthorAddress` .

A differenza del chiamante, non `ValidateAuthorAddress` richiede una transazione, ma può comunque partecipare alla transazione del chiamante. In questo passaggio, il valore dell'attributo Transaction è impostato su **supported**, come illustrato nella figura seguente, che estende la transazione esistente al nuovo oggetto.

![Diagramma che mostra l'estensione della transazione esistente al nuovo oggetto.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

Il valore dell'attributo **supportato** estende (o scorre) una transazione esistente solo quando il chiamante è transazionale. Quando `UpdateAuthorAddress` chiama `ValidateAuthorAddress` , com+ esamina prima di tutto il contesto del chiamante per verificare se è transazionale. COM+ esamina quindi gli attributi del servizio impostati su `ValidateAuthorAddress` e assegna al nuovo oggetto lo stesso identificatore di transazione assegnato all'oggetto chiamante. Per comprendere meglio questo processo, vedere [attivazione del contesto](context-activation.md).

Poiché condividono lo stesso identificatore di transazione, è necessario che entrambi gli oggetti completino correttamente il proprio lavoro oppure COM+ interrompa la transazione (annullando le modifiche apportate al database pubs).

Tutti gli oggetti che partecipano a una transazione votano per eseguire il commit o interrompere la transazione. Il voto viene eseguito in modo esplicito quando si includono le istruzioni per il voto nel codice, come illustrato nell'estrazione seguente dal codice di esempio Step 1, che crea il `UpdateAuthorAddress` componente:


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



Il voto viene inoltre eseguito in modo implicito, come avviene nel `ValidateAuthorAddress` componente. A meno che l'oggetto non dichiari diversamente, COM+ presuppone che un oggetto abbia completato il proprio lavoro, ma che non è pronto per essere disattivato. COM+ fa il presupposto seguente:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Quando viene `ValidateAuthorAddress` restituito al chiamante, com+ legge il voto come commit. COM+ non conta i voti fino a quando non disattiva l'oggetto radice, ovvero il primo oggetto nella transazione, in questo caso l' `UpdateAuthorAddress` oggetto.

## <a name="sample-code"></a>Codice di esempio

Il `ValidateAuthorAddress` componente esegue una semplice verifica dell'indirizzo dell'autore. Poiché non `UpdateAuthorAddress` vota in modo esplicito, com+ utilizza le impostazioni di voto predefinite.


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

-   L'impostazione dell'attributo Transaction di un componente su **supported** può comportare la creazione del nuovo oggetto nella transazione dell'oggetto chiamante. COM+ esamina il contesto del chiamante per determinare lo stato transazionale del nuovo oggetto. Se il chiamante è transazionale, COM+ trasmette la transazione al nuovo oggetto.
-   Tutti gli oggetti che partecipano alla stessa transazione condividono un identificatore di transazione comune, che viene letto da COM+ dal contesto dell'oggetto.
-   Ogni oggetto in una transazione Vota indipendentemente da altri oggetti. COM+ conta i voti quando l'oggetto radice viene disattivato.
-   È possibile attivare o disattivare il voto di transazione di un oggetto tra commit e Abort fino a quando COM+ disattiva l'oggetto o fino a quando COM+ non disattiva l'oggetto radice e termina la transazione. Viene conteggiata solo l'ultima impostazione di voto. Le interfacce [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) e [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) forniscono metodi e producono risultati di voto simili, come illustrato nella tabella seguente. È possibile utilizzare una delle due interfacce per votare in modo esplicito in una transazione. 

    | Metodi di combinazione [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | Metodo equivalente [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TXABORT**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **true**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TXABORT**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **false**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ imposta il voto di un oggetto sull'equivalente di [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , a meno che il componente non voti esplicitamente.
-   Il voto in modo esplicito può ridurre la durata complessiva della transazione e rilasciare blocchi di risorse costosi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Passaggio 1: creazione di un componente transazionale](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Passaggio 3: riutilizzo dei componenti](step-3--reusing-components.md)
</dt> <dt>

[Attivazione del contesto](context-activation.md)
</dt> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




