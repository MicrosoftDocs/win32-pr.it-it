---
description: Recupera le informazioni di analisi dall'oggetto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524402"
---
# <a name="calldivide-function"></a><span data-ttu-id="3f3da-103">CallDivide (funzione)</span><span class="sxs-lookup"><span data-stu-id="3f3da-103">CallDivide function</span></span>

<span data-ttu-id="3f3da-104">Recupera le informazioni di analisi dall'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3da-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="3f3da-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3da-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3da-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f3da-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="3f3da-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f3da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f3da-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3da-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-110">*pWordSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-111">Dimensione della parola restituita dall'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3da-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-112">*pLineSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-113">Dimensione della riga restituita dall'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3da-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-114">*pParagraphSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-115">Dimensioni del paragrafo restituito dall'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3da-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-116">*pDrawingSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-117">Dimensioni del disegno restituito dall'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3da-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-118">*pWordCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-119">Numero di parole restituite dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="3f3da-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-120">*pLineCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-121">Numero di righe restituite dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="3f3da-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="3f3da-122">*pParagraphCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f3da-123">Numero di paragrafi restituiti dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="3f3da-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f3da-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f3da-124">Return value</span></span>

<span data-ttu-id="3f3da-125">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3f3da-125">This function can return one of these values.</span></span>



| <span data-ttu-id="3f3da-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3f3da-126">Return code</span></span>                                                                                  | <span data-ttu-id="3f3da-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f3da-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="3f3da-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f3da-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3f3da-129">Funzione riuscito.</span><span class="sxs-lookup"><span data-stu-id="3f3da-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="3f3da-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3f3da-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3f3da-131">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="3f3da-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f3da-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f3da-132">Requirements</span></span>



| <span data-ttu-id="3f3da-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f3da-133">Requirement</span></span> | <span data-ttu-id="3f3da-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3f3da-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3da-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f3da-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3da-136">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3f3da-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3f3da-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f3da-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3da-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3f3da-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="3f3da-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f3da-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f3da-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f3da-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




