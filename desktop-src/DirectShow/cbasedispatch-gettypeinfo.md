---
description: "Metodo CBaseDispatch.GetTypeInfo: il metodo GetTypeInfo recupera le informazioni sul tipo per l'oggetto, che possono quindi essere usate per ottenere le informazioni sul tipo per un'interfaccia."
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Metodo CBaseDispatch.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: a9b1e21133b4fa561c743fefc6282c777b444e6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120119"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="02ad1-103">Metodo CBaseDispatch.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="02ad1-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="02ad1-104">Il metodo recupera le informazioni sul tipo per l'oggetto , che può quindi essere usato per `GetTypeInfo` ottenere le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="02ad1-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ad1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02ad1-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="02ad1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02ad1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ad1-107">*Riid*</span><span class="sxs-lookup"><span data-stu-id="02ad1-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="02ad1-108">Riferimento a un identificatore di interfaccia (IID) che specifica l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="02ad1-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="02ad1-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="02ad1-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="02ad1-110">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="02ad1-110">Type information to return.</span></span> <span data-ttu-id="02ad1-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="02ad1-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="02ad1-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="02ad1-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="02ad1-113">Identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="02ad1-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02ad1-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="02ad1-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="02ad1-115">Indirizzo di una variabile che riceve un **puntatore ITypeInfo.**</span><span class="sxs-lookup"><span data-stu-id="02ad1-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ad1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02ad1-116">Return value</span></span>

<span data-ttu-id="02ad1-117">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="02ad1-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="02ad1-118">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="02ad1-118">Possible values include the following.</span></span>



| <span data-ttu-id="02ad1-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="02ad1-119">Return code</span></span>                                                                                             | <span data-ttu-id="02ad1-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02ad1-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="02ad1-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02ad1-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="02ad1-122">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="02ad1-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="02ad1-123"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="02ad1-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="02ad1-124">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="02ad1-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="02ad1-125"><dt>**TIPO \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="02ad1-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="02ad1-126">Il *parametro itinfo* non è zero.</span><span class="sxs-lookup"><span data-stu-id="02ad1-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02ad1-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="02ad1-127">Remarks</span></span>

<span data-ttu-id="02ad1-128">Questo metodo si comporta come **il metodo IDispatch::GetTypeInfo.**</span><span class="sxs-lookup"><span data-stu-id="02ad1-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="02ad1-129">Include tuttavia un parametro aggiuntivo, *riid*, che specifica l'interfaccia per cui recuperare le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="02ad1-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="02ad1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02ad1-130">Requirements</span></span>



| <span data-ttu-id="02ad1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="02ad1-131">Requirement</span></span> | <span data-ttu-id="02ad1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="02ad1-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ad1-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02ad1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="02ad1-134"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="02ad1-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02ad1-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="02ad1-135">Library</span></span><br/> | <dl> <span data-ttu-id="02ad1-136"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02ad1-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ad1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02ad1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ad1-138">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="02ad1-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




