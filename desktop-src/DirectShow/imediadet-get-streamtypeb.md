---
description: Il \_ metodo Get StreamTypeB recupera una stringa che rappresenta il GUID del tipo di supporto per il flusso corrente.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'Metodo IMediaDet:: get_StreamTypeB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332029"
---
# <a name="imediadetget_streamtypeb-method"></a><span data-ttu-id="8f7c2-103">Metodo IMediaDet:: Get \_ StreamTypeB</span><span class="sxs-lookup"><span data-stu-id="8f7c2-103">IMediaDet::get\_StreamTypeB method</span></span>

> [!Note]  
> <span data-ttu-id="8f7c2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-104">\[Deprecated.</span></span> <span data-ttu-id="8f7c2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f7c2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8f7c2-106">Il `get_StreamTypeB` metodo recupera una stringa che rappresenta il GUID del tipo di supporto per il flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-106">The `get_StreamTypeB` method retrieves a string representing the GUID of the media type for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f7c2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f7c2-107">Syntax</span></span>


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8f7c2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f7c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f7c2-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8f7c2-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8f7c2-110">Riceve una rappresentazione di stringa del GUID del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-110">Receives a string representation of the media type GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f7c2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f7c2-111">Return value</span></span>

<span data-ttu-id="8f7c2-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f7c2-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f7c2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f7c2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f7c2-114">Remarks</span></span>

<span data-ttu-id="8f7c2-115">Il formato **BSTR** restituito è simile al seguente: `{73647561-0000-0010-8000-00AA00389B71}`</span><span class="sxs-lookup"><span data-stu-id="8f7c2-115">The returned **BSTR** is formatted like the following: `{73647561-0000-0010-8000-00AA00389B71}`</span></span>

<span data-ttu-id="8f7c2-116">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-116">The method allocates memory for the string.</span></span> <span data-ttu-id="8f7c2-117">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="8f7c2-117">The application must call **SysFreeString** to free the memory.</span></span>

<span data-ttu-id="8f7c2-118">Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="8f7c2-118">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="8f7c2-119">Se il rilevatore multimediale è in modalità di cattura bitmap, questo metodo restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-119">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="8f7c2-120">Per ulteriori informazioni, vedere [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="8f7c2-120">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f7c2-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8f7c2-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8f7c2-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8f7c2-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8f7c2-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f7c2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f7c2-124">Requirements</span></span>



| <span data-ttu-id="8f7c2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f7c2-125">Requirement</span></span> | <span data-ttu-id="8f7c2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8f7c2-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7c2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f7c2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8f7c2-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f7c2-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8f7c2-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f7c2-129">Library</span></span><br/> | <dl> <span data-ttu-id="8f7c2-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f7c2-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7c2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f7c2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7c2-132">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="8f7c2-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="8f7c2-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8f7c2-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




