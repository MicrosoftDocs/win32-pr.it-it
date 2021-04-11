---
description: Crea un oggetto transazionale generico che avvia una transazione.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Classe TransactionContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225754"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="f75ec-103">Classe TransactionContext</span><span class="sxs-lookup"><span data-stu-id="f75ec-103">TransactionContext class</span></span>

<span data-ttu-id="f75ec-104">Crea un oggetto transazionale generico che avvia una transazione.</span><span class="sxs-lookup"><span data-stu-id="f75ec-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="f75ec-105">Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.</span><span class="sxs-lookup"><span data-stu-id="f75ec-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f75ec-106">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="f75ec-106">When to implement</span></span>

<span data-ttu-id="f75ec-107">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="f75ec-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f75ec-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f75ec-108">Requirement</span></span> | <span data-ttu-id="f75ec-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f75ec-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="f75ec-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="f75ec-110">CLSID</span></span>      | <span data-ttu-id="f75ec-111">\_TRANSACTIONCONTEXT CLSID</span><span class="sxs-lookup"><span data-stu-id="f75ec-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="f75ec-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="f75ec-112">ProgID</span></span>     | <span data-ttu-id="f75ec-113">L "TxCTx. TransactionContext"</span><span class="sxs-lookup"><span data-stu-id="f75ec-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="f75ec-114">Interfacce</span><span class="sxs-lookup"><span data-stu-id="f75ec-114">Interfaces</span></span> | [<span data-ttu-id="f75ec-115">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="f75ec-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="f75ec-116">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f75ec-116">When to use</span></span>

<span data-ttu-id="f75ec-117">Un client non transazionale utilizza questa classe per avviare una transazione.</span><span class="sxs-lookup"><span data-stu-id="f75ec-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="f75ec-118">Utilizzando i metodi di questa classe, il client può chiamare oggetti COM aggiuntivi che, se configurati per partecipare a una transazione, vengono eseguiti all'interno del limite della transazione dell'oggetto del contesto di transazione.</span><span class="sxs-lookup"><span data-stu-id="f75ec-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="f75ec-119">In base alla logica di business, il client può eseguire in modo esplicito il commit o l'interruzione della transazione.</span><span class="sxs-lookup"><span data-stu-id="f75ec-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="f75ec-120">La classe **TransactionContext** limita il riutilizzo della logica di business che guida la transazione.</span><span class="sxs-lookup"><span data-stu-id="f75ec-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="f75ec-121">Per questo motivo, è consigliabile usare sporadicamente gli oggetti di cui è stata creata un'istanza dalla classe **TransactionContext** .</span><span class="sxs-lookup"><span data-stu-id="f75ec-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="f75ec-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f75ec-122">Remarks</span></span>

<span data-ttu-id="f75ec-123">Per creare questo oggetto, chiamare [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="f75ec-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="f75ec-124">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="f75ec-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="f75ec-125">Un oggetto TransactionContext può essere dichiarato con "COMSVCSLib. TransactionContext" come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="f75ec-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="f75ec-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f75ec-126">Requirements</span></span>



| <span data-ttu-id="f75ec-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f75ec-127">Requirement</span></span> | <span data-ttu-id="f75ec-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f75ec-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f75ec-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f75ec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f75ec-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f75ec-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f75ec-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f75ec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f75ec-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f75ec-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f75ec-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f75ec-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f75ec-134"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f75ec-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f75ec-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f75ec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75ec-136">Configurazione di transazioni</span><span class="sxs-lookup"><span data-stu-id="f75ec-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="f75ec-137">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="f75ec-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="f75ec-138">**TransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="f75ec-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 




