---
description: Il \_ metodo get Width recupera la larghezza del rettangolo di destinazione.
ms.assetid: 023c976e-279e-489c-ada5-ae33144c6358
title: 'Metodo IDxtCompositor:: get_Width (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_Width
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8f7b18e4cc02b28284f8ce680a7de04eaf8c9b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330644"
---
# <a name="idxtcompositorget_width-method"></a><span data-ttu-id="6233c-103">Metodo IDxtCompositor:: Get \_ Width</span><span class="sxs-lookup"><span data-stu-id="6233c-103">IDxtCompositor::get\_Width method</span></span>

> [!Note]  
> <span data-ttu-id="6233c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6233c-104">\[Deprecated.</span></span> <span data-ttu-id="6233c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6233c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6233c-106">Il `get_Width` metodo recupera la larghezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6233c-106">The `get_Width` method retrieves the width of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6233c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6233c-107">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6233c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6233c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6233c-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6233c-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6233c-110">Riceve la larghezza, in pixel, del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6233c-110">Receives the width of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6233c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6233c-111">Return value</span></span>

<span data-ttu-id="6233c-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6233c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6233c-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6233c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6233c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6233c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6233c-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6233c-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6233c-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6233c-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6233c-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6233c-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6233c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6233c-118">Requirements</span></span>



| <span data-ttu-id="6233c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6233c-119">Requirement</span></span> | <span data-ttu-id="6233c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6233c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6233c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6233c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6233c-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6233c-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6233c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6233c-123">Library</span></span><br/> | <dl> <span data-ttu-id="6233c-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6233c-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6233c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6233c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6233c-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="6233c-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




