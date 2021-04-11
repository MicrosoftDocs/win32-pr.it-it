---
description: Imposta una funzione di callback da utilizzare durante il riconoscimento della riga.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: SetLineRecoCallback (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232090"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="c41ca-103">SetLineRecoCallback (funzione)</span><span class="sxs-lookup"><span data-stu-id="c41ca-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="c41ca-104">Imposta una funzione di callback da utilizzare durante il riconoscimento della riga.</span><span class="sxs-lookup"><span data-stu-id="c41ca-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="c41ca-105">Questa funzione helper non è progettata per essere utilizzata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c41ca-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41ca-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c41ca-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="c41ca-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c41ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41ca-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c41ca-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41ca-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c41ca-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c41ca-110">*PFN*</span><span class="sxs-lookup"><span data-stu-id="c41ca-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="c41ca-111">Puntatore a una funzione che viene chiamata quando si verifica il riconoscimento in [**InkDivider**](inkdivider-class.md) passato.</span><span class="sxs-lookup"><span data-stu-id="c41ca-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41ca-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c41ca-112">Return value</span></span>

<span data-ttu-id="c41ca-113">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c41ca-113">This function can return one of these values.</span></span>



| <span data-ttu-id="c41ca-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c41ca-114">Return code</span></span>                                                                                  | <span data-ttu-id="c41ca-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c41ca-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c41ca-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c41ca-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c41ca-117">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="c41ca-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="c41ca-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c41ca-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c41ca-119">Il parametro *pDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c41ca-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c41ca-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c41ca-120">Remarks</span></span>

<span data-ttu-id="c41ca-121">Di seguito è riportata la sintassi per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="c41ca-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="c41ca-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c41ca-122">Requirements</span></span>



| <span data-ttu-id="c41ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c41ca-123">Requirement</span></span> | <span data-ttu-id="c41ca-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c41ca-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c41ca-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c41ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c41ca-126">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c41ca-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c41ca-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c41ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c41ca-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c41ca-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c41ca-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c41ca-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c41ca-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c41ca-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




