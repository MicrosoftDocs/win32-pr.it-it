---
title: Messaggio LB_DIR (winuser. h)
description: Aggiunge nomi all'elenco visualizzato da una casella di riepilogo. Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file. LB \_ dir può anche aggiungere lettere di unità mappate alla casella di riepilogo.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- Controlli di Windows Message LB_DIR
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121318"
---
# <a name="lb_dir-message"></a><span data-ttu-id="7b195-106">\_Messaggio dir lb</span><span class="sxs-lookup"><span data-stu-id="7b195-106">LB\_DIR message</span></span>

<span data-ttu-id="7b195-107">Aggiunge nomi all'elenco visualizzato da una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7b195-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="7b195-108">Il messaggio aggiunge i nomi delle directory e dei file che corrispondono a una stringa specificata e a un set di attributi di file.</span><span class="sxs-lookup"><span data-stu-id="7b195-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="7b195-109">**Lb \_ DIR** può anche aggiungere lettere di unità mappate alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7b195-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b195-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b195-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b195-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b195-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b195-112">Attributi dei file o delle directory da aggiungere alla casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7b195-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="7b195-113">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b195-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="7b195-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7b195-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="7b195-115">Significato</span><span class="sxs-lookup"><span data-stu-id="7b195-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="7b195-116"><dt>**\_Archivio DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="7b195-117">Include i file archiviati.</span><span class="sxs-lookup"><span data-stu-id="7b195-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="7b195-118"><dt>**\_directory DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="7b195-119">Include le sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="7b195-119">Includes subdirectories.</span></span> <span data-ttu-id="7b195-120">I nomi delle sottodirectory sono racchiusi tra parentesi quadre ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="7b195-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="7b195-121"><dt>**\_unità DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="7b195-122">Tutte le unità mappate vengono aggiunte all'elenco.</span><span class="sxs-lookup"><span data-stu-id="7b195-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="7b195-123">Le unità sono elencate nel formato \[ - *x* - \] , dove *x* è la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="7b195-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="7b195-124"><dt>**\_esclusiva DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="7b195-125">Include solo i file con gli attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="7b195-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="7b195-126">Per impostazione predefinita, i file di lettura/scrittura sono elencati anche se DDL \_ ReadWrite non è specificato.</span><span class="sxs-lookup"><span data-stu-id="7b195-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="7b195-127"><dt>**DDL \_ nascosto**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="7b195-128">Include i file nascosti.</span><span class="sxs-lookup"><span data-stu-id="7b195-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="7b195-129"><dt>**sola \_ lettura DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="7b195-130">Include i file di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7b195-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="7b195-131"><dt>**\_ReadWrite DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="7b195-132">Include i file di lettura/scrittura senza attributi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="7b195-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="7b195-133">Si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7b195-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="7b195-134"><dt>**\_sistema DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="7b195-135">Include i file di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b195-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="7b195-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b195-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b195-137">Puntatore alla stringa con terminazione null che specifica un percorso assoluto, un percorso relativo o un nome di file.</span><span class="sxs-lookup"><span data-stu-id="7b195-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="7b195-138">Un percorso assoluto può iniziare con una lettera di unità (ad esempio, d: \) o un nome UNC, ad esempio \\ \\ *machineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="7b195-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="7b195-139">Se la stringa specifica un nome file o una directory con gli attributi specificati dal parametro *wParam* , il nome file o la directory viene aggiunta all'elenco.</span><span class="sxs-lookup"><span data-stu-id="7b195-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="7b195-140">Se il nome del file o della directory contiene caratteri jolly (?</span><span class="sxs-lookup"><span data-stu-id="7b195-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="7b195-141">o \* ), all'elenco vengono aggiunti tutti i file o le directory che corrispondono all'espressione con caratteri jolly e che hanno gli attributi specificati dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="7b195-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b195-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b195-142">Return value</span></span>

<span data-ttu-id="7b195-143">Se il messaggio ha esito positivo, il valore restituito è l'indice in base zero del cognome aggiunto all'elenco.</span><span class="sxs-lookup"><span data-stu-id="7b195-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="7b195-144">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="7b195-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="7b195-145">Se non è disponibile spazio sufficiente per archiviare le nuove stringhe, il valore restituito è LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="7b195-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b195-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b195-146">Remarks</span></span>

<span data-ttu-id="7b195-147">Il messaggio [**lb \_ INITSTORAGE**](lb-initstorage.md) consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100).</span><span class="sxs-lookup"><span data-stu-id="7b195-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="7b195-148">Si riserva la quantità di memoria specificata in modo che i messaggi di **lb \_ dir** successivi prendano il minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="7b195-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="7b195-149">È possibile utilizzare le stime per i parametri *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="7b195-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="7b195-150">Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.</span><span class="sxs-lookup"><span data-stu-id="7b195-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="7b195-151">Se *wParam* include il \_ flag di directory DDL e *lParam* specifica tutte le sottodirectory di una directory di primo livello, ad esempio C: \\ temp \\ \* , nella casella di riepilogo viene sempre inclusa una voce ".." per la directory radice.</span><span class="sxs-lookup"><span data-stu-id="7b195-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="7b195-152">Questo vale anche se la directory radice contiene attributi di sistema o nascosti e i \_ flag DDL Hidden e DDL \_ System non sono specificati.</span><span class="sxs-lookup"><span data-stu-id="7b195-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="7b195-153">La directory radice di un volume NTFS presenta gli attributi nascosti e di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b195-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="7b195-154">L'elenco Visualizza i nomi di file lunghi, se presenti.</span><span class="sxs-lookup"><span data-stu-id="7b195-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="7b195-155">Per un'applicazione ANSI, il sistema converte il testo in una casella di riepilogo in formato Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="7b195-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="7b195-156">Ciò può causare problemi.</span><span class="sxs-lookup"><span data-stu-id="7b195-156">This can cause problems.</span></span> <span data-ttu-id="7b195-157">Ad esempio, i caratteri romani accentati in una casella di riepilogo non Unicode nelle finestre giapponesi verranno disattivati.</span><span class="sxs-lookup"><span data-stu-id="7b195-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="7b195-158">Per risolvere questo problema, compilare l'applicazione come Unicode o utilizzare una casella di riepilogo creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="7b195-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b195-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b195-159">Requirements</span></span>



| <span data-ttu-id="7b195-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b195-160">Requirement</span></span> | <span data-ttu-id="7b195-161">Valore</span><span class="sxs-lookup"><span data-stu-id="7b195-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b195-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b195-162">Minimum supported client</span></span><br/> | <span data-ttu-id="7b195-163">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b195-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b195-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b195-164">Minimum supported server</span></span><br/> | <span data-ttu-id="7b195-165">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b195-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7b195-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b195-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b195-167"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b195-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b195-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b195-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b195-169">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="7b195-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





