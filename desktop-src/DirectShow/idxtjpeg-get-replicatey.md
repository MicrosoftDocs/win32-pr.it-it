---
description: Il \_ metodo Get replicate Recupera il numero di volte in cui il modello di cancellazione viene replicato verticalmente.
ms.assetid: 347e1ffa-bb39-4980-b8af-5806a23d1334
title: 'Metodo IDxtJpeg:: get_ReplicateY (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ae5c68d153b64783f84a6c4c4a8ba7f5d5f0f24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333253"
---
# <a name="idxtjpegget_replicatey-method"></a><span data-ttu-id="f4ddd-103">Metodo IDxtJpeg:: Get \_ replicate</span><span class="sxs-lookup"><span data-stu-id="f4ddd-103">IDxtJpeg::get\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="f4ddd-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-104">\[Deprecated.</span></span> <span data-ttu-id="f4ddd-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f4ddd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f4ddd-106">Il `get_ReplicateY` metodo recupera il numero di volte in cui il modello di cancellazione viene replicato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-106">The `get_ReplicateY` method retrieves the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ddd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4ddd-107">Syntax</span></span>


```C++
HRESULT get_ReplicateY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f4ddd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4ddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4ddd-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f4ddd-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f4ddd-110">Riceve il numero di volte in cui il modello di cancellazione viene replicato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-110">Receives the number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4ddd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4ddd-111">Return value</span></span>

<span data-ttu-id="f4ddd-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4ddd-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4ddd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ddd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4ddd-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4ddd-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f4ddd-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4ddd-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f4ddd-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f4ddd-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4ddd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4ddd-118">Requirements</span></span>



| <span data-ttu-id="f4ddd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4ddd-119">Requirement</span></span> | <span data-ttu-id="f4ddd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f4ddd-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ddd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4ddd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f4ddd-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4ddd-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f4ddd-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4ddd-123">Library</span></span><br/> | <dl> <span data-ttu-id="f4ddd-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4ddd-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ddd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4ddd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ddd-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="f4ddd-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




