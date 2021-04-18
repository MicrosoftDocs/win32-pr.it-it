---
description: Il \_ metodo Get SrcOffsetX recupera l'offset orizzontale del rettangolo di origine.
ms.assetid: 528a5306-86bd-4ae2-ad03-57247362c5b5
title: 'Metodo IDxtCompositor:: get_SrcOffsetX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcOffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ee116537061986a556854aed093b5e9a414016e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330655"
---
# <a name="idxtcompositorget_srcoffsetx-method"></a><span data-ttu-id="8a4c0-103">Metodo IDxtCompositor:: Get \_ SrcOffsetX</span><span class="sxs-lookup"><span data-stu-id="8a4c0-103">IDxtCompositor::get\_SrcOffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="8a4c0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8a4c0-104">\[Deprecated.</span></span> <span data-ttu-id="8a4c0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8a4c0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8a4c0-106">Il `get_SrcOffsetX` metodo recupera l'offset orizzontale del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="8a4c0-106">The `get_SrcOffsetX` method retrieves the horizontal offset of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4c0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a4c0-107">Syntax</span></span>


```C++
HRESULT get_SrcOffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8a4c0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a4c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a4c0-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8a4c0-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4c0-110">Riceve l'offset orizzontale del rettangolo di origine, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="8a4c0-110">Receives the horizontal offset of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a4c0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a4c0-111">Return value</span></span>

<span data-ttu-id="8a4c0-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8a4c0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a4c0-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a4c0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a4c0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a4c0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8a4c0-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8a4c0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8a4c0-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a4c0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8a4c0-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8a4c0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a4c0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a4c0-118">Requirements</span></span>



| <span data-ttu-id="8a4c0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a4c0-119">Requirement</span></span> | <span data-ttu-id="8a4c0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8a4c0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4c0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a4c0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8a4c0-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a4c0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8a4c0-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a4c0-123">Library</span></span><br/> | <dl> <span data-ttu-id="8a4c0-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a4c0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a4c0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a4c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4c0-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="8a4c0-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




