---
title: Funzione type size (D2d1helper. h)
description: Crea una struttura di dimensioni che archivia la larghezza e l'altezza usando il tipo di dati specificato.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Funzione tipo dimensione Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476258"
---
# <a name="sizetype-function"></a><span data-ttu-id="a76b1-104">Size ( <Type> funzione)</span><span class="sxs-lookup"><span data-stu-id="a76b1-104">Size<Type> Function</span></span>

<span data-ttu-id="a76b1-105">Crea una struttura di dimensioni che archivia la larghezza e l'altezza usando il tipo di dati specificato.</span><span class="sxs-lookup"><span data-stu-id="a76b1-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="a76b1-106">Parametri di template</span><span class="sxs-lookup"><span data-stu-id="a76b1-106">Template Parameters</span></span>



| <span data-ttu-id="a76b1-107">Parametro</span><span class="sxs-lookup"><span data-stu-id="a76b1-107">Parameter</span></span> | <span data-ttu-id="a76b1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a76b1-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76b1-109">Type</span><span class="sxs-lookup"><span data-stu-id="a76b1-109">Type</span></span>      | <span data-ttu-id="a76b1-110">Tipo di dati utilizzato per archiviare la larghezza e l'altezza delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a76b1-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="a76b1-111">I valori possibili sono FLOAT e UINT32.</span><span class="sxs-lookup"><span data-stu-id="a76b1-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a76b1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a76b1-112">Parameters</span></span>



| <span data-ttu-id="a76b1-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="a76b1-113">Parameter</span></span> | <span data-ttu-id="a76b1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a76b1-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="a76b1-115">width</span><span class="sxs-lookup"><span data-stu-id="a76b1-115">width</span></span>     | <span data-ttu-id="a76b1-116">Larghezza della dimensione.</span><span class="sxs-lookup"><span data-stu-id="a76b1-116">The size's width.</span></span>  |
| <span data-ttu-id="a76b1-117">altezza</span><span class="sxs-lookup"><span data-stu-id="a76b1-117">height</span></span>    | <span data-ttu-id="a76b1-118">Altezza della dimensione.</span><span class="sxs-lookup"><span data-stu-id="a76b1-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="a76b1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a76b1-119">Return Value</span></span>

<span data-ttu-id="a76b1-120">Dimensioni che contengono la larghezza e l'altezza specificate.</span><span class="sxs-lookup"><span data-stu-id="a76b1-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="a76b1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a76b1-121">Requirements</span></span>



| <span data-ttu-id="a76b1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a76b1-122">Requirement</span></span> | <span data-ttu-id="a76b1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a76b1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76b1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a76b1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a76b1-125">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a76b1-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a76b1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a76b1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a76b1-127">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a76b1-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a76b1-128">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a76b1-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a76b1-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="a76b1-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="a76b1-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a76b1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a76b1-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="a76b1-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="a76b1-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a76b1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a76b1-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a76b1-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="a76b1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a76b1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a76b1-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a76b1-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





