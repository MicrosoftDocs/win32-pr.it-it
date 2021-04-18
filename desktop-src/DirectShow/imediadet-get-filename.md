---
description: Il \_ metodo Get FileName Recupera il nome del file di origine attualmente utilizzato dal rilevamento multimediale.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'Metodo IMediaDet:: get_Filename (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330636"
---
# <a name="imediadetget_filename-method"></a><span data-ttu-id="556bd-103">Metodo IMediaDet:: Get \_ filename</span><span class="sxs-lookup"><span data-stu-id="556bd-103">IMediaDet::get\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="556bd-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="556bd-104">\[Deprecated.</span></span> <span data-ttu-id="556bd-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="556bd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="556bd-106">Il `get_Filename` metodo recupera il nome del file di origine attualmente utilizzato dal rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="556bd-106">The `get_Filename` method retrieves the name of the source file currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="556bd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="556bd-107">Syntax</span></span>


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="556bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="556bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="556bd-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="556bd-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="556bd-110">Riceve il nome del file.</span><span class="sxs-lookup"><span data-stu-id="556bd-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="556bd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="556bd-111">Return value</span></span>

<span data-ttu-id="556bd-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="556bd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="556bd-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="556bd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="556bd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="556bd-114">Remarks</span></span>

<span data-ttu-id="556bd-115">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="556bd-115">The method allocates memory for the string.</span></span> <span data-ttu-id="556bd-116">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="556bd-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="556bd-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="556bd-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="556bd-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="556bd-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="556bd-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="556bd-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="556bd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="556bd-120">Requirements</span></span>



| <span data-ttu-id="556bd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="556bd-121">Requirement</span></span> | <span data-ttu-id="556bd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="556bd-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="556bd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="556bd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="556bd-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="556bd-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="556bd-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="556bd-125">Library</span></span><br/> | <dl> <span data-ttu-id="556bd-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="556bd-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="556bd-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="556bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="556bd-128">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="556bd-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="556bd-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="556bd-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




