---
description: Il \_ metodo Get InputSize restituisce le dimensioni di input correnti del filtro Resizer.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Metodo IResize:: get_InputSize (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332570"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="0d441-103">Metodo IResize:: Get \_ InputSize</span><span class="sxs-lookup"><span data-stu-id="0d441-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="0d441-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0d441-104">\[Deprecated.</span></span> <span data-ttu-id="0d441-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d441-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d441-106">Il `get_InputSize` metodo restituisce le dimensioni di input correnti del filtro Resizer.</span><span class="sxs-lookup"><span data-stu-id="0d441-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d441-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d441-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="0d441-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d441-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d441-109">*piHeight* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d441-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d441-110">Riceve l'altezza del video in pixel.</span><span class="sxs-lookup"><span data-stu-id="0d441-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0d441-111">*piWidth* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0d441-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d441-112">Riceve la larghezza del video in pixel.</span><span class="sxs-lookup"><span data-stu-id="0d441-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d441-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d441-113">Return value</span></span>

<span data-ttu-id="0d441-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d441-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d441-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d441-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d441-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d441-116">Remarks</span></span>

<span data-ttu-id="0d441-117">Se il pin di input del filtro non è connesso, restituire un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="0d441-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="0d441-118">In caso contrario, restituire la larghezza e l'altezza del video, come specificato dal tipo di supporto del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="0d441-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="0d441-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0d441-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0d441-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d441-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0d441-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0d441-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d441-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d441-122">Requirements</span></span>



| <span data-ttu-id="0d441-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d441-123">Requirement</span></span> | <span data-ttu-id="0d441-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0d441-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d441-125">Versione</span><span class="sxs-lookup"><span data-stu-id="0d441-125">Version</span></span><br/> | <span data-ttu-id="0d441-126">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0d441-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="0d441-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d441-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0d441-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d441-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d441-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d441-129">Library</span></span><br/> | <dl> <span data-ttu-id="0d441-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d441-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d441-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d441-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d441-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="0d441-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="0d441-133">**Interfaccia IResize**</span><span class="sxs-lookup"><span data-stu-id="0d441-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




