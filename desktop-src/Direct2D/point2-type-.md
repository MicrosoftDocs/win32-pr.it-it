---
title: Funzione di tipo point2 (D2d1helper. h)
description: Crea un punto che archivia le coordinate usando il tipo di dati specificato.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2 funzione di tipo Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302033"
---
# <a name="point2type-function"></a><span data-ttu-id="4013c-104">Point2 ( <Type> funzione)</span><span class="sxs-lookup"><span data-stu-id="4013c-104">Point2<Type> Function</span></span>

<span data-ttu-id="4013c-105">Crea un punto che archivia le coordinate usando il tipo di dati specificato.</span><span class="sxs-lookup"><span data-stu-id="4013c-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="4013c-106">Parametri di template</span><span class="sxs-lookup"><span data-stu-id="4013c-106">Template Parameters</span></span>



| <span data-ttu-id="4013c-107">Parametro</span><span class="sxs-lookup"><span data-stu-id="4013c-107">Parameter</span></span> | <span data-ttu-id="4013c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4013c-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4013c-109">Type</span><span class="sxs-lookup"><span data-stu-id="4013c-109">Type</span></span>      | <span data-ttu-id="4013c-110">Tipo di dati utilizzato per archiviare la coordinata x e la coordinata y del punto.</span><span class="sxs-lookup"><span data-stu-id="4013c-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="4013c-111">I valori possibili sono FLOAT e UINT32.</span><span class="sxs-lookup"><span data-stu-id="4013c-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="4013c-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4013c-112">Parameters</span></span>



| <span data-ttu-id="4013c-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="4013c-113">Parameter</span></span> | <span data-ttu-id="4013c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4013c-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="4013c-115">x</span><span class="sxs-lookup"><span data-stu-id="4013c-115">x</span></span>         | <span data-ttu-id="4013c-116">Coordinata x del punto.</span><span class="sxs-lookup"><span data-stu-id="4013c-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="4013c-117">y</span><span class="sxs-lookup"><span data-stu-id="4013c-117">y</span></span>         | <span data-ttu-id="4013c-118">Coordinata y del punto.</span><span class="sxs-lookup"><span data-stu-id="4013c-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="4013c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4013c-119">Return Value</span></span>

<span data-ttu-id="4013c-120">Punto che contiene la coordinata x e la coordinata y specificate.</span><span class="sxs-lookup"><span data-stu-id="4013c-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4013c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4013c-121">Requirements</span></span>



| <span data-ttu-id="4013c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4013c-122">Requirement</span></span> | <span data-ttu-id="4013c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4013c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4013c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4013c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4013c-125">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4013c-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="4013c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4013c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4013c-127">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4013c-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="4013c-128">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4013c-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4013c-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="4013c-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="4013c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4013c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4013c-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="4013c-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="4013c-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="4013c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="4013c-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4013c-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="4013c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4013c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4013c-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4013c-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





