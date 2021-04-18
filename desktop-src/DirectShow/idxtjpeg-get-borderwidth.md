---
description: Il \_ metodo Get BorderWidth recupera la larghezza del bordo solido lungo i bordi del pattern di cancellazione.
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: 'Metodo IDxtJpeg:: get_BorderWidth (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28405c08d5666c8f182e0ffdb6ed1aa7bac599d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330643"
---
# <a name="idxtjpegget_borderwidth-method"></a><span data-ttu-id="38d6a-103">Metodo IDxtJpeg:: Get \_ BorderWidth</span><span class="sxs-lookup"><span data-stu-id="38d6a-103">IDxtJpeg::get\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="38d6a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="38d6a-104">\[Deprecated.</span></span> <span data-ttu-id="38d6a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38d6a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38d6a-106">Il `get_BorderWidth` metodo recupera la larghezza del bordo solido lungo i bordi del pattern di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="38d6a-106">The `get_BorderWidth` method retrieves the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d6a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38d6a-107">Syntax</span></span>


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="38d6a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="38d6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d6a-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="38d6a-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="38d6a-110">Riceve la larghezza del bordo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="38d6a-110">Receives the width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d6a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38d6a-111">Return value</span></span>

<span data-ttu-id="38d6a-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="38d6a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38d6a-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38d6a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d6a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="38d6a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="38d6a-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="38d6a-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38d6a-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="38d6a-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38d6a-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="38d6a-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38d6a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38d6a-118">Requirements</span></span>



| <span data-ttu-id="38d6a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="38d6a-119">Requirement</span></span> | <span data-ttu-id="38d6a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="38d6a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38d6a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38d6a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="38d6a-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="38d6a-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38d6a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="38d6a-123">Library</span></span><br/> | <dl> <span data-ttu-id="38d6a-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38d6a-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d6a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38d6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d6a-126">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="38d6a-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




