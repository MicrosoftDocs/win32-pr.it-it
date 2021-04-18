---
description: Il metodo AddFoundLocation aggiunge una directory alla cache di directory.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'Metodo IMediaLocator:: AddFoundLocation (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325304"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="9f6fe-103">Metodo IMediaLocator:: AddFoundLocation</span><span class="sxs-lookup"><span data-stu-id="9f6fe-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="9f6fe-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-104">\[Deprecated.</span></span> <span data-ttu-id="9f6fe-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f6fe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9f6fe-106">Il `AddFoundLocation` metodo aggiunge una directory alla cache di directory.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6fe-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f6fe-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="9f6fe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6fe-109">*DirectoryName*</span><span class="sxs-lookup"><span data-stu-id="9f6fe-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6fe-110">Percorso della directory da aggiungere alla cache.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6fe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f6fe-111">Return value</span></span>

<span data-ttu-id="9f6fe-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f6fe-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f6fe-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f6fe-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f6fe-114">Remarks</span></span>

<span data-ttu-id="9f6fe-115">Il localizzatore multimediale mantiene una cache dei percorsi di directory in cui i file sono stati trovati correttamente nelle ricerche precedenti.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="9f6fe-116">Quando individua correttamente un file, aggiunge la directory alla cache.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="9f6fe-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f6fe-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f6fe-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9f6fe-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9f6fe-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f6fe-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f6fe-120">Requirements</span></span>



| <span data-ttu-id="9f6fe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f6fe-121">Requirement</span></span> | <span data-ttu-id="9f6fe-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9f6fe-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6fe-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f6fe-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9f6fe-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f6fe-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9f6fe-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f6fe-125">Library</span></span><br/> | <dl> <span data-ttu-id="9f6fe-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f6fe-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6fe-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f6fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6fe-128">**Interfaccia IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="9f6fe-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="9f6fe-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="9f6fe-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




