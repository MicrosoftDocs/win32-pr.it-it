---
description: I metodi usati per lavorare con i file DirectX. x possono restituire i valori seguenti oltre ai valori restituiti standard COM. Deprecato.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Valori restituiti (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762131"
---
# <a name="return-values-dxfileh"></a><span data-ttu-id="c33fc-104">Valori restituiti (DXFile. h)</span><span class="sxs-lookup"><span data-stu-id="c33fc-104">Return Values (DXFile.h)</span></span>

<span data-ttu-id="c33fc-105">I metodi usati per lavorare con i file DirectX. x possono restituire i valori seguenti oltre ai valori restituiti standard COM.</span><span class="sxs-lookup"><span data-stu-id="c33fc-105">The methods used to work with DirectX .x files can return the following values in addition to the standard COM return values.</span></span> <span data-ttu-id="c33fc-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c33fc-106">Deprecated.</span></span>

<dl> <dt>

<span data-ttu-id="c33fc-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ OK**</span><span class="sxs-lookup"><span data-stu-id="c33fc-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-108">Comando completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c33fc-108">Command completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**\_BADALLOC DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR\_BADALLOC**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-110">L'allocazione di memoria ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c33fc-110">Memory allocation failed.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**\_BADARRAYSIZE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR\_BADARRAYSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-112">La dimensione della matrice non è valida.</span><span class="sxs-lookup"><span data-stu-id="c33fc-112">Array size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**\_BADCACHEFILE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR\_BADCACHEFILE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-114">Il file di cache contenente la data del file con estensione x non è valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-114">The cache file containing the .x file date is invalid.</span></span> <span data-ttu-id="c33fc-115">Un file di cache contiene i dati recuperati dalla rete, memorizzati nella cache sul disco rigido e recuperati nelle richieste successive.</span><span class="sxs-lookup"><span data-stu-id="c33fc-115">A cache file contains data retrieved from the network, cached on the hard disk, and retrieved in subsequent requests.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**\_BADDATAREFERENCE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR\_BADDataReference**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-117">Riferimento ai dati non valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-117">Data reference is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**\_BadFile DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR\_BADFILE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-119">Il file non è valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-119">File is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**\_BADFILECOMPRESSIONTYPE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR\_BADFILECOMPRESSIONTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-121">Il tipo di compressione del file non è valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-121">File compression type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**\_BADFILEFLOATSIZE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR\_BADFILEFLOATSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-123">Le dimensioni a virgola mobile non sono valide.</span><span class="sxs-lookup"><span data-stu-id="c33fc-123">Floating-point size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**\_BADFILETYPE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR\_BADFILETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-125">Il file non è un file DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="c33fc-125">File is not a DirectX .x file.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**\_BADFILEVERSION DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR\_BADFILEVERSION**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-127">La versione del file non è valida.</span><span class="sxs-lookup"><span data-stu-id="c33fc-127">File version is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**\_BADINTRINSICS DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR\_BADINTRINSICS**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-129">Gli intrinseci non sono validi.</span><span class="sxs-lookup"><span data-stu-id="c33fc-129">Intrinsics are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**\_BADOBJECT DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR\_BADOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-131">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-131">Object is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**\_BADRESOURCE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR\_BADRESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-133">La risorsa non è valida.</span><span class="sxs-lookup"><span data-stu-id="c33fc-133">Resource is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**\_BADSTREAMHANDLE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR\_BADSTREAMHANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-135">Handle del flusso non valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-135">Stream handle is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**\_BADTYPE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR\_BADTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-137">Il tipo di oggetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-137">Object type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**\_BADVALUE DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR\_BADVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-139">Il parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="c33fc-139">Parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**\_FileNotFound DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR\_FILENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-141">Il file non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="c33fc-141">File could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**\_INTERNALERROR DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR\_INTERNALERROR**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-143">Si è verificato un errore interno.</span><span class="sxs-lookup"><span data-stu-id="c33fc-143">Internal error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOinternet**</span><span class="sxs-lookup"><span data-stu-id="c33fc-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR\_NOINTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-145">Connessione Internet non trovata.</span><span class="sxs-lookup"><span data-stu-id="c33fc-145">Internet connection not found.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**\_NOMOREDATA DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR\_NOMOREDATA**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-147">Non sono disponibili altri dati.</span><span class="sxs-lookup"><span data-stu-id="c33fc-147">No further data is available.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**\_NOMOREOBJECTS DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR\_NOMOREOBJECTS**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-149">Tutti gli oggetti sono stati enumerati.</span><span class="sxs-lookup"><span data-stu-id="c33fc-149">All objects have been enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**\_NOMORESTREAMHANDLES DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR\_NOMORESTREAMHANDLES**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-151">Non sono disponibili handle di flusso.</span><span class="sxs-lookup"><span data-stu-id="c33fc-151">No stream handles are available.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**\_NOTDONEYET DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR\_NOTDONEYET**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-153">Operazione non completata.</span><span class="sxs-lookup"><span data-stu-id="c33fc-153">Operation has not completed.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**\_NotFound DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR\_NOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-155">Impossibile trovare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c33fc-155">Object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR ( \_ PARSEERROR)**</span><span class="sxs-lookup"><span data-stu-id="c33fc-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR\_PARSEERROR**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-157">Non è stato possibile analizzare il file.</span><span class="sxs-lookup"><span data-stu-id="c33fc-157">File could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**\_RESOURCENOTFOUND DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR\_RESOURCENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-159">Impossibile trovare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c33fc-159">Resource could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**notemplate DXFILEERR \_**</span><span class="sxs-lookup"><span data-stu-id="c33fc-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR\_NOTEMPLATE**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-161">Non sono disponibili modelli.</span><span class="sxs-lookup"><span data-stu-id="c33fc-161">No template available.</span></span>

</dd> <dt>

<span data-ttu-id="c33fc-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**\_URLNOTFOUND DXFILEERR**</span><span class="sxs-lookup"><span data-stu-id="c33fc-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR\_URLNOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="c33fc-163">Impossibile trovare l'URL.</span><span class="sxs-lookup"><span data-stu-id="c33fc-163">URL could not be found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c33fc-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c33fc-164">Requirements</span></span>



| <span data-ttu-id="c33fc-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33fc-165">Requirement</span></span> | <span data-ttu-id="c33fc-166">Valore</span><span class="sxs-lookup"><span data-stu-id="c33fc-166">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c33fc-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c33fc-167">Header</span></span><br/> | <dl> <span data-ttu-id="c33fc-168"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33fc-168"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33fc-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c33fc-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33fc-170">Riferimento file X (legacy)</span><span class="sxs-lookup"><span data-stu-id="c33fc-170">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




