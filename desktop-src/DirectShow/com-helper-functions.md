---
description: Queste funzioni forniscono il supporto per l'implementazione dell'interfaccia IUnknown in DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funzioni helper COM (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333434"
---
# <a name="com-helper-functions"></a><span data-ttu-id="4a9a6-103">Funzioni helper COM</span><span class="sxs-lookup"><span data-stu-id="4a9a6-103">COM Helper Functions</span></span>

<span data-ttu-id="4a9a6-104">Queste funzioni forniscono il supporto per l'implementazione dell'interfaccia **IUnknown** in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4a9a6-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="4a9a6-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="4a9a6-105">Function</span></span>                                               | <span data-ttu-id="4a9a6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a9a6-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="4a9a6-107">**DICHIARARE \_ IUnknown**</span><span class="sxs-lookup"><span data-stu-id="4a9a6-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="4a9a6-108">Dichiara i tre metodi dell'interfaccia di base per una nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4a9a6-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="4a9a6-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="4a9a6-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="4a9a6-110">Recupera un puntatore di interfaccia al client richiesto.</span><span class="sxs-lookup"><span data-stu-id="4a9a6-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="4a9a6-111">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="4a9a6-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="4a9a6-112">Versione non delegata dell'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="4a9a6-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="4a9a6-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="4a9a6-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="4a9a6-114">Carica la DLL di automazione (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="4a9a6-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="4a9a6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a9a6-115">Requirements</span></span>



| <span data-ttu-id="4a9a6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a9a6-116">Requirement</span></span> | <span data-ttu-id="4a9a6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4a9a6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9a6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a9a6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4a9a6-119"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a9a6-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a9a6-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a9a6-120">Library</span></span><br/> | <dl> <span data-ttu-id="4a9a6-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4a9a6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a9a6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a9a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9a6-123">Funzioni di utilità</span><span class="sxs-lookup"><span data-stu-id="4a9a6-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




