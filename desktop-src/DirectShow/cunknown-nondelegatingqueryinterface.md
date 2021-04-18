---
description: 'Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. Questo metodo implementa il metodo INonDelegatingUnknown:: NonDelegatingQueryInterface.'
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Metodo CUnknown. NonDelegatingQueryInterface (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331446"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="05356-104">CUnknown. NonDelegatingQueryInterface, metodo</span><span class="sxs-lookup"><span data-stu-id="05356-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="05356-105">Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="05356-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="05356-106">Questo metodo implementa il metodo **INonDelegatingUnknown:: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="05356-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05356-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05356-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="05356-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="05356-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05356-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="05356-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="05356-110">Identificatore dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="05356-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="05356-111">*PPV*</span><span class="sxs-lookup"><span data-stu-id="05356-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="05356-112">Indirizzo di un puntatore per la ricezione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="05356-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05356-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05356-113">Return value</span></span>

<span data-ttu-id="05356-114">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="05356-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="05356-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="05356-115">Return code</span></span>                                                                                   | <span data-ttu-id="05356-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05356-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="05356-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05356-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05356-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="05356-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="05356-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="05356-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="05356-120">L'oggetto non supporta questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="05356-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="05356-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="05356-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="05356-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="05356-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="05356-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="05356-123">Remarks</span></span>

<span data-ttu-id="05356-124">La classe **CUnknown** espone solo l'interfaccia **IUknown** .</span><span class="sxs-lookup"><span data-stu-id="05356-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="05356-125">Eseguire l'override di questo metodo per esporre interfacce aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="05356-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="05356-126">Per informazioni su come eseguire l'override di questo metodo, vedere [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="05356-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05356-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05356-127">Requirements</span></span>



| <span data-ttu-id="05356-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="05356-128">Requirement</span></span> | <span data-ttu-id="05356-129">Valore</span><span class="sxs-lookup"><span data-stu-id="05356-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05356-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05356-130">Header</span></span><br/>  | <dl> <span data-ttu-id="05356-131"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05356-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05356-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="05356-132">Library</span></span><br/> | <dl> <span data-ttu-id="05356-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05356-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




