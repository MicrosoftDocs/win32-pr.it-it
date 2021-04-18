---
description: Il metodo SetSourceNameValidation specifica il modo in cui il motore di rendering convalida i nomi di file.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Metodo IRenderEngine:: SetSourceNameValidation (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330782"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="df015-103">Metodo IRenderEngine:: SetSourceNameValidation</span><span class="sxs-lookup"><span data-stu-id="df015-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="df015-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="df015-104">\[Deprecated.</span></span> <span data-ttu-id="df015-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df015-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="df015-106">Il `SetSourceNameValidation` metodo specifica il modo in cui il motore di rendering convalida i nomi di file.</span><span class="sxs-lookup"><span data-stu-id="df015-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="df015-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df015-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="df015-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df015-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df015-109">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="df015-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="df015-110">Valore **BSTR** contenente coppie di stringhe di filtro, formattato come richiesto dal membro **LpstrFilter** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="df015-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="df015-111">Il localizzatore multimediale usa questo filtro se presenta una finestra di dialogo Apri file per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="df015-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="df015-112">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="df015-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="df015-113">Puntatore facoltativo all'interfaccia [**IMediaLocator**](imedialocator.md) di un localizzatore multimediale da usare al posto del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="df015-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="df015-114">Per usare il localizzatore multimediale predefinito, impostare il valore di questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="df015-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="df015-115">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="df015-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="df015-116">*Flag*</span><span class="sxs-lookup"><span data-stu-id="df015-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="df015-117">Combinazione bit per bit dei [**flag di convalida dei nomi di file**](file-name-validation-flags.md) che specificano il comportamento del localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="df015-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="df015-118">Il \_ flag di controllo SFN VALIDATEF \_ deve essere presente.</span><span class="sxs-lookup"><span data-stu-id="df015-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="df015-119">Il \_ flag SFN VALIDATEF \_ hlinkMUTED non ha alcun effetto con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="df015-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df015-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df015-120">Return value</span></span>

<span data-ttu-id="df015-121">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="df015-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="df015-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="df015-122">Return code</span></span>                                                                                            | <span data-ttu-id="df015-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df015-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="df015-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df015-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="df015-125">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="df015-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="df015-126"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="df015-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="df015-127">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="df015-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df015-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="df015-128">Remarks</span></span>

<span data-ttu-id="df015-129">Utilizzando il parametro *pOverride* , è possibile fornire un'implementazione personalizzata dell'interfaccia [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="df015-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="df015-130">Ad esempio, il localizzatore multimediale predefinito non notifica a un'applicazione i file che trova (o non trova).</span><span class="sxs-lookup"><span data-stu-id="df015-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="df015-131">Per aggirare questa limitazione, è possibile implementare un localizzatore multimediale personalizzato, rendendolo un wrapper per la versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="df015-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="df015-132">Passare quindi le chiamate a [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) direttamente alla versione predefinita ed esaminare il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="df015-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="df015-133">Attualmente, questo metodo non convalida le origini caricate dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="df015-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="df015-134">Vedere [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="df015-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="df015-135">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="df015-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="df015-136">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="df015-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="df015-137">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="df015-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df015-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df015-138">Requirements</span></span>



| <span data-ttu-id="df015-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="df015-139">Requirement</span></span> | <span data-ttu-id="df015-140">Valore</span><span class="sxs-lookup"><span data-stu-id="df015-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df015-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df015-141">Header</span></span><br/>  | <dl> <span data-ttu-id="df015-142"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="df015-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="df015-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="df015-143">Library</span></span><br/> | <dl> <span data-ttu-id="df015-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df015-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df015-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df015-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df015-146">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="df015-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="df015-147">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="df015-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
