---
description: Crea un oggetto transazionale generico che avvia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Classe TransactionContextEx (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748839"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="5b36e-104">Classe TransactionContextEx</span><span class="sxs-lookup"><span data-stu-id="5b36e-104">TransactionContextEx class</span></span>

<span data-ttu-id="5b36e-105">Crea un oggetto transazionale generico che avvia una transazione.</span><span class="sxs-lookup"><span data-stu-id="5b36e-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="5b36e-106">Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.</span><span class="sxs-lookup"><span data-stu-id="5b36e-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="5b36e-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="5b36e-107">When to implement</span></span>

<span data-ttu-id="5b36e-108">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="5b36e-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="5b36e-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b36e-109">Requirement</span></span> | <span data-ttu-id="5b36e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="5b36e-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="5b36e-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="5b36e-111">CLSID</span></span>      | <span data-ttu-id="5b36e-112">\_TRANSACTIONCONTEXTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="5b36e-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="5b36e-113">ProgID</span><span class="sxs-lookup"><span data-stu-id="5b36e-113">ProgID</span></span>     | <span data-ttu-id="5b36e-114">L "TxCTx. TransactionContextEx"</span><span class="sxs-lookup"><span data-stu-id="5b36e-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="5b36e-115">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5b36e-115">Interfaces</span></span> | [<span data-ttu-id="5b36e-116">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="5b36e-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="5b36e-117">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="5b36e-117">When to use</span></span>

<span data-ttu-id="5b36e-118">Un client non transazionale utilizza questa classe per avviare una transazione.</span><span class="sxs-lookup"><span data-stu-id="5b36e-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="5b36e-119">Utilizzando i metodi di questa classe, il client può chiamare oggetti COM aggiuntivi che, se configurati per partecipare a una transazione, vengono eseguiti all'interno del limite della transazione dell'oggetto del contesto di transazione.</span><span class="sxs-lookup"><span data-stu-id="5b36e-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="5b36e-120">In base alla logica di business, il client può eseguire in modo esplicito il commit o l'interruzione della transazione.</span><span class="sxs-lookup"><span data-stu-id="5b36e-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="5b36e-121">La classe **TransactionContextEx** limita il riutilizzo della logica di business che guida la transazione.</span><span class="sxs-lookup"><span data-stu-id="5b36e-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="5b36e-122">Per questo motivo, è consigliabile usare sporadicamente gli oggetti di cui è stata creata un'istanza dalla classe **TransactionContextEx** .</span><span class="sxs-lookup"><span data-stu-id="5b36e-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b36e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b36e-123">Remarks</span></span>

<span data-ttu-id="5b36e-124">Per creare questo oggetto, chiamare [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="5b36e-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="5b36e-125">La classe **TransactionContextEx** non è stata progettata per essere utilizzata in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b36e-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="5b36e-126">In alternativa, usare la classe [**TransactionContext**](transactioncontext.md) .</span><span class="sxs-lookup"><span data-stu-id="5b36e-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b36e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b36e-127">Requirements</span></span>



| <span data-ttu-id="5b36e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b36e-128">Requirement</span></span> | <span data-ttu-id="5b36e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5b36e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b36e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b36e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5b36e-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b36e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5b36e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b36e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5b36e-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b36e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b36e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b36e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b36e-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b36e-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b36e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b36e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b36e-137">Configurazione di transazioni</span><span class="sxs-lookup"><span data-stu-id="5b36e-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="5b36e-138">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="5b36e-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="5b36e-139">**TransactionContext**</span><span class="sxs-lookup"><span data-stu-id="5b36e-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 




