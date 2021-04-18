---
description: Il \_ metodo Get OffsetX recupera l'offset orizzontale del rettangolo di destinazione.
ms.assetid: a9d8c81b-f978-4b47-9c7f-12cee7c2c40d
title: 'Metodo IDxtCompositor:: get_OffsetX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8e2f21956e67b42158f4e646d33aa6e3e90d9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332193"
---
# <a name="idxtcompositorget_offsetx-method"></a><span data-ttu-id="8e3a6-103">Metodo IDxtCompositor:: Get \_ offsetX</span><span class="sxs-lookup"><span data-stu-id="8e3a6-103">IDxtCompositor::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="8e3a6-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-104">\[Deprecated.</span></span> <span data-ttu-id="8e3a6-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8e3a6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8e3a6-106">Il `get_OffsetX` metodo recupera l'offset orizzontale del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-106">The `get_OffsetX` method retrieves the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3a6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e3a6-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8e3a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e3a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e3a6-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8e3a6-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a6-110">Riceve l'offset orizzontale del rettangolo di destinazione, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-110">Receives the horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e3a6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e3a6-111">Return value</span></span>

<span data-ttu-id="8e3a6-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e3a6-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e3a6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3a6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e3a6-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8e3a6-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8e3a6-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e3a6-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8e3a6-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8e3a6-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e3a6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e3a6-118">Requirements</span></span>



| <span data-ttu-id="8e3a6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e3a6-119">Requirement</span></span> | <span data-ttu-id="8e3a6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8e3a6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3a6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e3a6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8e3a6-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e3a6-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8e3a6-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e3a6-123">Library</span></span><br/> | <dl> <span data-ttu-id="8e3a6-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e3a6-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e3a6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e3a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3a6-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="8e3a6-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




