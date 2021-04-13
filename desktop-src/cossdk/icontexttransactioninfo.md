---
description: Fornisce l'accesso alle proprietà dell'oggetto di contesto correlate alle transazioni.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interfaccia IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483437"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="cffea-103">Interfaccia IContextTransactionInfo</span><span class="sxs-lookup"><span data-stu-id="cffea-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="cffea-104">Fornisce l'accesso alle proprietà dell'oggetto di contesto correlate alle transazioni.</span><span class="sxs-lookup"><span data-stu-id="cffea-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="cffea-105">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="cffea-105">When to implement</span></span>

<span data-ttu-id="cffea-106">Non implementare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cffea-106">You should not implement this interface.</span></span> <span data-ttu-id="cffea-107">L'implementazione standard offre funzionalità complete.</span><span class="sxs-lookup"><span data-stu-id="cffea-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cffea-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="cffea-108">When to use</span></span>

<span data-ttu-id="cffea-109">Utilizzare questa interfaccia per accedere alle proprietà dell'oggetto di contesto correlate alle transazioni.</span><span class="sxs-lookup"><span data-stu-id="cffea-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="cffea-110">Membri</span><span class="sxs-lookup"><span data-stu-id="cffea-110">Members</span></span>

<span data-ttu-id="cffea-111">L'interfaccia **IContextTransactionInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cffea-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cffea-112">**IContextTransactionInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cffea-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="cffea-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="cffea-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cffea-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="cffea-114">Methods</span></span>

<span data-ttu-id="cffea-115">L'interfaccia **IContextTransactionInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cffea-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="cffea-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="cffea-116">Method</span></span>                                                                                         | <span data-ttu-id="cffea-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cffea-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cffea-118">**FetchTransaction**</span><span class="sxs-lookup"><span data-stu-id="cffea-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="cffea-119">Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.</span><span class="sxs-lookup"><span data-stu-id="cffea-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="cffea-120">**GetTxIsolationLevelAndTimeout**</span><span class="sxs-lookup"><span data-stu-id="cffea-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="cffea-121">Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto di transazione radice.</span><span class="sxs-lookup"><span data-stu-id="cffea-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="cffea-122">**RegisterTransactionProxy**</span><span class="sxs-lookup"><span data-stu-id="cffea-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="cffea-123">Associa un'implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) al contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="cffea-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="cffea-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cffea-124">Requirements</span></span>



| <span data-ttu-id="cffea-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cffea-125">Requirement</span></span> | <span data-ttu-id="cffea-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cffea-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cffea-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cffea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cffea-128">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cffea-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cffea-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cffea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cffea-130">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="cffea-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 

