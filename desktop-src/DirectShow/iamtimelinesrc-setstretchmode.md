---
description: Il metodo SetStretchMode imposta la modalità di estensione. La modalità di estensione determina come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Metodo IAMTimelineSrc:: SetStretchMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325180"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="4485e-104">Metodo IAMTimelineSrc:: SetStretchMode</span><span class="sxs-lookup"><span data-stu-id="4485e-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="4485e-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4485e-105">\[Deprecated.</span></span> <span data-ttu-id="4485e-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4485e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4485e-107">Il `SetStretchMode` metodo imposta la modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="4485e-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="4485e-108">La modalità di estensione determina come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.</span><span class="sxs-lookup"><span data-stu-id="4485e-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4485e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4485e-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="4485e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4485e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4485e-111">*nStretchMode*</span><span class="sxs-lookup"><span data-stu-id="4485e-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="4485e-112">Flag che indica la modalità di estensione corrente.</span><span class="sxs-lookup"><span data-stu-id="4485e-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="4485e-113">Per un elenco di valori possibili, vedere [**ridimensionare i flag**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4485e-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4485e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4485e-114">Return value</span></span>

<span data-ttu-id="4485e-115">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4485e-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4485e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4485e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4485e-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4485e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4485e-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4485e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4485e-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4485e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4485e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4485e-120">Requirements</span></span>



| <span data-ttu-id="4485e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4485e-121">Requirement</span></span> | <span data-ttu-id="4485e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4485e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4485e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4485e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4485e-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4485e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4485e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4485e-125">Library</span></span><br/> | <dl> <span data-ttu-id="4485e-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4485e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4485e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4485e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4485e-128">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="4485e-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="4485e-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4485e-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




