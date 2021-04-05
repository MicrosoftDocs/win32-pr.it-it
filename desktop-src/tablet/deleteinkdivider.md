---
description: Elimina un oggetto InkDivider e rilascia le risorse associate.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884378"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="5267b-103">DeleteInkDivider (funzione)</span><span class="sxs-lookup"><span data-stu-id="5267b-103">DeleteInkDivider function</span></span>

<span data-ttu-id="5267b-104">Elimina un oggetto [**InkDivider**](inkdivider-class.md) e rilascia le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="5267b-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="5267b-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5267b-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5267b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5267b-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="5267b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5267b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5267b-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5267b-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5267b-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5267b-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5267b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5267b-110">Return value</span></span>

<span data-ttu-id="5267b-111">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5267b-111">This function can return one of these values.</span></span>



| <span data-ttu-id="5267b-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5267b-112">Return code</span></span>                                                                                  | <span data-ttu-id="5267b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5267b-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="5267b-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5267b-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5267b-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5267b-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="5267b-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5267b-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5267b-117">Il parametro *hDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="5267b-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5267b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5267b-118">Requirements</span></span>



| <span data-ttu-id="5267b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5267b-119">Requirement</span></span> | <span data-ttu-id="5267b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5267b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5267b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5267b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5267b-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5267b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5267b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5267b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5267b-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5267b-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="5267b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="5267b-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5267b-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5267b-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




