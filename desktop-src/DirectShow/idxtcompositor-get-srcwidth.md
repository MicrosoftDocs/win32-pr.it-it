---
description: Il \_ metodo Get SrcWidth recupera la larghezza del rettangolo di origine.
ms.assetid: 373bb108-5f0b-47f3-a39a-ed43b536e612
title: 'Metodo IDxtCompositor:: get_SrcWidth (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abd368c32b11b064f37c5c416cd944ee999272b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330647"
---
# <a name="idxtcompositorget_srcwidth-method"></a><span data-ttu-id="0fb70-103">Metodo IDxtCompositor:: Get \_ SrcWidth</span><span class="sxs-lookup"><span data-stu-id="0fb70-103">IDxtCompositor::get\_SrcWidth method</span></span>

> [!Note]  
> <span data-ttu-id="0fb70-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0fb70-104">\[Deprecated.</span></span> <span data-ttu-id="0fb70-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0fb70-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0fb70-106">Il `get_SrcWidth` metodo recupera la larghezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="0fb70-106">The `get_SrcWidth` method retrieves the width of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb70-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fb70-107">Syntax</span></span>


```C++
HRESULT get_SrcWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0fb70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fb70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb70-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0fb70-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb70-110">Riceve la larghezza, in pixel, del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="0fb70-110">Receives the width of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb70-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fb70-111">Return value</span></span>

<span data-ttu-id="0fb70-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0fb70-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0fb70-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0fb70-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fb70-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fb70-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0fb70-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0fb70-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0fb70-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0fb70-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0fb70-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0fb70-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fb70-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fb70-118">Requirements</span></span>



| <span data-ttu-id="0fb70-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fb70-119">Requirement</span></span> | <span data-ttu-id="0fb70-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0fb70-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb70-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fb70-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0fb70-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb70-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0fb70-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="0fb70-123">Library</span></span><br/> | <dl> <span data-ttu-id="0fb70-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fb70-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb70-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fb70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb70-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="0fb70-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




