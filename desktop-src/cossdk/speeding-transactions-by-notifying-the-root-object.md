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
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="38436-103">Velocizzare le transazioni inviando una notifica all'oggetto radice</span><span class="sxs-lookup"><span data-stu-id="38436-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="38436-104">Per utilizzare in modo efficace le transazioni automatiche, ogni componente transazionale deve indicare che ha completato il lavoro.</span><span class="sxs-lookup"><span data-stu-id="38436-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="38436-105">Quando un'istanza dell'oggetto completa correttamente l'attività, deve impostare i flag coerenti e done su true chiamando il metodo [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="38436-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="38436-106">Quando tutti gli oggetti interni della transazione hanno chiamato **secomplete**, la transazione può essere terminata disattivando in modo esplicito l'oggetto radice chiamando il relativo metodo **secomplete** .</span><span class="sxs-lookup"><span data-stu-id="38436-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="38436-107">Indicando in modo esplicito che un oggetto radice ha completato il proprio lavoro, è possibile ridurre la lunghezza della transazione.</span><span class="sxs-lookup"><span data-stu-id="38436-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="38436-108">Quando un metodo di un oggetto transazionale ha esito negativo, l'oggetto deve impostare il flag coerente su false e il flag done su true chiamando il metodo [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) .</span><span class="sxs-lookup"><span data-stu-id="38436-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="38436-109">Chiamando il metodo **SetAbort** , un oggetto restituisce il controllo al chiamante e assicura che la transazione venga infine interrotta.</span><span class="sxs-lookup"><span data-stu-id="38436-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="38436-110">Tuttavia, a meno che l'oggetto che chiama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) sia la radice della transazione, la transazione continua a essere eseguita anche se non è possibile salvarla dalla fine dell'interruzione.</span><span class="sxs-lookup"><span data-stu-id="38436-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="38436-111">Per velocizzare la chiusura di una transazione non riuscita, è possibile generare un errore per avvisare l'oggetto radice anche per chiamare **SetAbort**.</span><span class="sxs-lookup"><span data-stu-id="38436-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="38436-112">Per il completamento, l'oggetto radice deve quindi inviare un messaggio di errore al client.</span><span class="sxs-lookup"><span data-stu-id="38436-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="38436-113">Sebbene esistano molti approcci diversi per la gestione degli errori, l'approccio dovrebbe coordinare in modo chiaro le comunicazioni tra gli oggetti interni e l'oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="38436-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="38436-114">I frammenti di codice Visual Basic seguenti illustrano un approccio alla gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="38436-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="38436-115">Nel primo frammento, un oggetto interno chiama [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), genera un errore e genera un messaggio di errore, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="38436-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="38436-116">Nel secondo frammento, l'oggetto radice gestisce l'errore e passa il messaggio al client, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="38436-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="38436-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38436-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38436-118">Gestione delle transazioni automatiche in COM+</span><span class="sxs-lookup"><span data-stu-id="38436-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



