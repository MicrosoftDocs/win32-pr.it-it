---
title: Metodo IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: Il metodo GetAnalogVideoRestrictionLevels recupera tutte le restrizioni video analogiche impostate per la licenza corrente.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Metodo GetAnalogVideoRestrictionLevels Windows Media Format
- Metodo GetAnalogVideoRestrictionLevels Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328529"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="641d7-106">Metodo IWMDRMLicense:: GetAnalogVideoRestrictionLevels</span><span class="sxs-lookup"><span data-stu-id="641d7-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="641d7-107">Il metodo **GetAnalogVideoRestrictionLevels** recupera tutte le restrizioni video analogiche impostate per la licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="641d7-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="641d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="641d7-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="641d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="641d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="641d7-110">*\[ rgAnalogVideoRestrictions \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="641d7-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="641d7-111">Riceve una matrice di strutture di [**\_ \_ \_ restrizioni video analogiche WMDRM**](wmdrm-analog-video-restrictions.md) .</span><span class="sxs-lookup"><span data-stu-id="641d7-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="641d7-112">Impostare su **null** per ottenere il numero di elementi nella matrice in *pcResctrictions*.</span><span class="sxs-lookup"><span data-stu-id="641d7-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="641d7-113">*pcRestrictions* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="641d7-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="641d7-114">Numero di elementi nella matrice di restrizioni.</span><span class="sxs-lookup"><span data-stu-id="641d7-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="641d7-115">Se *rgAnalogVideoRestrictions* è impostato su **null**, questo valore viene impostato sul numero di elementi necessari nella matrice.</span><span class="sxs-lookup"><span data-stu-id="641d7-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="641d7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="641d7-116">Return value</span></span>

<span data-ttu-id="641d7-117">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="641d7-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="641d7-118">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="641d7-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="641d7-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="641d7-119">Return code</span></span>                                                                          | <span data-ttu-id="641d7-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="641d7-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="641d7-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="641d7-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="641d7-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="641d7-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="641d7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="641d7-123">Remarks</span></span>

<span data-ttu-id="641d7-124">È necessario allocare memoria per la matrice di restrizioni.</span><span class="sxs-lookup"><span data-stu-id="641d7-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="641d7-125">A tale scopo, chiamare prima il metodo con *rgAnalogVideoRestrictions* impostato su **null**, impostando il valore su *pcRestrictions* sul numero di elementi necessari.</span><span class="sxs-lookup"><span data-stu-id="641d7-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="641d7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="641d7-126">Requirements</span></span>



| <span data-ttu-id="641d7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="641d7-127">Requirement</span></span> | <span data-ttu-id="641d7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="641d7-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="641d7-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="641d7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="641d7-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="641d7-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="641d7-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="641d7-131">Library</span></span><br/> | <dl> <span data-ttu-id="641d7-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="641d7-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="641d7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="641d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="641d7-134">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="641d7-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





