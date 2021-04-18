---
description: Il \_ metodo Put SrcHeight specifica l'altezza del rettangolo di origine.
ms.assetid: 80c8cf92-36e2-4e57-8ce7-6a114bc8bab4
title: 'IDxtCompositor: metodo:p ut_SrcHeight (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 80697a3c4a159256389f48273e66ca86547478fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329143"
---
# <a name="idxtcompositorput_srcheight-method"></a><span data-ttu-id="22282-103">IDxtCompositor::p UT \_ SrcHeight metodo</span><span class="sxs-lookup"><span data-stu-id="22282-103">IDxtCompositor::put\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="22282-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="22282-104">\[Deprecated.</span></span> <span data-ttu-id="22282-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22282-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22282-106">Il `put_SrcHeight` metodo specifica l'altezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="22282-106">The `put_SrcHeight` method specifies the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="22282-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22282-107">Syntax</span></span>


```C++
HRESULT put_SrcHeight(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="22282-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="22282-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22282-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22282-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22282-110">Altezza, in pixel, del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="22282-110">The height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22282-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22282-111">Return value</span></span>

<span data-ttu-id="22282-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22282-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22282-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22282-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22282-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="22282-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="22282-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="22282-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22282-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="22282-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22282-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="22282-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22282-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22282-118">Requirements</span></span>



| <span data-ttu-id="22282-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="22282-119">Requirement</span></span> | <span data-ttu-id="22282-120">Valore</span><span class="sxs-lookup"><span data-stu-id="22282-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22282-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22282-121">Header</span></span><br/>  | <dl> <span data-ttu-id="22282-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="22282-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22282-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="22282-123">Library</span></span><br/> | <dl> <span data-ttu-id="22282-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22282-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22282-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22282-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22282-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="22282-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




