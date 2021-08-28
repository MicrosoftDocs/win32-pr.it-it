---
description: Terminazione di una transazione automatica chiamando SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Terminazione di una transazione automatica chiamando SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d84d18b45309d750864d514728b8e23a3326e5edeba0bf144105bcbaa4797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499661"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Terminazione di una transazione automatica chiamando SetComplete

Per utilizzare le transazioni automatiche in modo efficace, ogni componente transazionale deve indicare che ha completato il proprio lavoro. Quando un'istanza dell'oggetto completa correttamente l'attività, deve impostare i flag coerenti e completati su True chiamando il metodo [**IObjectContext::SetComplete,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) esposto tramite [**l'interfaccia IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) e l'oggetto [**ObjectContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext)

Il modo più efficiente per completare una transazione automatica è disattivare in modo esplicito l'oggetto radice usando il [**metodo SetComplete.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) Indicando in modo esplicito che un oggetto radice ha completato il lavoro, è possibile ridurre la lunghezza della transazione.

Nell'Visual Basic seguente viene illustrato come indicare che un oggetto transazionale ha completato correttamente il lavoro:


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

[Flag coerenti e con completamento](consistent-and-done-flags.md)
</dt> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



