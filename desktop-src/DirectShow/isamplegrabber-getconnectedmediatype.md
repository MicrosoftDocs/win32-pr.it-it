---
description: Il metodo GetConnectedMediaType Recupera il tipo di supporto per la connessione sul pin di input del grabber di esempio.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Metodo ISampleGrabber:: GetConnectedMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325297"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="c75c7-103">Metodo ISampleGrabber:: GetConnectedMediaType</span><span class="sxs-lookup"><span data-stu-id="c75c7-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="c75c7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c75c7-104">\[Deprecated.</span></span> <span data-ttu-id="c75c7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c75c7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c75c7-106">Il `GetConnectedMediaType` metodo recupera il tipo di supporto per la connessione sul pin di input del grabber di esempio.</span><span class="sxs-lookup"><span data-stu-id="c75c7-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c75c7-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="c75c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c75c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75c7-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="c75c7-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="c75c7-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="c75c7-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75c7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c75c7-111">Return value</span></span>

<span data-ttu-id="c75c7-112">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c75c7-112">Returns one of the following values.</span></span>



| <span data-ttu-id="c75c7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c75c7-113">Return code</span></span>                                                                                           | <span data-ttu-id="c75c7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c75c7-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c75c7-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="c75c7-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c75c7-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="c75c7-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="c75c7-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c75c7-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="c75c7-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c75c7-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="c75c7-119"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="c75c7-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c75c7-120">Il filtro non è connesso.</span><span class="sxs-lookup"><span data-stu-id="c75c7-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c75c7-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c75c7-121">Remarks</span></span>

<span data-ttu-id="c75c7-122">Questo metodo copia il tipo di supporto nella struttura del **\_ \_ tipo di supporto am** specificata da *pType*.</span><span class="sxs-lookup"><span data-stu-id="c75c7-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="c75c7-123">Il chiamante deve liberare il blocco di formato del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c75c7-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="c75c7-124">È possibile usare la funzione **CoTaskMemFree** o la funzione [**FreeMediaType**](freemediatype.md) nella libreria di classi di base.</span><span class="sxs-lookup"><span data-stu-id="c75c7-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="c75c7-125">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c75c7-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c75c7-126">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c75c7-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c75c7-127">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c75c7-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c75c7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c75c7-128">Requirements</span></span>



| <span data-ttu-id="c75c7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c75c7-129">Requirement</span></span> | <span data-ttu-id="c75c7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c75c7-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c75c7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c75c7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c75c7-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c75c7-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c75c7-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="c75c7-133">Library</span></span><br/> | <dl> <span data-ttu-id="c75c7-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c75c7-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75c7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c75c7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c75c7-136">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="c75c7-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="c75c7-137">**Interfaccia ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="c75c7-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




