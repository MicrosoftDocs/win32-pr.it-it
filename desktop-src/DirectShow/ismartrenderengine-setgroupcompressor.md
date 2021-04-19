---
description: Specifica un filtro di compressione da usare quando si esegue il rendering del gruppo specificato.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Metodo ISmartRenderEngine:: SetGroupCompressor (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333431"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="742fb-103">Metodo ISmartRenderEngine:: SetGroupCompressor</span><span class="sxs-lookup"><span data-stu-id="742fb-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="742fb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="742fb-104">\[Deprecated.</span></span> <span data-ttu-id="742fb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="742fb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="742fb-106">Specifica un filtro di compressione da usare quando si esegue il rendering del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="742fb-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="742fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="742fb-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="742fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="742fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="742fb-109">*Gruppo*</span><span class="sxs-lookup"><span data-stu-id="742fb-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="742fb-110">Indice in base zero del gruppo.</span><span class="sxs-lookup"><span data-stu-id="742fb-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="742fb-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="742fb-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="742fb-112">Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di compressione.</span><span class="sxs-lookup"><span data-stu-id="742fb-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="742fb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="742fb-113">Return value</span></span>

<span data-ttu-id="742fb-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="742fb-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="742fb-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="742fb-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="742fb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="742fb-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="742fb-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="742fb-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="742fb-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="742fb-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="742fb-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="742fb-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="742fb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="742fb-120">Requirements</span></span>



| <span data-ttu-id="742fb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="742fb-121">Requirement</span></span> | <span data-ttu-id="742fb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="742fb-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="742fb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="742fb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="742fb-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="742fb-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="742fb-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="742fb-125">Library</span></span><br/> | <dl> <span data-ttu-id="742fb-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="742fb-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="742fb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="742fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742fb-128">**Interfaccia ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="742fb-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="742fb-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="742fb-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




