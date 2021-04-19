---
description: Il metodo SetDefaultFPS imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Metodo IAMTimelineSrc:: SetDefaultFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330184"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="bff09-103">Metodo IAMTimelineSrc:: SetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="bff09-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="bff09-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bff09-104">\[Deprecated.</span></span> <span data-ttu-id="bff09-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bff09-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bff09-106">Il `SetDefaultFPS` metodo imposta la frequenza dei fotogrammi predefinita dell'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="bff09-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff09-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bff09-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="bff09-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bff09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff09-109">*FPS*</span><span class="sxs-lookup"><span data-stu-id="bff09-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="bff09-110">Frequenza fotogrammi predefinita, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="bff09-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff09-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bff09-111">Return value</span></span>

<span data-ttu-id="bff09-112">Restituisce \_ OK se ha esito positivo oppure E \_ INVALIDARG se la frequenza dei fotogrammi specificata è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="bff09-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff09-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bff09-113">Remarks</span></span>

<span data-ttu-id="bff09-114">Il motore di rendering utilizza questo valore se non è in grado di determinare la frequenza dei fotogrammi dal file di origine originale.</span><span class="sxs-lookup"><span data-stu-id="bff09-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="bff09-115">Chiamare questo metodo solo per i file di origine senza una frequenza dei fotogrammi predefinita.</span><span class="sxs-lookup"><span data-stu-id="bff09-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="bff09-116">Per i file bitmap e JPEG, la frequenza dei fotogrammi predefinita è zero, che fa sì che l'origine venga sottoposta a rendering come immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="bff09-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="bff09-117">Per usare l'immagine come primo fotogramma in una sequenza DIB, impostare la frequenza dei fotogrammi su un valore maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="bff09-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="bff09-118">Per ulteriori informazioni, vedere [utilizzo delle origini](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="bff09-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="bff09-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bff09-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bff09-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bff09-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bff09-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bff09-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bff09-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bff09-122">Requirements</span></span>



| <span data-ttu-id="bff09-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff09-123">Requirement</span></span> | <span data-ttu-id="bff09-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bff09-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bff09-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bff09-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bff09-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff09-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bff09-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="bff09-127">Library</span></span><br/> | <dl> <span data-ttu-id="bff09-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bff09-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff09-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bff09-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff09-130">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="bff09-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="bff09-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="bff09-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




