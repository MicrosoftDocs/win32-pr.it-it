---
description: Recupera i risultati dell'analisi dall'oggetto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127819"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="38ae9-103">CallDivideResults (funzione)</span><span class="sxs-lookup"><span data-stu-id="38ae9-103">CallDivideResults function</span></span>

<span data-ttu-id="38ae9-104">Recupera i risultati dell'analisi dall'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="38ae9-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="38ae9-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38ae9-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ae9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38ae9-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="38ae9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="38ae9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ae9-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="38ae9-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-110">*aWordStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-111">Matrice di identificatori associati alla parola passata alla classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="38ae9-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-112">*aLineStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-113">Matrice di proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati alla riga passata alla classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="38ae9-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-114">*aParagraphStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-115">Matrice delle proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati al paragrafo dalla classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="38ae9-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-116">*aDrawingStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-117">Matrice di proprietà [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) per gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) associati al disegno dalla classe [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="38ae9-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-118">*pastrWords* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-119">Matrice di parole restituita dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="38ae9-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-120">*pastrLines* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-121">Matrice di righe restituite dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="38ae9-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-122">*pastrParagraphs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-123">Matrice di paragrafi restituiti dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="38ae9-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-124">*aWordRotationCenterX* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-125">Matrice dei punti centrali delle parole lungo l'asse x dall'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="38ae9-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-126">*aWordRotationCenterY* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-127">Matrice dei punti centrali delle parole lungo l'asse y dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="38ae9-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-128">*aWordAngle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-129">Matrice contenente gli angoli in base ai quali ruotare le parole per ottenere risultati di analisi ottimali.</span><span class="sxs-lookup"><span data-stu-id="38ae9-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-130">*aLineRotationCenterX* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-131">Matrice contenente i punti centrali delle linee lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="38ae9-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-132">*aLineRotationCenterY* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-133">Matrice contenente i punti centrali delle linee lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="38ae9-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="38ae9-134">*aLineAngle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ae9-135">Matrice contenente gli angoli in base ai quali ruotare le linee per ottenere risultati di analisi ottimali.</span><span class="sxs-lookup"><span data-stu-id="38ae9-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ae9-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38ae9-136">Return value</span></span>

<span data-ttu-id="38ae9-137">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="38ae9-137">This function can return one of these values.</span></span>



| <span data-ttu-id="38ae9-138">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="38ae9-138">Return code</span></span>                                                                                   | <span data-ttu-id="38ae9-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38ae9-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="38ae9-140"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38ae9-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="38ae9-141">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="38ae9-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="38ae9-142"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="38ae9-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="38ae9-143">Il parametro *hDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="38ae9-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="38ae9-144"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="38ae9-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="38ae9-145">Non è stato possibile allocare memoria sufficiente per archiviare i risultati.</span><span class="sxs-lookup"><span data-stu-id="38ae9-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38ae9-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="38ae9-146">Remarks</span></span>

<span data-ttu-id="38ae9-147">Per evitare perdite di memoria, è necessario rilasciare le risorse per *pastrWords*, *pastrLines* e *pastrParagraphs*.</span><span class="sxs-lookup"><span data-stu-id="38ae9-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ae9-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38ae9-148">Requirements</span></span>



| <span data-ttu-id="38ae9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ae9-149">Requirement</span></span> | <span data-ttu-id="38ae9-150">Valore</span><span class="sxs-lookup"><span data-stu-id="38ae9-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38ae9-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38ae9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="38ae9-152">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="38ae9-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="38ae9-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38ae9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="38ae9-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="38ae9-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="38ae9-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="38ae9-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="38ae9-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38ae9-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




