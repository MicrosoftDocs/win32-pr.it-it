---
description: Il metodo init Inizializza l'oggetto.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Metodo CSeekingPassThru.Init (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324665"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="cb792-103">Metodo CSeekingPassThru.Init</span><span class="sxs-lookup"><span data-stu-id="cb792-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="cb792-104">Il `Init` metodo inizializza l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb792-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb792-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb792-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="cb792-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb792-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb792-107">*bSupportRendering* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb792-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb792-108">Valore booleano che specifica se il filtro è un renderer.</span><span class="sxs-lookup"><span data-stu-id="cb792-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="cb792-109">Usare il valore **true** se il filtro è un renderer oppure **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cb792-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="cb792-110">*pPin*</span><span class="sxs-lookup"><span data-stu-id="cb792-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="cb792-111">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) sul pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="cb792-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb792-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb792-112">Return value</span></span>

<span data-ttu-id="cb792-113">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cb792-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="cb792-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cb792-114">Return code</span></span>                                                                                   | <span data-ttu-id="cb792-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb792-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="cb792-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb792-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cb792-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cb792-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="cb792-118"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="cb792-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cb792-119">Oggetto già inizializzato.</span><span class="sxs-lookup"><span data-stu-id="cb792-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="cb792-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="cb792-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cb792-121">Memoria insufficiente per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb792-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb792-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb792-122">Remarks</span></span>

<span data-ttu-id="cb792-123">Se il valore di *bSupportRendering* è **true**, questo metodo crea un'istanza della classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="cb792-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="cb792-124">In caso contrario, viene creata un'istanza della classe [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="cb792-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb792-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb792-125">Requirements</span></span>



| <span data-ttu-id="cb792-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb792-126">Requirement</span></span> | <span data-ttu-id="cb792-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cb792-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb792-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb792-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cb792-129"><dt>Seekpt. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb792-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cb792-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb792-130">Library</span></span><br/> | <dl> <span data-ttu-id="cb792-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cb792-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb792-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb792-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb792-133">**Classe CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="cb792-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




