---
description: Il \_ metodo Put filename specifica il nome del file di origine per il rilevatore multimediale da usare.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: 'IMediaDet: metodo:p ut_Filename (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327823"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="e4b01-103">IMediaDet: metodo:p UT \_ filename</span><span class="sxs-lookup"><span data-stu-id="e4b01-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="e4b01-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e4b01-104">\[Deprecated.</span></span> <span data-ttu-id="e4b01-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4b01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e4b01-106">Il `put_Filename` metodo specifica il nome del file di origine per il rilevatore multimediale da usare.</span><span class="sxs-lookup"><span data-stu-id="e4b01-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="e4b01-107">Non chiamare questo metodo due volte sullo stesso oggetto MediaDet.</span><span class="sxs-lookup"><span data-stu-id="e4b01-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="e4b01-108">Per usare questa interfaccia con più di un file di origine, creare istanze separate dell'oggetto MediaDet.</span><span class="sxs-lookup"><span data-stu-id="e4b01-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b01-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4b01-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e4b01-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4b01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b01-111">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4b01-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b01-112">Nome del file di origine.</span><span class="sxs-lookup"><span data-stu-id="e4b01-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b01-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4b01-113">Return value</span></span>

<span data-ttu-id="e4b01-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e4b01-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4b01-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4b01-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b01-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4b01-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4b01-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e4b01-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e4b01-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e4b01-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e4b01-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e4b01-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4b01-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4b01-120">Requirements</span></span>



| <span data-ttu-id="e4b01-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b01-121">Requirement</span></span> | <span data-ttu-id="e4b01-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b01-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b01-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4b01-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b01-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b01-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e4b01-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4b01-125">Library</span></span><br/> | <dl> <span data-ttu-id="e4b01-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4b01-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b01-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4b01-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b01-128">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="e4b01-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="e4b01-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="e4b01-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




