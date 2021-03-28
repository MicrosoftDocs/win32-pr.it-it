---
description: Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider cloud.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104995237"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="aca8d-103">Metodo IStorageProviderCopyHook:: CopyCallback</span><span class="sxs-lookup"><span data-stu-id="aca8d-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="aca8d-104">Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider cloud.</span><span class="sxs-lookup"><span data-stu-id="aca8d-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca8d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aca8d-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="aca8d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aca8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca8d-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-108">Handle per la finestra che deve essere utilizzato dal gestore dell'hook di copia come elemento padre per gli elementi dell'interfaccia utente che possono essere visualizzati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="aca8d-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="aca8d-109">Se **FOF_SILENT** è specificato nell' *operazione*, il metodo deve ignorare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="aca8d-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aca8d-110">*operazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-111">Operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="aca8d-111">The operation to perform.</span></span> <span data-ttu-id="aca8d-112">Questo parametro può essere uno dei valori elencati sotto il membro **wFunc** della struttura [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="aca8d-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aca8d-113">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-114">Flag che controllano l'operazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-114">The flags that control the operation.</span></span> <span data-ttu-id="aca8d-115">Questo parametro può essere uno o più dei valori elencati sotto il membro *fFlags* della struttura [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="aca8d-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="aca8d-116">Per gli hook di copia della stampante, questo valore corrisponde a uno dei valori seguenti definiti in Shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="aca8d-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="aca8d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="aca8d-117">Value</span></span>       | <span data-ttu-id="aca8d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aca8d-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="aca8d-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="aca8d-119">**PO_DELETE**</span></span>      | <span data-ttu-id="aca8d-120">È in corso l'eliminazione di una stampante.</span><span class="sxs-lookup"><span data-stu-id="aca8d-120">A printer is being deleted.</span></span> <span data-ttu-id="aca8d-121">Il parametro *SrcFile* punta al percorso completo della stampante specificata.</span><span class="sxs-lookup"><span data-stu-id="aca8d-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="aca8d-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="aca8d-122">**PO_RENAME**</span></span>       | <span data-ttu-id="aca8d-123">È in corso la ridenominazione di una stampante.</span><span class="sxs-lookup"><span data-stu-id="aca8d-123">A printer is being renamed.</span></span> <span data-ttu-id="aca8d-124">Il parametro *SrcFile* punta al nuovo nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="aca8d-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="aca8d-125">Il parametro *destFile* punta al nome precedente.</span><span class="sxs-lookup"><span data-stu-id="aca8d-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="aca8d-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="aca8d-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="aca8d-127">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="aca8d-127">Not supported.</span></span> <span data-ttu-id="aca8d-128">Non usare.</span><span class="sxs-lookup"><span data-stu-id="aca8d-128">Do not use.</span></span>          |
| <span data-ttu-id="aca8d-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="aca8d-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="aca8d-130">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="aca8d-130">Not supported.</span></span> <span data-ttu-id="aca8d-131">Non usare.</span><span class="sxs-lookup"><span data-stu-id="aca8d-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="aca8d-132">*SrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-133">Puntatore a una stringa che contiene il nome della cartella di origine.</span><span class="sxs-lookup"><span data-stu-id="aca8d-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="aca8d-134">*srcAttribs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-135">Attributi della cartella di origine.</span><span class="sxs-lookup"><span data-stu-id="aca8d-135">The attributes of the source folder.</span></span> <span data-ttu-id="aca8d-136">Questo parametro può essere una combinazione di qualsiasi flag di attributo file (FILE_ATTRIBUTE_ \*) definito nei file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="aca8d-137">Vedere [costanti degli attributi di file](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="aca8d-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="aca8d-138">*destFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-139">Puntatore a una stringa che contiene il nome della cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="aca8d-140">*destAttribs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-141">Attributi della cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-141">The attributes of the destination folder.</span></span> <span data-ttu-id="aca8d-142">Questo parametro può essere una combinazione di qualsiasi flag di attributo file (FILE_ATTRIBUTE_ \*) definito nei file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="aca8d-143">Vedere [costanti degli attributi di file](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="aca8d-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="aca8d-144">*risultato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aca8d-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aca8d-145">Valore intero che indica se la shell deve eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="aca8d-146">I tipi validi sono:</span><span class="sxs-lookup"><span data-stu-id="aca8d-146">One of the following:</span></span>

| <span data-ttu-id="aca8d-147">Valore</span><span class="sxs-lookup"><span data-stu-id="aca8d-147">Value</span></span>       | <span data-ttu-id="aca8d-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aca8d-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="aca8d-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="aca8d-149">**IDYES**</span></span>       | <span data-ttu-id="aca8d-150">Consente l'operazione.</span><span class="sxs-lookup"><span data-stu-id="aca8d-150">Allows the operation.</span></span>           |
| <span data-ttu-id="aca8d-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="aca8d-151">**IDNO**</span></span>        | <span data-ttu-id="aca8d-152">Impedisce l'operazione su questa cartella ma continua con altre operazioni approvate, ad esempio un'operazione di copia batch.</span><span class="sxs-lookup"><span data-stu-id="aca8d-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="aca8d-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="aca8d-153">**IDCANCEL**</span></span>    | <span data-ttu-id="aca8d-154">Impedisce l'operazione corrente e Annulla tutte le operazioni in sospeso.</span><span class="sxs-lookup"><span data-stu-id="aca8d-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="aca8d-155">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aca8d-155">Return value</span></span>

<span data-ttu-id="aca8d-156">Restituisce **S_OK** in caso di esito positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="aca8d-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aca8d-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="aca8d-157">Remarks</span></span>

<span data-ttu-id="aca8d-158">La shell chiama il gestore di hook di copia del provider cloud per ogni cartella sotto la radice di sincronizzazione registrata.</span><span class="sxs-lookup"><span data-stu-id="aca8d-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="aca8d-159">Per registrare un gestore di hook di copia per le cartelle Cloud, impostare il valore **CopyHook** nella chiave **HKEY_LOCAL_MACHINE/software/Microsoft/Windows/CurrentVersion/Explorer/syncrootmanager/{syncrootid}** sul CLSID dell'oggetto copia hook.</span><span class="sxs-lookup"><span data-stu-id="aca8d-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="aca8d-160">Quando viene chiamato il metodo **CopyCallback** , la shell Inizializza direttamente l'interfaccia [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) senza usare prima un'interfaccia [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .</span><span class="sxs-lookup"><span data-stu-id="aca8d-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca8d-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aca8d-161">Requirements</span></span>

| <span data-ttu-id="aca8d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca8d-162">Requirement</span></span> | <span data-ttu-id="aca8d-163">Valore</span><span class="sxs-lookup"><span data-stu-id="aca8d-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aca8d-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca8d-164">Minimum supported client</span></span> | <span data-ttu-id="aca8d-165">Windows 10 Insider Preview Build 19624</span><span class="sxs-lookup"><span data-stu-id="aca8d-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="aca8d-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aca8d-166">Header</span></span>                   | <span data-ttu-id="aca8d-167">ShObjIdl. h</span><span class="sxs-lookup"><span data-stu-id="aca8d-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="aca8d-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aca8d-168">See also</span></span>

[<span data-ttu-id="aca8d-169">Creare un motore di sincronizzazione cloud che supporti i file segnaposto</span><span class="sxs-lookup"><span data-stu-id="aca8d-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)