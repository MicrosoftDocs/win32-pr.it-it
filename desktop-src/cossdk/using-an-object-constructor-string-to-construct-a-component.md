---
description: Uso di una stringa del costruttore di oggetti per costruire un componente
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Uso di una stringa del costruttore di oggetti per costruire un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483412"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>Uso di una stringa del costruttore di oggetti per costruire un componente

Nell'esempio seguente viene illustrato come recuperare e utilizzare una stringa del costruttore di un oggetto a livello di codice quando viene creata un'istanza di un componente. Viene illustrata un'implementazione dell'interfaccia [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) che recupera una stringa del costruttore di oggetti. La stringa può quindi essere analizzata per impostare i valori iniziali o influenzare il comportamento del componente.

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alle stringhe del costruttore di oggetti COM+](com--object-constructor-strings-concepts.md)
</dt> <dt>

[Specifica di una stringa del costruttore di oggetti per un componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



