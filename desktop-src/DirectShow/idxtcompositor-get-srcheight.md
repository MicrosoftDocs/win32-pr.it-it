---
description: Il \_ metodo Get SrcHeight recupera l'altezza del rettangolo di origine.
ms.assetid: 3c6647b3-dfca-490d-a3d5-9aa6988e387d
title: 'Metodo IDxtCompositor:: get_SrcHeight (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3ad874d7c02a9c9300af7fe3dbc69f6d351bba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330654"
---
# <a name="idxtcompositorget_srcheight-method"></a><span data-ttu-id="f6998-103">Metodo IDxtCompositor:: Get \_ SrcHeight</span><span class="sxs-lookup"><span data-stu-id="f6998-103">IDxtCompositor::get\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="f6998-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f6998-104">\[Deprecated.</span></span> <span data-ttu-id="f6998-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f6998-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f6998-106">Il `get_SrcHeight` metodo recupera l'altezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f6998-106">The `get_SrcHeight` method retrieves the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6998-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6998-107">Syntax</span></span>


```C++
HRESULT get_SrcHeight(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f6998-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6998-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6998-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f6998-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f6998-110">Riceve l'altezza, in pixel, del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f6998-110">Receives the height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6998-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6998-111">Return value</span></span>

<span data-ttu-id="f6998-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f6998-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6998-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6998-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6998-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6998-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f6998-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f6998-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f6998-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6998-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f6998-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f6998-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6998-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6998-118">Requirements</span></span>



| <span data-ttu-id="f6998-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6998-119">Requirement</span></span> | <span data-ttu-id="f6998-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f6998-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6998-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6998-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f6998-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6998-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f6998-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6998-123">Library</span></span><br/> | <dl> <span data-ttu-id="f6998-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6998-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6998-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6998-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6998-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="f6998-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




