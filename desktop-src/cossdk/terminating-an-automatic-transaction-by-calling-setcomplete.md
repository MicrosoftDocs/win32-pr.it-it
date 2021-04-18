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
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="202ce-103">Terminazione di una transazione automatica mediante una chiamata a Tocomplete</span><span class="sxs-lookup"><span data-stu-id="202ce-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="202ce-104">Per utilizzare in modo efficace le transazioni automatiche, ogni componente transazionale deve indicare che ha completato il lavoro.</span><span class="sxs-lookup"><span data-stu-id="202ce-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="202ce-105">Quando un'istanza dell'oggetto completa correttamente l'attività, deve impostare i flag coerenti e done su true chiamando il metodo [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , esposto tramite l'interfaccia [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) e l'oggetto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .</span><span class="sxs-lookup"><span data-stu-id="202ce-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="202ce-106">Il modo più efficiente per completare una transazione automatica consiste nell'disattivare in modo esplicito l'oggetto radice utilizzando il metodo [**Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="202ce-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="202ce-107">Indicando in modo esplicito che un oggetto radice ha completato il proprio lavoro, è possibile ridurre la lunghezza della transazione.</span><span class="sxs-lookup"><span data-stu-id="202ce-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="202ce-108">Nell'esempio di Visual Basic seguente viene illustrato come indicare che un oggetto transazionale ha completato correttamente il proprio lavoro:</span><span class="sxs-lookup"><span data-stu-id="202ce-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="202ce-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="202ce-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="202ce-110">Flag coerenti e done</span><span class="sxs-lookup"><span data-stu-id="202ce-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="202ce-111">Gestione delle transazioni automatiche in COM+</span><span class="sxs-lookup"><span data-stu-id="202ce-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



