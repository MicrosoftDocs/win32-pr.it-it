---
description: Velocizzare le transazioni inviando una notifica all'oggetto radice
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Velocizzare le transazioni inviando una notifica all'oggetto radice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225611"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Velocizzare le transazioni inviando una notifica all'oggetto radice

Per utilizzare in modo efficace le transazioni automatiche, ogni componente transazionale deve indicare che ha completato il lavoro. Quando un'istanza dell'oggetto completa correttamente l'attività, deve impostare i flag coerenti e done su true chiamando il metodo [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Quando tutti gli oggetti interni della transazione hanno chiamato **secomplete**, la transazione può essere terminata disattivando in modo esplicito l'oggetto radice chiamando il relativo metodo **secomplete** . Indicando in modo esplicito che un oggetto radice ha completato il proprio lavoro, è possibile ridurre la lunghezza della transazione.

Quando un metodo di un oggetto transazionale ha esito negativo, l'oggetto deve impostare il flag coerente su false e il flag done su true chiamando il metodo [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) . Chiamando il metodo **SetAbort** , un oggetto restituisce il controllo al chiamante e assicura che la transazione venga infine interrotta.

Tuttavia, a meno che l'oggetto che chiama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) sia la radice della transazione, la transazione continua a essere eseguita anche se non è possibile salvarla dalla fine dell'interruzione. Per velocizzare la chiusura di una transazione non riuscita, è possibile generare un errore per avvisare l'oggetto radice anche per chiamare **SetAbort**. Per il completamento, l'oggetto radice deve quindi inviare un messaggio di errore al client.

Sebbene esistano molti approcci diversi per la gestione degli errori, l'approccio dovrebbe coordinare in modo chiaro le comunicazioni tra gli oggetti interni e l'oggetto radice.

I frammenti di codice Visual Basic seguenti illustrano un approccio alla gestione degli errori. Nel primo frammento, un oggetto interno chiama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), genera un errore e genera un messaggio di errore, come indicato di seguito:

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

Nel secondo frammento, l'oggetto radice gestisce l'errore e passa il messaggio al client, come indicato di seguito:

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



