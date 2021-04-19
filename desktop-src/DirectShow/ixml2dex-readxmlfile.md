---
description: Il metodo ReadXMLFile carica un file di progetto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'Metodo IXml2Dex:: ReadXMLFile (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332637"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="1cf45-103">Metodo IXml2Dex:: ReadXMLFile</span><span class="sxs-lookup"><span data-stu-id="1cf45-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="1cf45-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1cf45-104">\[Deprecated.</span></span> <span data-ttu-id="1cf45-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1cf45-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1cf45-106">Il `ReadXMLFile` metodo carica un file di progetto XML.</span><span class="sxs-lookup"><span data-stu-id="1cf45-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="1cf45-107">Questo metodo consente di creare istanze di tutti gli oggetti espressi nel file XML e di inserirli nella sequenza temporale, nonché di applicare gli attributi specificati per la sequenza temporale, ad esempio la frequenza dei fotogrammi o l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="1cf45-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf45-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cf45-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="1cf45-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cf45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf45-110">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="1cf45-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf45-111">Puntatore all'interfaccia **IUnknown** di un oggetto della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="1cf45-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="1cf45-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="1cf45-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf45-113">Stringa che specifica il nome del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="1cf45-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cf45-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cf45-114">Return value</span></span>

<span data-ttu-id="1cf45-115">Restituisce un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1cf45-115">Returns an HRESULT value.</span></span> <span data-ttu-id="1cf45-116">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="1cf45-116">Possible values include the following.</span></span>



| <span data-ttu-id="1cf45-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1cf45-117">Return code</span></span>                                                                                                  | <span data-ttu-id="1cf45-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cf45-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1cf45-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1cf45-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="1cf45-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="1cf45-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="1cf45-121"><dt>**\_formato file VFW E \_ non valido \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cf45-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="1cf45-122">Formato di file non valido</span><span class="sxs-lookup"><span data-stu-id="1cf45-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1cf45-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cf45-123">Remarks</span></span>

<span data-ttu-id="1cf45-124">Questo metodo non cancella gli oggetti esistenti dalla sequenza temporale prima di inserire i nuovi oggetti definiti nel file XML.</span><span class="sxs-lookup"><span data-stu-id="1cf45-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="1cf45-125">Se è necessario aggiornare una sequenza temporale esistente, chiamare prima [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf45-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="1cf45-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="1cf45-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1cf45-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1cf45-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1cf45-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1cf45-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1cf45-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cf45-129">Requirements</span></span>



| <span data-ttu-id="1cf45-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf45-130">Requirement</span></span> | <span data-ttu-id="1cf45-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1cf45-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf45-132">Versione</span><span class="sxs-lookup"><span data-stu-id="1cf45-132">Version</span></span><br/> | <span data-ttu-id="1cf45-133">Internet Explorer 4,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1cf45-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="1cf45-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cf45-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1cf45-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf45-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1cf45-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cf45-136">Library</span></span><br/> | <dl> <span data-ttu-id="1cf45-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cf45-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf45-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cf45-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf45-139">**Interfaccia IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="1cf45-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="1cf45-140">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1cf45-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




