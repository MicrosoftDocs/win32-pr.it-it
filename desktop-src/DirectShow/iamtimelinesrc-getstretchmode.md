---
description: Il metodo GetStretchMode recupera la modalità di estensione. La modalità di estensione determina come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'Metodo IAMTimelineSrc:: GetStretchMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332763"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="46f2e-104">Metodo IAMTimelineSrc:: GetStretchMode</span><span class="sxs-lookup"><span data-stu-id="46f2e-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="46f2e-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="46f2e-105">\[Deprecated.</span></span> <span data-ttu-id="46f2e-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46f2e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46f2e-107">Il `GetStretchMode` metodo recupera la modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="46f2e-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="46f2e-108">La modalità di estensione determina come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.</span><span class="sxs-lookup"><span data-stu-id="46f2e-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f2e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46f2e-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="46f2e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="46f2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f2e-111">*pnStretchMode*</span><span class="sxs-lookup"><span data-stu-id="46f2e-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="46f2e-112">Riceve un flag che indica la modalità di estensione corrente.</span><span class="sxs-lookup"><span data-stu-id="46f2e-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="46f2e-113">Per un elenco di valori possibili, vedere [**ridimensionare i flag**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="46f2e-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46f2e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46f2e-114">Return value</span></span>

<span data-ttu-id="46f2e-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46f2e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46f2e-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46f2e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46f2e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="46f2e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46f2e-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="46f2e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46f2e-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46f2e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46f2e-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46f2e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46f2e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46f2e-121">Requirements</span></span>



| <span data-ttu-id="46f2e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f2e-122">Requirement</span></span> | <span data-ttu-id="46f2e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="46f2e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46f2e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46f2e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="46f2e-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46f2e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46f2e-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="46f2e-126">Library</span></span><br/> | <dl> <span data-ttu-id="46f2e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46f2e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46f2e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46f2e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f2e-129">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="46f2e-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="46f2e-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="46f2e-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




