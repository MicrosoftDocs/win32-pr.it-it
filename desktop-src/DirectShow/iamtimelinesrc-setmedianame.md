---
description: Il metodo semedianame specifica il nome del file di origine rappresentato da questo oggetto di origine.
ms.assetid: 60307c87-9dce-4e60-b14b-07d2c8604dd8
title: 'Metodo IAMTimelineSrc:: semedianame (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a770c697f72c8776e9ec7070272ab09fc0dd6af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332748"
---
# <a name="iamtimelinesrcsetmedianame-method"></a><span data-ttu-id="e6418-103">Metodo IAMTimelineSrc:: semedianame</span><span class="sxs-lookup"><span data-stu-id="e6418-103">IAMTimelineSrc::SetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="e6418-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e6418-104">\[Deprecated.</span></span> <span data-ttu-id="e6418-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6418-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6418-106">Il `SetMediaName` metodo specifica il nome del file di origine rappresentato da questo oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="e6418-106">The `SetMediaName` method specifies the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6418-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6418-107">Syntax</span></span>


```C++
HRESULT SetMediaName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e6418-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6418-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6418-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="e6418-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e6418-110">Stringa che specifica il nome del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="e6418-110">String that specifies the name of the media file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6418-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6418-111">Return value</span></span>

<span data-ttu-id="e6418-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6418-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6418-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6418-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6418-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6418-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6418-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e6418-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6418-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6418-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6418-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e6418-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6418-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6418-118">Requirements</span></span>



| <span data-ttu-id="e6418-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6418-119">Requirement</span></span> | <span data-ttu-id="e6418-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e6418-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6418-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6418-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e6418-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6418-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6418-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6418-123">Library</span></span><br/> | <dl> <span data-ttu-id="e6418-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6418-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6418-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6418-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6418-126">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="e6418-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="e6418-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e6418-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




