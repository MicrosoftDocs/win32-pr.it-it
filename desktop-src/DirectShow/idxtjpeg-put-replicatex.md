---
description: Il \_ metodo Put ReplicateX specifica il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.
ms.assetid: 8baa641c-c063-4c22-8b00-3559c173d627
title: 'IDxtJpeg: metodo:p ut_ReplicateX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08d892619fe1e6f8222b40d45e634a350e4e9b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327519"
---
# <a name="idxtjpegput_replicatex-method"></a><span data-ttu-id="3885c-103">IDxtJpeg::p UT \_ ReplicateX metodo</span><span class="sxs-lookup"><span data-stu-id="3885c-103">IDxtJpeg::put\_ReplicateX method</span></span>

> [!Note]  
> <span data-ttu-id="3885c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3885c-104">\[Deprecated.</span></span> <span data-ttu-id="3885c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3885c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3885c-106">Il `put_ReplicateX` metodo specifica il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="3885c-106">The `put_ReplicateX` method specifies the number of times the wipe pattern is replicated horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="3885c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3885c-107">Syntax</span></span>


```C++
HRESULT put_ReplicateX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="3885c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3885c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3885c-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3885c-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3885c-110">Il numero di volte in cui il modello di cancellazione viene replicato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="3885c-110">The number of times the wipe pattern is replicated horizontally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3885c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3885c-111">Return value</span></span>

<span data-ttu-id="3885c-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3885c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3885c-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3885c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3885c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3885c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3885c-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="3885c-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3885c-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3885c-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3885c-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3885c-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3885c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3885c-118">Requirements</span></span>



| <span data-ttu-id="3885c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3885c-119">Requirement</span></span> | <span data-ttu-id="3885c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3885c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3885c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3885c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3885c-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3885c-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3885c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3885c-123">Library</span></span><br/> | <dl> <span data-ttu-id="3885c-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3885c-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3885c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3885c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3885c-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="3885c-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




