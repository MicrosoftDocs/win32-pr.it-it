---
description: Il \_ metodo Put BorderWidth specifica la larghezza del bordo solido lungo i bordi del pattern di cancellazione.
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: 'IDxtJpeg: metodo:p ut_BorderWidth (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df7435b8a516b818b6d7c86e907ba75cce86f6c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332188"
---
# <a name="idxtjpegput_borderwidth-method"></a><span data-ttu-id="313d0-103">IDxtJpeg::p UT \_ BorderWidth (metodo)</span><span class="sxs-lookup"><span data-stu-id="313d0-103">IDxtJpeg::put\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="313d0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="313d0-104">\[Deprecated.</span></span> <span data-ttu-id="313d0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="313d0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="313d0-106">Il `put_BorderWidth` metodo specifica la larghezza del bordo solido lungo i bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="313d0-106">The `put_BorderWidth` method specifies the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="313d0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="313d0-107">Syntax</span></span>


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="313d0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="313d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313d0-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="313d0-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="313d0-110">Larghezza, in pixel, del bordo.</span><span class="sxs-lookup"><span data-stu-id="313d0-110">The width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313d0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="313d0-111">Return value</span></span>

<span data-ttu-id="313d0-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="313d0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="313d0-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="313d0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="313d0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="313d0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="313d0-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="313d0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="313d0-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="313d0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="313d0-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="313d0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="313d0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="313d0-118">Requirements</span></span>



| <span data-ttu-id="313d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="313d0-119">Requirement</span></span> | <span data-ttu-id="313d0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="313d0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="313d0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="313d0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="313d0-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="313d0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="313d0-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="313d0-123">Library</span></span><br/> | <dl> <span data-ttu-id="313d0-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="313d0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313d0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="313d0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313d0-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="313d0-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




