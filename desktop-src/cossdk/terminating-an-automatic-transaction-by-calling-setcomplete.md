---
description: Terminazione di una transazione automatica mediante una chiamata a Tocomplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Terminazione di una transazione automatica mediante una chiamata a Tocomplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304724"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Terminazione di una transazione automatica mediante una chiamata a Tocomplete

Per utilizzare in modo efficace le transazioni automatiche, ogni componente transazionale deve indicare che ha completato il lavoro. Quando un'istanza dell'oggetto completa correttamente l'attività, deve impostare i flag coerenti e done su true chiamando il metodo [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , esposto tramite l'interfaccia [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) e l'oggetto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Il modo più efficiente per completare una transazione automatica consiste nell'disattivare in modo esplicito l'oggetto radice utilizzando il metodo [**Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Indicando in modo esplicito che un oggetto radice ha completato il proprio lavoro, è possibile ridurre la lunghezza della transazione.

Nell'esempio di Visual Basic seguente viene illustrato come indicare che un oggetto transazionale ha completato correttamente il proprio lavoro:


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flag coerenti e done](consistent-and-done-flags.md)
</dt> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



