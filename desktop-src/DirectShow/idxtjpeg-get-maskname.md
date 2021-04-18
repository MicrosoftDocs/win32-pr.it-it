---
description: Il \_ metodo Get maskName Recupera il nome di un file JPEG da usare come maschera di cancellazione.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'Metodo IDxtJpeg:: get_MaskName (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325921"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="0a71d-103">Metodo IDxtJpeg:: Get \_ maskName</span><span class="sxs-lookup"><span data-stu-id="0a71d-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="0a71d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0a71d-104">\[Deprecated.</span></span> <span data-ttu-id="0a71d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a71d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a71d-106">Il `get_MaskName` metodo recupera il nome di un file JPEG da utilizzare come maschera di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="0a71d-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a71d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a71d-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0a71d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a71d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a71d-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0a71d-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0a71d-110">Riceve il nome del file.</span><span class="sxs-lookup"><span data-stu-id="0a71d-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a71d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a71d-111">Return value</span></span>

<span data-ttu-id="0a71d-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a71d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a71d-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a71d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a71d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a71d-114">Remarks</span></span>

<span data-ttu-id="0a71d-115">Se la transizione di cancellazione usa una delle cancellazioni SMPTE predefinite supportate, il valore di questa proprietà è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="0a71d-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="0a71d-116">Il chiamante deve rilasciare la stringa restituita, usando la funzione **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="0a71d-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="0a71d-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0a71d-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a71d-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0a71d-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a71d-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0a71d-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a71d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a71d-120">Requirements</span></span>



| <span data-ttu-id="0a71d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a71d-121">Requirement</span></span> | <span data-ttu-id="0a71d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0a71d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a71d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a71d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0a71d-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a71d-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a71d-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a71d-125">Library</span></span><br/> | <dl> <span data-ttu-id="0a71d-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a71d-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a71d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a71d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a71d-128">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="0a71d-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="0a71d-129">**IDxtJpeg:: Get \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="0a71d-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




