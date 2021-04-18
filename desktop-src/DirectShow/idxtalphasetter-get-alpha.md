---
description: Il \_ metodo Get Alpha Recupera il valore alfa per l'intera immagine.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Metodo IDxtAlphaSetter:: get_Alpha (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327922"
---
# <a name="idxtalphasetterget_alpha-method"></a><span data-ttu-id="80a92-103">Metodo IDxtAlphaSetter:: Get \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="80a92-103">IDxtAlphaSetter::get\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="80a92-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="80a92-104">\[Deprecated.</span></span> <span data-ttu-id="80a92-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80a92-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="80a92-106">Il `get_Alpha` metodo recupera il valore alfa per l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="80a92-106">The `get_Alpha` method retrieves the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a92-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80a92-107">Syntax</span></span>


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="80a92-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="80a92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a92-109">*pAlpha* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="80a92-109">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="80a92-110">Riceve il valore alfa.</span><span class="sxs-lookup"><span data-stu-id="80a92-110">Receives the alpha value.</span></span> <span data-ttu-id="80a92-111">Questo valore alfa verrà applicato all'intera immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80a92-111">This alpha value will be applied to the entire target image.</span></span> <span data-ttu-id="80a92-112">Un valore negativo indica che non è impostato alcun valore alfa.</span><span class="sxs-lookup"><span data-stu-id="80a92-112">A negative value indicates that no alpha value is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a92-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80a92-113">Return value</span></span>

<span data-ttu-id="80a92-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80a92-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="80a92-115">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="80a92-115">Possible values include the following.</span></span>



| <span data-ttu-id="80a92-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="80a92-116">Return code</span></span>                                                                               | <span data-ttu-id="80a92-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80a92-117">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="80a92-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="80a92-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="80a92-119">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="80a92-119">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="80a92-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80a92-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="80a92-121">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="80a92-121">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="80a92-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="80a92-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80a92-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="80a92-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="80a92-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="80a92-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="80a92-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="80a92-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80a92-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80a92-126">Requirements</span></span>



| <span data-ttu-id="80a92-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a92-127">Requirement</span></span> | <span data-ttu-id="80a92-128">Valore</span><span class="sxs-lookup"><span data-stu-id="80a92-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80a92-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80a92-129">Header</span></span><br/>  | <dl> <span data-ttu-id="80a92-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a92-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="80a92-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="80a92-131">Library</span></span><br/> | <dl> <span data-ttu-id="80a92-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80a92-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a92-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80a92-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a92-134">**Interfaccia IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="80a92-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




