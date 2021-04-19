---
description: Il \_ metodo Put replicate specifica il numero di volte in cui il modello di cancellazione viene replicato verticalmente.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: 'IDxtJpeg: metodo:p ut_ReplicateY (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ac5016635cb8e6f5b81b99f1ea67f0282878d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328331"
---
# <a name="idxtjpegput_replicatey-method"></a><span data-ttu-id="46484-103">IDxtJpeg: metodo di \_ replica ut:p</span><span class="sxs-lookup"><span data-stu-id="46484-103">IDxtJpeg::put\_ReplicateY method</span></span>

> [!Note]  
> <span data-ttu-id="46484-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="46484-104">\[Deprecated.</span></span> <span data-ttu-id="46484-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46484-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46484-106">Il `put_ReplicateY` metodo specifica il numero di volte in cui il modello di cancellazione viene replicato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="46484-106">The `put_ReplicateY` method specifies the number of times the wipe pattern is replicated vertically.</span></span>

## <a name="syntax"></a><span data-ttu-id="46484-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46484-107">Syntax</span></span>


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="46484-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46484-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46484-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46484-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46484-110">Il numero di volte in cui il modello di cancellazione viene replicato verticalmente.</span><span class="sxs-lookup"><span data-stu-id="46484-110">The number of times the wipe pattern is replicated vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46484-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46484-111">Return value</span></span>

<span data-ttu-id="46484-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="46484-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46484-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46484-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46484-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="46484-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46484-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="46484-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="46484-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="46484-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="46484-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="46484-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46484-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46484-118">Requirements</span></span>



| <span data-ttu-id="46484-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="46484-119">Requirement</span></span> | <span data-ttu-id="46484-120">Valore</span><span class="sxs-lookup"><span data-stu-id="46484-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46484-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46484-121">Header</span></span><br/>  | <dl> <span data-ttu-id="46484-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="46484-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="46484-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="46484-123">Library</span></span><br/> | <dl> <span data-ttu-id="46484-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46484-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46484-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46484-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46484-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="46484-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




