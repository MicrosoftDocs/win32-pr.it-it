---
description: Il metodo WriteXMLFile converte una sequenza temporale in XML e scrive i dati XML in un file.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'Metodo IXml2Dex:: WriteXMLFile (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332566"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="f28fb-103">Metodo IXml2Dex:: WriteXMLFile</span><span class="sxs-lookup"><span data-stu-id="f28fb-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="f28fb-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f28fb-104">\[Deprecated.</span></span> <span data-ttu-id="f28fb-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f28fb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f28fb-106">Il `WriteXMLFile` metodo converte una sequenza temporale in XML e scrive i dati XML in un file.</span><span class="sxs-lookup"><span data-stu-id="f28fb-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f28fb-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="f28fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f28fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f28fb-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="f28fb-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="f28fb-110">Puntatore all'interfaccia **IUnknown** dell'oggetto della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="f28fb-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="f28fb-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="f28fb-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="f28fb-112">Stringa che specifica il nome del file da scrivere.</span><span class="sxs-lookup"><span data-stu-id="f28fb-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f28fb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f28fb-113">Return value</span></span>

<span data-ttu-id="f28fb-114">Restituisce un valore **HRESULT** che dipende dall'implementazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f28fb-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="f28fb-115">**HRESULT** può includere una delle seguenti costanti standard o altri valori non elencati.</span><span class="sxs-lookup"><span data-stu-id="f28fb-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="f28fb-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f28fb-116">Return code</span></span>                                                                                   | <span data-ttu-id="f28fb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f28fb-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="f28fb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f28fb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f28fb-119">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="f28fb-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="f28fb-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f28fb-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f28fb-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f28fb-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="f28fb-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f28fb-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f28fb-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f28fb-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f28fb-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f28fb-124">Remarks</span></span>

<span data-ttu-id="f28fb-125">Questo metodo genera un file XML che rappresenta tutti i componenti nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="f28fb-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="f28fb-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f28fb-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f28fb-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f28fb-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f28fb-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f28fb-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f28fb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f28fb-129">Requirements</span></span>



| <span data-ttu-id="f28fb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f28fb-130">Requirement</span></span> | <span data-ttu-id="f28fb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f28fb-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f28fb-132">Versione</span><span class="sxs-lookup"><span data-stu-id="f28fb-132">Version</span></span><br/> | <span data-ttu-id="f28fb-133">Internet Explorer 4,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f28fb-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="f28fb-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f28fb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f28fb-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f28fb-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f28fb-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f28fb-136">Library</span></span><br/> | <dl> <span data-ttu-id="f28fb-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f28fb-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f28fb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f28fb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28fb-139">**Interfaccia IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="f28fb-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="f28fb-140">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f28fb-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




