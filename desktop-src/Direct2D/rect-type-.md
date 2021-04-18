---
title: Funzione di tipo Rect (D2d1helper. h)
description: Crea una struttura Rectangle che archivia le coordinate usando il tipo di dati specificato.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Funzione di tipo Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302032"
---
# <a name="recttype-function"></a><span data-ttu-id="caa55-104">Rect ( <Type> funzione)</span><span class="sxs-lookup"><span data-stu-id="caa55-104">Rect<Type> Function</span></span>

<span data-ttu-id="caa55-105">Crea una struttura Rectangle che archivia le coordinate usando il tipo di dati specificato.</span><span class="sxs-lookup"><span data-stu-id="caa55-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="caa55-106">Parametri di template</span><span class="sxs-lookup"><span data-stu-id="caa55-106">Template Parameters</span></span>



| <span data-ttu-id="caa55-107">Parametro</span><span class="sxs-lookup"><span data-stu-id="caa55-107">Parameter</span></span> | <span data-ttu-id="caa55-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caa55-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caa55-109">Type</span><span class="sxs-lookup"><span data-stu-id="caa55-109">Type</span></span>      | <span data-ttu-id="caa55-110">Tipo di dati utilizzato per archiviare le dimensioni del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="caa55-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="caa55-111">I valori possibili sono **float** e **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="caa55-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="caa55-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="caa55-112">Parameters</span></span>



| <span data-ttu-id="caa55-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="caa55-113">Parameter</span></span> | <span data-ttu-id="caa55-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caa55-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="caa55-115">sinistro</span><span class="sxs-lookup"><span data-stu-id="caa55-115">left</span></span>      | <span data-ttu-id="caa55-116">Coordinata x dell'angolo superiore sinistro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="caa55-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="caa55-117">top</span><span class="sxs-lookup"><span data-stu-id="caa55-117">top</span></span>       | <span data-ttu-id="caa55-118">Coordinata y dell'angolo superiore sinistro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="caa55-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="caa55-119">right</span><span class="sxs-lookup"><span data-stu-id="caa55-119">right</span></span>     | <span data-ttu-id="caa55-120">Coordinata x dell'angolo inferiore destro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="caa55-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="caa55-121">bottom</span><span class="sxs-lookup"><span data-stu-id="caa55-121">bottom</span></span>    | <span data-ttu-id="caa55-122">Coordinata y dell'angolo inferiore destro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="caa55-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="caa55-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caa55-123">Return Value</span></span>

<span data-ttu-id="caa55-124">Struttura Rectangle che contiene le coordinate specificate.</span><span class="sxs-lookup"><span data-stu-id="caa55-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa55-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caa55-125">Requirements</span></span>



| <span data-ttu-id="caa55-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="caa55-126">Requirement</span></span> | <span data-ttu-id="caa55-127">Valore</span><span class="sxs-lookup"><span data-stu-id="caa55-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caa55-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caa55-128">Minimum supported client</span></span><br/> | <span data-ttu-id="caa55-129">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="caa55-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="caa55-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caa55-130">Minimum supported server</span></span><br/> | <span data-ttu-id="caa55-131">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="caa55-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="caa55-132">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caa55-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="caa55-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="caa55-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="caa55-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="caa55-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa55-135"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="caa55-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="caa55-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="caa55-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="caa55-137"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caa55-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="caa55-138">DLL</span><span class="sxs-lookup"><span data-stu-id="caa55-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caa55-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caa55-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





