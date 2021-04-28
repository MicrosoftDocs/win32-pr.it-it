---
description: 'Costruttore CBaseWindow.CBaseWindow : metodo costruttore.'
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Costruttore CBaseWindow.CBaseWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095819"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="302d2-103">Costruttore CBaseWindow.CBaseWindow</span><span class="sxs-lookup"><span data-stu-id="302d2-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="302d2-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="302d2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="302d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="302d2-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="302d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="302d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="302d2-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="302d2-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="302d2-108">Valore booleano che specifica se recuperare il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="302d2-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="302d2-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="302d2-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="302d2-110">Valore booleano che specifica la [**variabile membro CBaseWindow::m \_ bDoPostToDestroy.**](cbasewindow-m-bdoposttodestroy.md)</span><span class="sxs-lookup"><span data-stu-id="302d2-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="302d2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="302d2-111">Remarks</span></span>

<span data-ttu-id="302d2-112">Dopo aver creato l'oggetto, chiamare il metodo [**CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) per creare la finestra.</span><span class="sxs-lookup"><span data-stu-id="302d2-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="302d2-113">**PrepareWindow** è un metodo virtuale.</span><span class="sxs-lookup"><span data-stu-id="302d2-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="302d2-114">Chiama [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), anche un metodo virtuale.</span><span class="sxs-lookup"><span data-stu-id="302d2-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="302d2-115">Questi metodi sono separati dal costruttore in modo che le classi derivate possano eseguirne l'override, se necessario.</span><span class="sxs-lookup"><span data-stu-id="302d2-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="302d2-116">Se il valore del *parametro bDoGetDC* è **TRUE,** l'oggetto recupera un handle per il contesto di dispositivo della finestra e lo archivia nella variabile membro `CBaseWindow` [**CBaseWindow::m \_ hdc.**](cbasewindow-m-hdc.md)</span><span class="sxs-lookup"><span data-stu-id="302d2-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="302d2-117">L'oggetto crea anche un controller di dominio di memoria compatibile, archiviato nella variabile membro [**CBaseWindow::m \_ MemoryDC.**](cbasewindow-m-memorydc.md)</span><span class="sxs-lookup"><span data-stu-id="302d2-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="302d2-118">Queste azioni si verificano **nel metodo InitialiseWindow.**</span><span class="sxs-lookup"><span data-stu-id="302d2-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="302d2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="302d2-119">Requirements</span></span>



| <span data-ttu-id="302d2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="302d2-120">Requirement</span></span> | <span data-ttu-id="302d2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="302d2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="302d2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="302d2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="302d2-123"><dt>Winutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="302d2-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="302d2-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="302d2-124">Library</span></span><br/> | <dl> <span data-ttu-id="302d2-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="302d2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="302d2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="302d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="302d2-127">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="302d2-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




