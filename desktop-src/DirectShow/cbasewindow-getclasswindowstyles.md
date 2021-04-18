---
description: Il metodo GetClassWindowStyles recupera gli stili della classe e gli stili della finestra.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Metodo CBaseWindow. GetClassWindowStyles (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327946"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="ab936-103">CBaseWindow. GetClassWindowStyles, metodo</span><span class="sxs-lookup"><span data-stu-id="ab936-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="ab936-104">Il `GetClassWindowStyles` metodo recupera gli stili della classe e gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="ab936-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab936-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab936-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="ab936-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab936-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab936-107">*pClassStyles*</span><span class="sxs-lookup"><span data-stu-id="ab936-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="ab936-108">Puntatore a una variabile che riceve gli stili della classe.</span><span class="sxs-lookup"><span data-stu-id="ab936-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="ab936-109">*pWindowStyles*</span><span class="sxs-lookup"><span data-stu-id="ab936-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="ab936-110">Puntatore a una variabile che riceve gli stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="ab936-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="ab936-111">*pWindowStylesEx*</span><span class="sxs-lookup"><span data-stu-id="ab936-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="ab936-112">Puntatore a una variabile che riceve gli stili della finestra estesa.</span><span class="sxs-lookup"><span data-stu-id="ab936-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab936-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab936-113">Return value</span></span>

<span data-ttu-id="ab936-114">Restituisce una stringa di testo statica che contiene il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="ab936-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab936-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab936-115">Remarks</span></span>

<span data-ttu-id="ab936-116">Il metodo [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chiama questo metodo per recuperare gli stili della classe e gli stili della finestra della finestra.</span><span class="sxs-lookup"><span data-stu-id="ab936-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="ab936-117">Questo metodo è virtuale puro; la classe derivata deve implementarla.</span><span class="sxs-lookup"><span data-stu-id="ab936-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="ab936-118">Nell'esempio seguente viene illustrata una possibile implementazione:</span><span class="sxs-lookup"><span data-stu-id="ab936-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="ab936-119">L'oggetto usa lo stile della classe per il membro **lpszClassName** di una struttura WNDCLASS, che passa alla funzione **registerClass** .</span><span class="sxs-lookup"><span data-stu-id="ab936-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="ab936-120">L'oggetto utilizza gli stili della finestra per i parametri *dwExStyle* e *DwStyle* della funzione **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="ab936-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="ab936-121">Per ulteriori informazioni, vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ab936-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab936-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab936-122">Requirements</span></span>



| <span data-ttu-id="ab936-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab936-123">Requirement</span></span> | <span data-ttu-id="ab936-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ab936-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab936-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab936-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ab936-126"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab936-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab936-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab936-127">Library</span></span><br/> | <dl> <span data-ttu-id="ab936-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab936-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab936-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab936-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab936-130">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="ab936-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




