---
description: 'Il metodo Move posiziona e ridimensiona la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage:: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Metodo CBasePropertyPage. Move (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329416"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="07f69-104">Metodo CBasePropertyPage. Move</span><span class="sxs-lookup"><span data-stu-id="07f69-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="07f69-105">Il `Move` Metodo posiziona e ridimensiona la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="07f69-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="07f69-106">Questo metodo implementa il metodo **IPropertyPage:: Move** .</span><span class="sxs-lookup"><span data-stu-id="07f69-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f69-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07f69-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="07f69-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07f69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f69-109">*prect*</span><span class="sxs-lookup"><span data-stu-id="07f69-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="07f69-110">Puntatore a una struttura **Rect** contenente le informazioni sul posizionamento.</span><span class="sxs-lookup"><span data-stu-id="07f69-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07f69-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07f69-111">Return value</span></span>

<span data-ttu-id="07f69-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07f69-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="07f69-113">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="07f69-113">Possible values include the following.</span></span>



| <span data-ttu-id="07f69-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="07f69-114">Return code</span></span>                                                                                  | <span data-ttu-id="07f69-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07f69-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="07f69-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="07f69-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="07f69-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="07f69-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="07f69-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="07f69-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="07f69-119">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="07f69-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="07f69-120"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="07f69-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="07f69-121">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="07f69-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="07f69-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07f69-122">Requirements</span></span>



| <span data-ttu-id="07f69-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f69-123">Requirement</span></span> | <span data-ttu-id="07f69-124">Valore</span><span class="sxs-lookup"><span data-stu-id="07f69-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07f69-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07f69-125">Header</span></span><br/>  | <dl> <span data-ttu-id="07f69-126"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07f69-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="07f69-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="07f69-127">Library</span></span><br/> | <dl> <span data-ttu-id="07f69-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07f69-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07f69-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07f69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f69-130">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="07f69-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




