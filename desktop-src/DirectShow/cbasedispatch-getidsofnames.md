---
description: 'Metodo CBaseDispatch.GetIDsOfNames: il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set corrispondente di DISPID.'
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Metodo CBaseDispatch.GetIDsOfNames (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f3b718c95d588ffdc7fa63902e6b26ffbf11fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099919"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="f9306-103">Metodo CBaseDispatch.GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="f9306-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="f9306-104">Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set corrispondente di DISPID.</span><span class="sxs-lookup"><span data-stu-id="f9306-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9306-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9306-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="f9306-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9306-107">*Riid*</span><span class="sxs-lookup"><span data-stu-id="f9306-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="f9306-108">Riferimento a un identificatore di interfaccia (IID) che specifica l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f9306-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="f9306-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="f9306-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="f9306-110">Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="f9306-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="f9306-111">*cNames*</span><span class="sxs-lookup"><span data-stu-id="f9306-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="f9306-112">Dimensione della matrice specificata dal *parametro rgszNames.*</span><span class="sxs-lookup"><span data-stu-id="f9306-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f9306-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="f9306-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="f9306-114">Contesto delle impostazioni locali in cui interpretare i nomi.</span><span class="sxs-lookup"><span data-stu-id="f9306-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="f9306-115">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f9306-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f9306-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="f9306-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="f9306-117">Puntatore a una matrice che riceve i DISPID.</span><span class="sxs-lookup"><span data-stu-id="f9306-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="f9306-118">Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel *parametro rgszNames.*</span><span class="sxs-lookup"><span data-stu-id="f9306-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9306-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9306-119">Return value</span></span>

<span data-ttu-id="f9306-120">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f9306-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f9306-121">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="f9306-121">Possible values include the following.</span></span>



| <span data-ttu-id="f9306-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9306-122">Return code</span></span>                                                                                         | <span data-ttu-id="f9306-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9306-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="f9306-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9306-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="f9306-125">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="f9306-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f9306-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f9306-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="f9306-127">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f9306-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="f9306-128"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="f9306-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="f9306-129">Uno o più nomi non erano noti.</span><span class="sxs-lookup"><span data-stu-id="f9306-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9306-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9306-130">Remarks</span></span>

<span data-ttu-id="f9306-131">Questo metodo si comporta come **il metodo IDispatch::GetIDsOfNames,** ma il *parametro riid* specifica l'interfaccia in cui recuperare i DISPID.</span><span class="sxs-lookup"><span data-stu-id="f9306-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="f9306-132">Nella versione **IDispatch** il *parametro riid* è riservato.</span><span class="sxs-lookup"><span data-stu-id="f9306-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="f9306-133">Se il metodo restituisce DISP E UNKNOWNNAME, i DISPID restituiti contengono DISPID UNKNOWN per ogni voce \_ che corrisponde a un nome \_ \_ sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f9306-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9306-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9306-134">Requirements</span></span>



| <span data-ttu-id="f9306-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9306-135">Requirement</span></span> | <span data-ttu-id="f9306-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f9306-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9306-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9306-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f9306-138"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9306-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9306-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9306-139">Library</span></span><br/> | <dl> <span data-ttu-id="f9306-140"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f9306-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9306-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9306-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9306-142">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="f9306-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




