---
description: Imposta la proprietà LineHeight sull'oggetto InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314902"
---
# <a name="setlineheight-function"></a><span data-ttu-id="7cc5e-103">SetLineHeight (funzione)</span><span class="sxs-lookup"><span data-stu-id="7cc5e-103">SetLineHeight function</span></span>

<span data-ttu-id="7cc5e-104">Imposta la proprietà [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) sull'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc5e-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="7cc5e-105">Questa funzione helper non è progettata per essere utilizzata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc5e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cc5e-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="7cc5e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cc5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cc5e-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cc5e-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc5e-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc5e-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="7cc5e-110">*lLineHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cc5e-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cc5e-111">Proprietà [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) dell'oggetto [**InkDivider**](inkdivider-class.md) , in unità HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cc5e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cc5e-112">Return value</span></span>

<span data-ttu-id="7cc5e-113">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-113">This function can return one of these values.</span></span>



| <span data-ttu-id="7cc5e-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7cc5e-114">Return code</span></span>                                                                                  | <span data-ttu-id="7cc5e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cc5e-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7cc5e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc5e-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7cc5e-117">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="7cc5e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc5e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7cc5e-119">Il parametro *pDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7cc5e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cc5e-120">Requirements</span></span>



| <span data-ttu-id="7cc5e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cc5e-121">Requirement</span></span> | <span data-ttu-id="7cc5e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7cc5e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc5e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cc5e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc5e-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7cc5e-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7cc5e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cc5e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc5e-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7cc5e-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="7cc5e-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7cc5e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cc5e-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cc5e-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
