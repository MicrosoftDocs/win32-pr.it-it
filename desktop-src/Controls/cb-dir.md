---
title: Messaggio CB_DIR (winuser. h)
description: Aggiunge nomi all'elenco visualizzato dalla casella combinata. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file. \_Il dir dir può anche aggiungere lettere di unità mappate all'elenco.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- Controlli di Windows Message CB_DIR
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873805"
---
# <a name="cb_dir-message"></a><span data-ttu-id="51631-106">\_Messaggio dir CB</span><span class="sxs-lookup"><span data-stu-id="51631-106">CB\_DIR message</span></span>

<span data-ttu-id="51631-107">Aggiunge nomi all'elenco visualizzato dalla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="51631-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="51631-108">Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file.</span><span class="sxs-lookup"><span data-stu-id="51631-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="51631-109">**CB \_ DIR** può anche aggiungere lettere di unità mappate all'elenco.</span><span class="sxs-lookup"><span data-stu-id="51631-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="51631-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="51631-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51631-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51631-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51631-112">Attributi dei file o delle directory da aggiungere alla casella combinata.</span><span class="sxs-lookup"><span data-stu-id="51631-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="51631-113">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="51631-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="51631-114">Valore</span><span class="sxs-lookup"><span data-stu-id="51631-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="51631-115">Significato</span><span class="sxs-lookup"><span data-stu-id="51631-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="51631-116"><dt>**\_Archivio DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="51631-117">Include i file archiviati.</span><span class="sxs-lookup"><span data-stu-id="51631-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="51631-118"><dt>**\_directory DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="51631-119">Include le sottodirectory, racchiuse tra parentesi quadre ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="51631-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="51631-120"><dt>**\_unità DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="51631-121">Tutte le unità mappate vengono aggiunte all'elenco.</span><span class="sxs-lookup"><span data-stu-id="51631-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="51631-122">Le unità sono elencate nel formato \[ - *x* - \] , dove *x* è la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="51631-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="51631-123"><dt>**\_esclusiva DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="51631-124">Include solo i file con gli attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="51631-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="51631-125">Per impostazione predefinita, i file di lettura/scrittura sono elencati anche se DDL \_ ReadWrite non è specificato.</span><span class="sxs-lookup"><span data-stu-id="51631-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="51631-126"><dt>**DDL \_ nascosto**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="51631-127">Include i file nascosti.</span><span class="sxs-lookup"><span data-stu-id="51631-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="51631-128"><dt>**sola \_ lettura DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="51631-129">Include i file di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="51631-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="51631-130"><dt>**\_ReadWrite DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="51631-131">Include i file di lettura/scrittura senza attributi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="51631-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="51631-132">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="51631-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="51631-133"><dt>**\_sistema DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="51631-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="51631-134">Include i file di sistema.</span><span class="sxs-lookup"><span data-stu-id="51631-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="51631-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51631-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51631-136">Puntatore **LPCTSTR** a una stringa con terminazione null che specifica un percorso assoluto, un percorso relativo o un nome file.</span><span class="sxs-lookup"><span data-stu-id="51631-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="51631-137">Un percorso assoluto può iniziare con una lettera di unità (ad esempio, d: \) o un nome UNC, ad esempio \\ \\ *machineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="51631-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="51631-138">Se la stringa specifica un nome file o una directory con gli attributi specificati dal parametro *wParam* , il nome file o la directory viene aggiunta all'elenco.</span><span class="sxs-lookup"><span data-stu-id="51631-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="51631-139">Se il nome file o il nome della directory contiene caratteri jolly (?</span><span class="sxs-lookup"><span data-stu-id="51631-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="51631-140">o \* ), tutti i file o le directory che corrispondono all'espressione con caratteri jolly e che hanno gli attributi specificati dal parametro *wParam* vengono aggiunti all'elenco visualizzato nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="51631-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51631-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51631-141">Return value</span></span>

<span data-ttu-id="51631-142">Se il messaggio ha esito positivo, il valore restituito è l'indice in base zero del cognome aggiunto all'elenco.</span><span class="sxs-lookup"><span data-stu-id="51631-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="51631-143">Se si verifica un errore, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="51631-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="51631-144">Se non è disponibile spazio sufficiente per archiviare le nuove stringhe, il valore restituito è CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="51631-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="51631-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="51631-145">Remarks</span></span>

<span data-ttu-id="51631-146">Se *wParam* include il \_ flag di directory DDL e *lParam* specifica tutte le sottodirectory di una directory di primo livello, ad esempio C: \\ temp \\ \* , nella casella di riepilogo viene sempre inclusa una voce ".." per la directory radice.</span><span class="sxs-lookup"><span data-stu-id="51631-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="51631-147">Questo vale anche se la directory radice contiene attributi di sistema o nascosti e i \_ flag DDL Hidden e DDL \_ System non sono specificati.</span><span class="sxs-lookup"><span data-stu-id="51631-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="51631-148">La directory radice di un volume NTFS presenta gli attributi nascosti e di sistema.</span><span class="sxs-lookup"><span data-stu-id="51631-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="51631-149">L'elenco Visualizza i nomi di file lunghi, se presenti.</span><span class="sxs-lookup"><span data-stu-id="51631-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="51631-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51631-150">Requirements</span></span>



| <span data-ttu-id="51631-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="51631-151">Requirement</span></span> | <span data-ttu-id="51631-152">Valore</span><span class="sxs-lookup"><span data-stu-id="51631-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51631-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51631-153">Minimum supported client</span></span><br/> | <span data-ttu-id="51631-154">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51631-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="51631-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51631-155">Minimum supported server</span></span><br/> | <span data-ttu-id="51631-156">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51631-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51631-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51631-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="51631-158"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51631-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51631-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51631-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="51631-160">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="51631-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51631-161">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="51631-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="51631-162">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="51631-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="51631-163">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="51631-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





