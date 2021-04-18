---
description: 'Il metodo Activate crea la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage:: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Metodo CBasePropertyPage. Activate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328077"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="34626-104">Metodo CBasePropertyPage. Activate</span><span class="sxs-lookup"><span data-stu-id="34626-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="34626-105">Il `Activate` metodo crea la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="34626-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="34626-106">Questo metodo implementa il metodo **IPropertyPage:: Activate** .</span><span class="sxs-lookup"><span data-stu-id="34626-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34626-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34626-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="34626-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="34626-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34626-109">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="34626-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="34626-110">Handle per la finestra padre della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="34626-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="34626-111">*prect*</span><span class="sxs-lookup"><span data-stu-id="34626-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="34626-112">Puntatore a una struttura **Rect** che contiene informazioni sul posizionamento per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="34626-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="34626-113">*fModal*</span><span class="sxs-lookup"><span data-stu-id="34626-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="34626-114">Valore booleano che indica se il frame della finestra di dialogo è modale (**true**) o non modale (**false**).</span><span class="sxs-lookup"><span data-stu-id="34626-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34626-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34626-115">Return value</span></span>

<span data-ttu-id="34626-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34626-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="34626-117">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="34626-117">Possible values include the following.</span></span>



| <span data-ttu-id="34626-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="34626-118">Return code</span></span>                                                                                   | <span data-ttu-id="34626-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34626-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="34626-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34626-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="34626-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="34626-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="34626-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="34626-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="34626-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="34626-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="34626-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="34626-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="34626-125">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="34626-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="34626-126"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="34626-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="34626-127">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="34626-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="34626-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34626-128">Requirements</span></span>



| <span data-ttu-id="34626-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="34626-129">Requirement</span></span> | <span data-ttu-id="34626-130">Valore</span><span class="sxs-lookup"><span data-stu-id="34626-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34626-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34626-131">Header</span></span><br/>  | <dl> <span data-ttu-id="34626-132"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34626-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="34626-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="34626-133">Library</span></span><br/> | <dl> <span data-ttu-id="34626-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34626-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34626-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34626-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34626-136">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="34626-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="34626-137">**CBasePropertyPage:: OnActivate**</span><span class="sxs-lookup"><span data-stu-id="34626-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




