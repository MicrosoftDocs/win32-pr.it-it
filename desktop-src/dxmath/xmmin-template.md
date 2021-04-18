---
description: Confronta due istanze di tipi di dati numerici o due istanze di un oggetto che supporta un overload di < e restituisce il più piccolo tra le due istanze. Il tipo di dati degli argomenti e il valore restituito sono gli stessi.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Modello XMMin (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324060"
---
# <a name="xmmin-template"></a><span data-ttu-id="c6012-104">Modello XMMin</span><span class="sxs-lookup"><span data-stu-id="c6012-104">XMMin template</span></span>

<span data-ttu-id="c6012-105">Confronta due istanze di tipi di dati numerici o due istanze di un oggetto che supporta un overload di < e restituisce il più piccolo tra le due istanze.</span><span class="sxs-lookup"><span data-stu-id="c6012-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the smaller one of the two instances.</span></span> <span data-ttu-id="c6012-106">Il tipo di dati degli argomenti e il valore restituito sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="c6012-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6012-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6012-107">Syntax</span></span>

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="c6012-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6012-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6012-109"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="c6012-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="c6012-110">\[in \] specifica il primo di due oggetti.</span><span class="sxs-lookup"><span data-stu-id="c6012-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="c6012-111"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="c6012-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="c6012-112">\[in \] specifica i due di due oggetti.</span><span class="sxs-lookup"><span data-stu-id="c6012-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6012-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6012-113">Return Value</span></span>

<span data-ttu-id="c6012-114">Restituisce il più piccolo dei due oggetti di input.</span><span class="sxs-lookup"><span data-stu-id="c6012-114">Returns the smaller of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6012-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6012-115">Remarks</span></span>

<span data-ttu-id="c6012-116">`XMMin` è un modello e il tipo T viene specificato quando viene creata un'istanza del modello.</span><span class="sxs-lookup"><span data-stu-id="c6012-116">`XMMin` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="c6012-117">Il `XMMin` modello è una novità di DirectXMath e non è disponibile per XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="c6012-117">The `XMMin` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="c6012-118">`XMMin` è disponibile come macro in XNAMath 2. x.</span><span class="sxs-lookup"><span data-stu-id="c6012-118">`XMMin` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6012-119">Utilizzare idealmente std:: min anziché `XMMin` .</span><span class="sxs-lookup"><span data-stu-id="c6012-119">Ideally use std::min instead of `XMMin`.</span></span> <span data-ttu-id="c6012-120">Per evitare conflitti con le intestazioni di Windows con std:: min, è necessario \# definire NOMINMAX prima di includere le intestazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="c6012-120">To avoid conflicts with Windows headers with std::min, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="c6012-121">**Spazio dei nomi**: usare DirectX</span><span class="sxs-lookup"><span data-stu-id="c6012-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="c6012-122">Requisiti della piattaforma</span><span class="sxs-lookup"><span data-stu-id="c6012-122">Platform Requirements</span></span>

<span data-ttu-id="c6012-123">Microsoft Visual Studio 2010 o Microsoft Visual Studio 2012 con la Windows SDK per Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c6012-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="c6012-124">Supportato per le app desktop Win32, le app di Windows Store e le app Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="c6012-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6012-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6012-125">Requirements</span></span>



| <span data-ttu-id="c6012-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6012-126">Requirement</span></span> | <span data-ttu-id="c6012-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c6012-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6012-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6012-128">Header</span></span><br/> | <dl> <span data-ttu-id="c6012-129"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6012-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6012-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6012-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6012-131">Funzioni del modello di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="c6012-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="c6012-132">**XMMax**</span><span class="sxs-lookup"><span data-stu-id="c6012-132">**XMMax**</span></span>](xmmax-template.md)
</dt> </dl>

 

 




