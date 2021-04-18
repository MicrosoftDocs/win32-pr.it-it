---
description: Recupera le proprietà ID per gli oggetti IInkStrokeDisp della parola, della riga, del paragrafo o del disegno corrispondente determinati dall'analisi dell'input penna.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305350"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="6aadf-103">CallDivideResultsStrokeIds (funzione)</span><span class="sxs-lookup"><span data-stu-id="6aadf-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="6aadf-104">Recupera le proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) della parola, della riga, del paragrafo o del disegno corrispondente determinati dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="6aadf-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="6aadf-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6aadf-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aadf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aadf-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="6aadf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aadf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aadf-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aadf-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aadf-109">Handle per l'oggetto [divisore](the-divider-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6aadf-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="6aadf-110">*\[ aWordStrokeIds \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="6aadf-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aadf-111">Matrice degli ID tratto dell'input penna nella parola.</span><span class="sxs-lookup"><span data-stu-id="6aadf-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="6aadf-112">*\[ aLineStrokeIds \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="6aadf-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aadf-113">Matrice degli ID tratto dell'input penna nella riga.</span><span class="sxs-lookup"><span data-stu-id="6aadf-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="6aadf-114">*\[ aParagraphStrokeIds \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="6aadf-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aadf-115">Matrice degli ID tratto dell'input penna nel paragrafo.</span><span class="sxs-lookup"><span data-stu-id="6aadf-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="6aadf-116">*\[ aDrawingStrokeIds \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="6aadf-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aadf-117">Matrice degli ID tratto dell'input penna nel disegno.</span><span class="sxs-lookup"><span data-stu-id="6aadf-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aadf-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aadf-118">Return value</span></span>

<span data-ttu-id="6aadf-119">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6aadf-119">This function can return one of these values.</span></span>



| <span data-ttu-id="6aadf-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6aadf-120">Return code</span></span>                                                                                  | <span data-ttu-id="6aadf-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6aadf-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="6aadf-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6aadf-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6aadf-123">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="6aadf-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="6aadf-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6aadf-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6aadf-125">Il parametro *hDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="6aadf-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6aadf-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aadf-126">Requirements</span></span>



| <span data-ttu-id="6aadf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aadf-127">Requirement</span></span> | <span data-ttu-id="6aadf-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6aadf-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6aadf-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aadf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6aadf-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6aadf-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6aadf-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aadf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6aadf-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6aadf-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6aadf-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="6aadf-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6aadf-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aadf-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




