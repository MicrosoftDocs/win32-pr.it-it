---
description: Verifica se l'oggetto InkDivider può usare la classe InkRecognizerContext per analizzare le parole.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882457"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="56a7d-103">RecognizerContextSet (funzione)</span><span class="sxs-lookup"><span data-stu-id="56a7d-103">RecognizerContextSet function</span></span>

<span data-ttu-id="56a7d-104">Verifica se l'oggetto [**InkDivider**](inkdivider-class.md) può usare la classe [**InkRecognizerContext**](inkrecognizercontext-class.md) per analizzare le parole.</span><span class="sxs-lookup"><span data-stu-id="56a7d-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="56a7d-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56a7d-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a7d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56a7d-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="56a7d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="56a7d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a7d-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56a7d-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a7d-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="56a7d-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a7d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56a7d-110">Return value</span></span>

<span data-ttu-id="56a7d-111">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="56a7d-111">This function can return one of these values.</span></span>



| <span data-ttu-id="56a7d-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="56a7d-112">Return code</span></span>                                                                                  | <span data-ttu-id="56a7d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a7d-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="56a7d-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56a7d-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="56a7d-115">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="56a7d-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="56a7d-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="56a7d-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="56a7d-117">Il parametro *pDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="56a7d-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56a7d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56a7d-118">Requirements</span></span>



| <span data-ttu-id="56a7d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="56a7d-119">Requirement</span></span> | <span data-ttu-id="56a7d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="56a7d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56a7d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56a7d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56a7d-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="56a7d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="56a7d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56a7d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56a7d-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="56a7d-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="56a7d-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="56a7d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="56a7d-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a7d-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




