---
description: Il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Metodo CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327971"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="9f38a-103">CBaseDispatch. GetTypeInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="9f38a-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="9f38a-104">Il `GetTypeInfo` metodo recupera le informazioni sul tipo per l'oggetto, che può quindi essere usato per ottenere le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9f38a-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f38a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f38a-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="9f38a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f38a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f38a-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="9f38a-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="9f38a-108">Riferimento a un identificatore di interfaccia (IID) che specifica l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9f38a-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="9f38a-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="9f38a-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9f38a-110">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="9f38a-110">Type information to return.</span></span> <span data-ttu-id="9f38a-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9f38a-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9f38a-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="9f38a-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="9f38a-113">Identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="9f38a-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9f38a-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="9f38a-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9f38a-115">Indirizzo di una variabile che riceve un puntatore **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="9f38a-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f38a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f38a-116">Return value</span></span>

<span data-ttu-id="9f38a-117">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f38a-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9f38a-118">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="9f38a-118">Possible values include the following.</span></span>



| <span data-ttu-id="9f38a-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9f38a-119">Return code</span></span>                                                                                             | <span data-ttu-id="9f38a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f38a-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9f38a-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f38a-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="9f38a-122">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9f38a-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="9f38a-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9f38a-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="9f38a-124">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="9f38a-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="9f38a-125"><dt>**Digitare \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="9f38a-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="9f38a-126">Il parametro *itinfo* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9f38a-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9f38a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f38a-127">Remarks</span></span>

<span data-ttu-id="9f38a-128">Questo metodo si comporta come il metodo **IDispatch:: GetTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="9f38a-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="9f38a-129">Tuttavia, include un parametro aggiuntivo, *riid*, che specifica l'interfaccia per la quale recuperare le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="9f38a-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f38a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f38a-130">Requirements</span></span>



| <span data-ttu-id="9f38a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f38a-131">Requirement</span></span> | <span data-ttu-id="9f38a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9f38a-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f38a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f38a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9f38a-134"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f38a-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f38a-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f38a-135">Library</span></span><br/> | <dl> <span data-ttu-id="9f38a-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f38a-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f38a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f38a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f38a-138">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="9f38a-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




