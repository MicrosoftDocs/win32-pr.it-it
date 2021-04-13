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
# <a name="using-an-object-constructor-string-to-construct-a-component"></a><span data-ttu-id="6fcc1-103">Uso di una stringa del costruttore di oggetti per costruire un componente</span><span class="sxs-lookup"><span data-stu-id="6fcc1-103">Using an Object Constructor String to Construct a Component</span></span>

<span data-ttu-id="6fcc1-104">Nell'esempio seguente viene illustrato come recuperare e utilizzare una stringa del costruttore di un oggetto a livello di codice quando viene creata un'istanza di un componente.</span><span class="sxs-lookup"><span data-stu-id="6fcc1-104">The following example illustrates how to programmatically retrieve and use an object constructor string when a component is instantiated.</span></span> <span data-ttu-id="6fcc1-105">Viene illustrata un'implementazione dell'interfaccia [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) che recupera una stringa del costruttore di oggetti.</span><span class="sxs-lookup"><span data-stu-id="6fcc1-105">It shows an implementation of the [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) interface that retrieves an object constructor string.</span></span> <span data-ttu-id="6fcc1-106">La stringa può quindi essere analizzata per impostare i valori iniziali o influenzare il comportamento del componente.</span><span class="sxs-lookup"><span data-stu-id="6fcc1-106">The string can then be parsed to set initial values or influence the behavior of the component.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="6fcc1-107">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6fcc1-107">Visual Basic</span></span>


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="6fcc1-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6fcc1-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fcc1-109">Concetti relativi alle stringhe del costruttore di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="6fcc1-109">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="6fcc1-110">Specifica di una stringa del costruttore di oggetti per un componente</span><span class="sxs-lookup"><span data-stu-id="6fcc1-110">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



