---
description: Il metodo LoadDefSettings Ripristina le impostazioni predefinite della transizione di cancellazione.
ms.assetid: 3f81002a-ecac-4d5a-8d2a-ada4d4884d7d
title: 'Metodo IDxtJpeg:: LoadDefSettings (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.LoadDefSettings
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51438a21782d1a703a3b43134517e8337ce9f75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330639"
---
# <a name="idxtjpegloaddefsettings-method"></a><span data-ttu-id="065ce-103">Metodo IDxtJpeg:: LoadDefSettings</span><span class="sxs-lookup"><span data-stu-id="065ce-103">IDxtJpeg::LoadDefSettings method</span></span>

> [!Note]  
> <span data-ttu-id="065ce-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="065ce-104">\[Deprecated.</span></span> <span data-ttu-id="065ce-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="065ce-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="065ce-106">Il `LoadDefSettings` metodo ripristina le impostazioni predefinite della transizione di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="065ce-106">The `LoadDefSettings` method restores the default settings of the Wipe transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="065ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="065ce-107">Syntax</span></span>


```C++
HRESULT LoadDefSettings();
```



## <a name="parameters"></a><span data-ttu-id="065ce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="065ce-108">Parameters</span></span>

<span data-ttu-id="065ce-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="065ce-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="065ce-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="065ce-110">Return value</span></span>

<span data-ttu-id="065ce-111">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="065ce-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="065ce-112">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="065ce-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="065ce-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="065ce-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="065ce-114">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="065ce-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="065ce-115">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="065ce-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="065ce-116">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="065ce-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="065ce-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="065ce-117">Requirements</span></span>



| <span data-ttu-id="065ce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="065ce-118">Requirement</span></span> | <span data-ttu-id="065ce-119">Valore</span><span class="sxs-lookup"><span data-stu-id="065ce-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="065ce-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="065ce-120">Header</span></span><br/>  | <dl> <span data-ttu-id="065ce-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="065ce-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="065ce-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="065ce-122">Library</span></span><br/> | <dl> <span data-ttu-id="065ce-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="065ce-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065ce-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="065ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065ce-125">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="065ce-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




