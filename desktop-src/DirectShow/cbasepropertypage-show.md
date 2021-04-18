---
description: 'Il metodo Show Visualizza o nasconde la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage:: Show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: Metodo CBasePropertyPage. Show (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330407"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="57da7-104">CBasePropertyPage. Show (metodo)</span><span class="sxs-lookup"><span data-stu-id="57da7-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="57da7-105">Il `Show` Metodo Visualizza o nasconde la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="57da7-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="57da7-106">Questo metodo implementa il metodo [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="57da7-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57da7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57da7-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="57da7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="57da7-108">Parameters</span></span>

<span data-ttu-id="57da7-109">*nCmdShow*</span><span class="sxs-lookup"><span data-stu-id="57da7-109">*nCmdShow*</span></span>

<span data-ttu-id="57da7-110">Tipo: **[uint](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57da7-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57da7-111">Valore che specifica se visualizzare o nascondere la finestra.</span><span class="sxs-lookup"><span data-stu-id="57da7-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="57da7-112">Per ulteriori informazioni, vedere il metodo [IPropertyPage:: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="57da7-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="57da7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57da7-113">Return value</span></span>

<span data-ttu-id="57da7-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57da7-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="57da7-115">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="57da7-115">Possible values include the following.</span></span>

| <span data-ttu-id="57da7-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="57da7-116">Return code</span></span>                                                                                  | <span data-ttu-id="57da7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57da7-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="57da7-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="57da7-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="57da7-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="57da7-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="57da7-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="57da7-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="57da7-121">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="57da7-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="57da7-122"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="57da7-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="57da7-123">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="57da7-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="57da7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57da7-124">Requirements</span></span>

| <span data-ttu-id="57da7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="57da7-125">Requirement</span></span> | <span data-ttu-id="57da7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="57da7-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57da7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57da7-127">Header</span></span>  | <dl> <span data-ttu-id="57da7-128"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57da7-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="57da7-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="57da7-129">Library</span></span> | <dl> <span data-ttu-id="57da7-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="57da7-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="57da7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57da7-131">See also</span></span>

[<span data-ttu-id="57da7-132">Classe CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="57da7-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
