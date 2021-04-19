---
description: Il \_ metodo Get AlphaRamp recupera la proprietà Alpha ramp. La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale. Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Metodo IDxtAlphaSetter:: get_AlphaRamp (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326782"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="71866-105">Metodo IDxtAlphaSetter:: Get \_ AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="71866-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="71866-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="71866-106">\[Deprecated.</span></span> <span data-ttu-id="71866-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71866-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="71866-108">Il `get_AlphaRamp` metodo recupera la proprietà della rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="71866-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="71866-109">La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="71866-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="71866-110">Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.</span><span class="sxs-lookup"><span data-stu-id="71866-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="71866-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71866-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="71866-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="71866-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71866-113">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="71866-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="71866-114">Riceve la rampa Alpha.</span><span class="sxs-lookup"><span data-stu-id="71866-114">Receives the alpha ramp.</span></span> <span data-ttu-id="71866-115">Un valore negativo indica che non è impostata alcuna rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="71866-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71866-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71866-116">Return value</span></span>

<span data-ttu-id="71866-117">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71866-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71866-118">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="71866-118">Possible values include the following.</span></span>



| <span data-ttu-id="71866-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="71866-119">Return code</span></span>                                                                               | <span data-ttu-id="71866-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71866-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="71866-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="71866-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="71866-122">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="71866-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="71866-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71866-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="71866-124">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="71866-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="71866-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="71866-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="71866-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="71866-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="71866-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="71866-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="71866-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="71866-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71866-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71866-129">Requirements</span></span>



| <span data-ttu-id="71866-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="71866-130">Requirement</span></span> | <span data-ttu-id="71866-131">Valore</span><span class="sxs-lookup"><span data-stu-id="71866-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71866-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71866-132">Header</span></span><br/>  | <dl> <span data-ttu-id="71866-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="71866-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="71866-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="71866-134">Library</span></span><br/> | <dl> <span data-ttu-id="71866-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71866-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71866-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71866-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71866-137">**Interfaccia IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="71866-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




