---
description: Il metodo WriteGrfFile scrive un grafico di filtro in un file in formato GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'Metodo IXml2Dex:: WriteGrfFile (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328454"
---
# <a name="ixml2dexwritegrffile-method"></a><span data-ttu-id="592b9-103">Metodo IXml2Dex:: WriteGrfFile</span><span class="sxs-lookup"><span data-stu-id="592b9-103">IXml2Dex::WriteGrfFile method</span></span>

> [!Note]  
> <span data-ttu-id="592b9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="592b9-104">\[Deprecated.</span></span> <span data-ttu-id="592b9-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="592b9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="592b9-106">Il `WriteGrfFile` metodo scrive un grafico di filtro in un file in formato. GRF.</span><span class="sxs-lookup"><span data-stu-id="592b9-106">The `WriteGrfFile` method writes a filter graph to a file in .grf format.</span></span>

## <a name="syntax"></a><span data-ttu-id="592b9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="592b9-107">Syntax</span></span>


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="592b9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="592b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="592b9-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="592b9-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="592b9-110">Puntatore all'interfaccia **IUnknown** del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="592b9-110">Pointer to the filter graph's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="592b9-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="592b9-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="592b9-112">Stringa che specifica il nome del file da scrivere.</span><span class="sxs-lookup"><span data-stu-id="592b9-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="592b9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="592b9-113">Return value</span></span>

<span data-ttu-id="592b9-114">Restituisce un valore **HRESULT** che dipende dall'implementazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="592b9-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="592b9-115">HRESULT può includere una delle seguenti costanti standard o altri valori non elencati.</span><span class="sxs-lookup"><span data-stu-id="592b9-115">HRESULT can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="592b9-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="592b9-116">Return code</span></span>                                                                                  | <span data-ttu-id="592b9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="592b9-117">Description</span></span>                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="592b9-118"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="592b9-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="592b9-119">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="592b9-119">Failure.</span></span><br/>             |
| <dl> <span data-ttu-id="592b9-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="592b9-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="592b9-121">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="592b9-121">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="592b9-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="592b9-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="592b9-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="592b9-123">Success.</span></span><br/>             |



 

<span data-ttu-id="592b9-124">Questo metodo può inoltre restituire i codici di errore generati dalle chiamate interne ai metodi **IStorage:: CreateStream** e **IPersist:: Save** .</span><span class="sxs-lookup"><span data-stu-id="592b9-124">This method can also return error codes generated by internal calls to the **IStorage::CreateStream** and **IPersist::Save** methods.</span></span> <span data-ttu-id="592b9-125">Per ulteriori informazioni, vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="592b9-125">For more information, see the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="592b9-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="592b9-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="592b9-127">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="592b9-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="592b9-128">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="592b9-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="592b9-129">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="592b9-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="592b9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="592b9-130">Requirements</span></span>



| <span data-ttu-id="592b9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="592b9-131">Requirement</span></span> | <span data-ttu-id="592b9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="592b9-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="592b9-133">Versione</span><span class="sxs-lookup"><span data-stu-id="592b9-133">Version</span></span><br/> | <span data-ttu-id="592b9-134">Internet Explorer 4,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="592b9-134">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="592b9-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="592b9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="592b9-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="592b9-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="592b9-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="592b9-137">Library</span></span><br/> | <dl> <span data-ttu-id="592b9-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="592b9-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592b9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="592b9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592b9-140">**Interfaccia IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="592b9-140">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="592b9-141">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="592b9-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




