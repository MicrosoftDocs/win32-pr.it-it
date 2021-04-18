---
description: Il metodo FindMediaFile Cerca un file e, in caso di esito positivo, recupera il percorso del file.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'Metodo IMediaLocator:: FindMediaFile (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325300"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="96ca7-103">Metodo IMediaLocator:: FindMediaFile</span><span class="sxs-lookup"><span data-stu-id="96ca7-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="96ca7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="96ca7-104">\[Deprecated.</span></span> <span data-ttu-id="96ca7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96ca7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96ca7-106">Il `FindMediaFile` metodo cerca un file e, in caso di esito positivo, recupera il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="96ca7-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ca7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96ca7-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="96ca7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96ca7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ca7-109">*Input*</span><span class="sxs-lookup"><span data-stu-id="96ca7-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="96ca7-110">Nome del file, incluso il percorso, in cui si trovava l'ultima versione del file.</span><span class="sxs-lookup"><span data-stu-id="96ca7-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="96ca7-111">Per gli oggetti di origine nella sequenza temporale, usare il nome del supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="96ca7-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="96ca7-112">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="96ca7-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="96ca7-113">**BSTR** contenente coppie di stringhe di filtro, formattate come richiesto dal membro **LpstrFilter** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="96ca7-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="96ca7-114">Il localizzatore multimediale usa questo filtro se Visualizza una finestra di dialogo Apri file.</span><span class="sxs-lookup"><span data-stu-id="96ca7-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="96ca7-115">Il valore può essere **null** se il parametro *Flags* non include il \_ \_ flag popup SFN VALIDATEF.</span><span class="sxs-lookup"><span data-stu-id="96ca7-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="96ca7-116">*pOutput*</span><span class="sxs-lookup"><span data-stu-id="96ca7-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="96ca7-117">Puntatore a una variabile che riceve il percorso effettivo del file, se è diverso dal valore contenuto nell' *input* e se il metodo individua correttamente il file.</span><span class="sxs-lookup"><span data-stu-id="96ca7-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="96ca7-118">*Flag*</span><span class="sxs-lookup"><span data-stu-id="96ca7-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="96ca7-119">Combinazione bit per bit di zero o più flag.</span><span class="sxs-lookup"><span data-stu-id="96ca7-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="96ca7-120">Per un elenco di flag possibili, vedere [**flag di convalida dei nomi di file**](file-name-validation-flags.md).</span><span class="sxs-lookup"><span data-stu-id="96ca7-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ca7-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96ca7-121">Return value</span></span>

<span data-ttu-id="96ca7-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96ca7-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96ca7-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96ca7-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96ca7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="96ca7-124">Remarks</span></span>

<span data-ttu-id="96ca7-125">La stringa di filtro per la finestra di dialogo Apri file, specificata dal parametro *FilterString* , contiene caratteri null interni.</span><span class="sxs-lookup"><span data-stu-id="96ca7-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="96ca7-126">Ad esempio, \\ il video 0 \* . avi \\ 0 \\ 0 è una stringa di filtro valida.</span><span class="sxs-lookup"><span data-stu-id="96ca7-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="96ca7-127">Non è possibile usare la funzione **SysAllocStr** per allocare BSTR, perché tale funzione prevede una stringa con terminazione null e tronca la stringa in corrispondenza del primo carattere null.</span><span class="sxs-lookup"><span data-stu-id="96ca7-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="96ca7-128">Utilizzare pertanto una funzione come **SysAllocStringLen**, che include un parametro esplicito per la lunghezza:</span><span class="sxs-lookup"><span data-stu-id="96ca7-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="96ca7-129">Se l'utente annulla la finestra di dialogo Apri file, il metodo restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="96ca7-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="96ca7-130">Il metodo alloca memoria per **BSTR** in *pOutput*.</span><span class="sxs-lookup"><span data-stu-id="96ca7-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="96ca7-131">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="96ca7-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="96ca7-132">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="96ca7-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="96ca7-133">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="96ca7-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="96ca7-134">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="96ca7-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96ca7-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96ca7-135">Requirements</span></span>



| <span data-ttu-id="96ca7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ca7-136">Requirement</span></span> | <span data-ttu-id="96ca7-137">Valore</span><span class="sxs-lookup"><span data-stu-id="96ca7-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96ca7-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96ca7-138">Header</span></span><br/>  | <dl> <span data-ttu-id="96ca7-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ca7-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="96ca7-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="96ca7-140">Library</span></span><br/> | <dl> <span data-ttu-id="96ca7-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96ca7-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ca7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ca7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ca7-143">**Interfaccia IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="96ca7-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="96ca7-144">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="96ca7-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
