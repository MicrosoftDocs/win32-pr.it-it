---
title: Metodo IDCompositionMatrixTransform sematrixelement (int, int, IDCompositionAnimation)
description: Aggiunge un'animazione al valore di un elemento della matrice di questa trasformazione 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Metodo sematrixelement DirectComposition
- Metodo sematrixelement DirectComposition, interfaccia IDCompositionMatrixTransform
- Interfaccia IDCompositionMatrixTransform DirectComposition, metodo sematrixelement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399458"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="301cb-106">Metodo IDCompositionMatrixTransform:: sematrixelement (int, int, IDCompositionAnimation \* )</span><span class="sxs-lookup"><span data-stu-id="301cb-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="301cb-107">Aggiunge un'animazione al valore di un elemento della matrice di questa trasformazione 2D.</span><span class="sxs-lookup"><span data-stu-id="301cb-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="301cb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="301cb-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="301cb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="301cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301cb-110">*riga* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="301cb-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="301cb-111">Indice di riga dell'elemento da modificare.</span><span class="sxs-lookup"><span data-stu-id="301cb-111">The row index of the element to change.</span></span> <span data-ttu-id="301cb-112">Questo valore deve essere compreso tra 0 e 2 inclusi.</span><span class="sxs-lookup"><span data-stu-id="301cb-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="301cb-113">*colonna* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="301cb-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="301cb-114">Indice di colonna dell'elemento da modificare.</span><span class="sxs-lookup"><span data-stu-id="301cb-114">The column index of the element to change.</span></span> <span data-ttu-id="301cb-115">Questo valore deve essere compreso tra 0 e 1, inclusi.</span><span class="sxs-lookup"><span data-stu-id="301cb-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="301cb-116">*animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="301cb-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="301cb-117">Animazione che rappresenta il modo in cui il valore dell'elemento specificato viene modificato nel tempo.</span><span class="sxs-lookup"><span data-stu-id="301cb-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="301cb-118">Questo parametro non può essere NULL.</span><span class="sxs-lookup"><span data-stu-id="301cb-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301cb-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="301cb-119">Return value</span></span>

<span data-ttu-id="301cb-120">Se la funzione ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="301cb-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="301cb-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="301cb-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="301cb-122">Per un elenco di codici di errore, vedere [codici di errore DirectComposition](directcomposition-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="301cb-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="301cb-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="301cb-123">Remarks</span></span>

<span data-ttu-id="301cb-124">Questo metodo crea una copia dell'animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="301cb-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="301cb-125">Se l'oggetto a cui fa riferimento il parametro *Animation* viene modificato dopo la chiamata a questo metodo, la modifica non influisce sull'elemento a meno che questo metodo non venga chiamato nuovamente.</span><span class="sxs-lookup"><span data-stu-id="301cb-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="301cb-126">Se l'elemento è stato precedentemente animato, la chiamata a questo metodo sostituisce l'animazione precedente con la nuova animazione.</span><span class="sxs-lookup"><span data-stu-id="301cb-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="301cb-127">Questo metodo ha esito negativo se l' *animazione* è un puntatore non valido o se non è stato creato dalla stessa interfaccia [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) della trasformazione interessata.</span><span class="sxs-lookup"><span data-stu-id="301cb-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="301cb-128">L'interfaccia non può essere un'implementazione personalizzata. con questo metodo è possibile usare solo le interfacce create da Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="301cb-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="301cb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="301cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301cb-130">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="301cb-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 