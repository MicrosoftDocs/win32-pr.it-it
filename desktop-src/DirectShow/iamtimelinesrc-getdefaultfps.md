---
description: Il metodo GetDefaultFPS recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine. Il motore di rendering utilizza questo valore se non è in grado di determinare la frequenza dei fotogrammi dall'origine originale.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Metodo IAMTimelineSrc:: GetDefaultFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324261"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="77813-104">Metodo IAMTimelineSrc:: GetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="77813-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="77813-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="77813-105">\[Deprecated.</span></span> <span data-ttu-id="77813-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77813-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="77813-107">Il `GetDefaultFPS` metodo recupera la frequenza dei fotogrammi predefinita dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="77813-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="77813-108">Il motore di rendering utilizza questo valore se non è in grado di determinare la frequenza dei fotogrammi dall'origine originale.</span><span class="sxs-lookup"><span data-stu-id="77813-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="77813-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77813-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="77813-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="77813-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77813-111">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="77813-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="77813-112">Riceve la frequenza dei fotogrammi predefinita, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="77813-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77813-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77813-113">Return value</span></span>

<span data-ttu-id="77813-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="77813-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77813-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77813-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77813-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="77813-116">Remarks</span></span>

<span data-ttu-id="77813-117">La frequenza dei fotogrammi predefinita non è obbligatoria se il formato di file specifica la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="77813-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="77813-118">Questo è il caso di formati audio e video.</span><span class="sxs-lookup"><span data-stu-id="77813-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="77813-119">Se l'origine è un'immagine bitmap o JPEG, il motore di rendering la usa come prima immagine in una sequenza di bitmap indipendente dal dispositivo (DIB), con una frequenza di fotogrammi uguale alla frequenza dei fotogrammi predefinita.</span><span class="sxs-lookup"><span data-stu-id="77813-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="77813-120">Per eseguire il rendering di un'immagine statica, anziché una sequenza DIB, impostare la frequenza dei fotogrammi predefinita su 0.</span><span class="sxs-lookup"><span data-stu-id="77813-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="77813-121">Se l'origine è un GIF, non impostare la frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="77813-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="77813-122">Per gif animate, il file GIF specifica il ritardo tra le singole immagini.</span><span class="sxs-lookup"><span data-stu-id="77813-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="77813-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="77813-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="77813-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="77813-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="77813-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="77813-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77813-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77813-126">Requirements</span></span>



| <span data-ttu-id="77813-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="77813-127">Requirement</span></span> | <span data-ttu-id="77813-128">Valore</span><span class="sxs-lookup"><span data-stu-id="77813-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77813-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77813-129">Header</span></span><br/>  | <dl> <span data-ttu-id="77813-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="77813-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="77813-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="77813-131">Library</span></span><br/> | <dl> <span data-ttu-id="77813-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77813-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77813-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77813-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77813-134">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="77813-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="77813-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="77813-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




