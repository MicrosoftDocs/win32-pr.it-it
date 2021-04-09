---
title: IFillLockBytes-implementazione
description: Il sistema fornisce un'implementazione di IFillLockBytes come parte dell'implementazione dei file composti.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955439"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="1ff4b-104">IFillLockBytes-implementazione</span><span class="sxs-lookup"><span data-stu-id="1ff4b-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="1ff4b-105">Il sistema fornisce un'implementazione di [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) come parte dell'implementazione dei file composti.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="1ff4b-106">Il download del codice può creare un'istanza di un oggetto file composto asincrono chiamando [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span><span class="sxs-lookup"><span data-stu-id="1ff4b-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="1ff4b-107">Il download del codice può anche creare un'istanza di un oggetto wrapper della matrice di byte asincrona su un file o una matrice di byte esistente chiamando la funzione [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) o [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="1ff4b-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1ff4b-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1ff4b-108">When to Use</span></span>

<span data-ttu-id="1ff4b-109">Attualmente, i moniker URL sono gli unici utenti dell'implementazione di archiviazione asincrona COM.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff4b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ff4b-110">Remarks</span></span>

<span data-ttu-id="1ff4b-111">Di seguito sono riportati i quattro metodi dell'implementazione di [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .</span><span class="sxs-lookup"><span data-stu-id="1ff4b-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="1ff4b-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes:: FillAppend**</span><span class="sxs-lookup"><span data-stu-id="1ff4b-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="1ff4b-113">Scrive un nuovo blocco di byte alla fine di una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="1ff4b-114">La dimensione del blocco viene specificata come parametro per [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span><span class="sxs-lookup"><span data-stu-id="1ff4b-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="1ff4b-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes:: FillAt**</span><span class="sxs-lookup"><span data-stu-id="1ff4b-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="1ff4b-116">Scrive un nuovo blocco di dati in una posizione specificata nella matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="1ff4b-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes:: SetFillSize**</span><span class="sxs-lookup"><span data-stu-id="1ff4b-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="1ff4b-118">Imposta la dimensione della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-118">Sets the size of the byte array.</span></span> <span data-ttu-id="1ff4b-119">Restituisce E \_ non vengono eseguite chiamate a [**ILockBytes:: ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) che tentano di accedere ai dati oltre il limite massimo specificato dal metodo.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="1ff4b-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes:: terminate**</span><span class="sxs-lookup"><span data-stu-id="1ff4b-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="1ff4b-121">Informa la matrice di byte che un download è stato terminato, con esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="1ff4b-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




