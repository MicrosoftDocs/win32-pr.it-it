---
description: Il metodo WriteXML converte una sequenza temporale in una stringa XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'Metodo IXml2Dex:: WriteXML (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325293"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="4cfe2-103">Metodo IXml2Dex:: WriteXML</span><span class="sxs-lookup"><span data-stu-id="4cfe2-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="4cfe2-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-104">\[Deprecated.</span></span> <span data-ttu-id="4cfe2-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4cfe2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4cfe2-106">Il `WriteXML` metodo converte una sequenza temporale in una stringa XML.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfe2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cfe2-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="4cfe2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cfe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfe2-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="4cfe2-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="4cfe2-110">Puntatore all'interfaccia **IUnknown** dell'oggetto della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="4cfe2-111">*pbstrXML*</span><span class="sxs-lookup"><span data-stu-id="4cfe2-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="4cfe2-112">Puntatore a una variabile di tipo BSTR che riceve la stringa XML che descrive la sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfe2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cfe2-113">Return value</span></span>

<span data-ttu-id="4cfe2-114">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="4cfe2-115">Se la memoria non è sufficiente per la conversione, restituisce E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="4cfe2-116">In caso contrario, restituisce un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfe2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cfe2-117">Remarks</span></span>

<span data-ttu-id="4cfe2-118">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-118">The method allocates memory for the string.</span></span> <span data-ttu-id="4cfe2-119">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="4cfe2-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="4cfe2-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4cfe2-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4cfe2-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4cfe2-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4cfe2-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cfe2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cfe2-123">Requirements</span></span>



| <span data-ttu-id="4cfe2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfe2-124">Requirement</span></span> | <span data-ttu-id="4cfe2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4cfe2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfe2-126">Versione</span><span class="sxs-lookup"><span data-stu-id="4cfe2-126">Version</span></span><br/> | <span data-ttu-id="4cfe2-127">Internet Explorer 4,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4cfe2-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="4cfe2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cfe2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4cfe2-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfe2-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4cfe2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="4cfe2-130">Library</span></span><br/> | <dl> <span data-ttu-id="4cfe2-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cfe2-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cfe2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cfe2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfe2-133">**Interfaccia IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="4cfe2-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="4cfe2-134">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="4cfe2-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




