---
description: 'Il metodo GetPageInfo recupera le informazioni sulla pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Metodo CBasePropertyPage. GetPageInfo (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330694"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="9a6e0-104">CBasePropertyPage. GetPageInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="9a6e0-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="9a6e0-105">Il `GetPageInfo` metodo recupera le informazioni sulla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9a6e0-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="9a6e0-106">Questo metodo implementa il metodo **IPropertyPage:: GetPageInfo** .</span><span class="sxs-lookup"><span data-stu-id="9a6e0-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6e0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a6e0-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9a6e0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a6e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a6e0-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="9a6e0-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9a6e0-110">Puntatore a una struttura **PROPPAGEINFO** allocata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="9a6e0-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a6e0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a6e0-111">Return value</span></span>

<span data-ttu-id="9a6e0-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a6e0-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9a6e0-113">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="9a6e0-113">Possible values include the following.</span></span>



| <span data-ttu-id="9a6e0-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9a6e0-114">Return code</span></span>                                                                                   | <span data-ttu-id="9a6e0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a6e0-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="9a6e0-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6e0-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9a6e0-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9a6e0-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="9a6e0-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6e0-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9a6e0-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9a6e0-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9a6e0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a6e0-120">Requirements</span></span>



| <span data-ttu-id="9a6e0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a6e0-121">Requirement</span></span> | <span data-ttu-id="9a6e0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9a6e0-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6e0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a6e0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9a6e0-124"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a6e0-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="9a6e0-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a6e0-125">Library</span></span><br/> | <dl> <span data-ttu-id="9a6e0-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a6e0-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a6e0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a6e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a6e0-128">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="9a6e0-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




