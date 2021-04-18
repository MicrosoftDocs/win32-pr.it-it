---
description: "Rilascia l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview:: GetNewPreview. Rilascia anche il filtro di elaborazione delle immagini."
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'Metodo IWiaPreview:: Clear (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307359"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="4ac18-104">Metodo IWiaPreview:: Clear</span><span class="sxs-lookup"><span data-stu-id="4ac18-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="4ac18-105">Rilascia l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="4ac18-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="4ac18-106">Rilascia anche il filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="4ac18-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac18-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ac18-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="4ac18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ac18-108">Parameters</span></span>

<span data-ttu-id="4ac18-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4ac18-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ac18-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ac18-110">Return value</span></span>

<span data-ttu-id="4ac18-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="4ac18-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ac18-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ac18-112">Remarks</span></span>

<span data-ttu-id="4ac18-113">In **IWiaPreview:: Clear** il componente Windows Image Acquisition (WIA) 2,0 Preview rilascia tutti i puntatori di interfaccia archiviati.</span><span class="sxs-lookup"><span data-stu-id="4ac18-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="4ac18-114">Il componente WIA 2,0 Preview mantiene i riferimenti a *pWiaItem2* e *PWiaTransferCallback* passati in [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="4ac18-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="4ac18-115">Per essere precisi, il componente WIA 2,0 Preview mantiene un riferimento a *pWiaItem2* e al filtro di elaborazione delle immagini del driver, che a sua volta mantiene un riferimento a *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="4ac18-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="4ac18-116">In **IWiaPreview:: Clear**, il componente WIA 2,0 Preview rilascia anche il riferimento a *pWiaItem2* e al filtro di elaborazione dell'immagine, che a sua volta rilascia il riferimento a *pWiaTransferCallback*.</span><span class="sxs-lookup"><span data-stu-id="4ac18-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="4ac18-117">Il componente WIA 2,0 Preview Elimina l'immagine memorizzata nella cache e non filtrata che archivia internamente.</span><span class="sxs-lookup"><span data-stu-id="4ac18-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac18-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ac18-118">Requirements</span></span>



| <span data-ttu-id="4ac18-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ac18-119">Requirement</span></span> | <span data-ttu-id="4ac18-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4ac18-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac18-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ac18-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac18-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ac18-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ac18-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ac18-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac18-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ac18-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4ac18-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ac18-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ac18-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac18-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ac18-127">IDL</span><span class="sxs-lookup"><span data-stu-id="4ac18-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ac18-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ac18-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




