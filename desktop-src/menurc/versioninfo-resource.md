---
title: Risorsa VERSIONINFO
description: Definisce una risorsa di informazioni sulla versione. La risorsa contiene informazioni sul file come numero di versione, il sistema operativo previsto e il nome file originale. La risorsa deve essere utilizzata con le funzioni di informazioni sulla versione.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menu risorse VERSIONINFO e altre risorse
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "104339579"
---
# <a name="versioninfo-resource"></a><span data-ttu-id="20ea0-106">Risorsa VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="20ea0-106">VERSIONINFO resource</span></span>

<span data-ttu-id="20ea0-107">Definisce una risorsa di informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-107">Defines a version-information resource.</span></span> <span data-ttu-id="20ea0-108">La risorsa contiene informazioni sul file come numero di versione, il sistema operativo previsto e il nome file originale.</span><span class="sxs-lookup"><span data-stu-id="20ea0-108">The resource contains such information about the file as its version number, its intended operating system, and its original filename.</span></span> <span data-ttu-id="20ea0-109">La risorsa deve essere utilizzata con le funzioni di [informazioni sulla versione](./version-information.md) .</span><span class="sxs-lookup"><span data-stu-id="20ea0-109">The resource is intended to be used with the [Version Information](./version-information.md) functions.</span></span>

<span data-ttu-id="20ea0-110">Esistono due modi per formattare un'istruzione **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="20ea0-110">There are two ways to format a **VERSIONINFO** statement:</span></span>

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

<span data-ttu-id="20ea0-111">\- - oppure -</span><span class="sxs-lookup"><span data-stu-id="20ea0-111">\- or -</span></span>

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="20ea0-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="20ea0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ea0-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span><span class="sxs-lookup"><span data-stu-id="20ea0-113"><span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-114">Identificatore della risorsa di informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-114">Version-information resource identifier.</span></span> <span data-ttu-id="20ea0-115">Questo valore deve essere 1.</span><span class="sxs-lookup"><span data-stu-id="20ea0-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-info*</span><span class="sxs-lookup"><span data-stu-id="20ea0-116"><span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-117">Informazioni sulla versione, ad esempio la versione del file e il sistema operativo desiderato.</span><span class="sxs-lookup"><span data-stu-id="20ea0-117">Version information, such as the file version and the intended operating system.</span></span> <span data-ttu-id="20ea0-118">Questo parametro è costituito dalle istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-118">This parameter consists of the following statements.</span></span>



| <span data-ttu-id="20ea0-119">Istruzione</span><span class="sxs-lookup"><span data-stu-id="20ea0-119">Statement</span></span>                         | <span data-ttu-id="20ea0-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ea0-121">*Versione* **fileversion**</span><span class="sxs-lookup"><span data-stu-id="20ea0-121">**FILEVERSION** *version*</span></span>         | <span data-ttu-id="20ea0-122">Numero di versione binario del file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-122">Binary version number for the file.</span></span> <span data-ttu-id="20ea0-123">La *versione* è costituita da integer a 2 32 bit, definiti da integer a 4 16 bit.</span><span class="sxs-lookup"><span data-stu-id="20ea0-123">The *version* consists of two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="20ea0-124">Ad esempio, "FileVersion 3, 10, 0, 61" viene convertito in due parole doppie: 0x0003000a e 0x0000003D, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="20ea0-124">For example, "FILEVERSION 3,10,0,61" is translated into two doublewords: 0x0003000a and 0x0000003d, in that order.</span></span> <span data-ttu-id="20ea0-125">Di conseguenza, se la *versione* è definita dai valori **DWORD** *DW1* e *DW2*, è necessario che vengano visualizzati nell'istruzione **fileversion** nel modo seguente: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` .</span><span class="sxs-lookup"><span data-stu-id="20ea0-125">Therefore, if *version* is defined by the **DWORD** values *dw1* and *dw2*, they need to appear in the **FILEVERSION** statement as follows: `HIWORD(dw1)`, `LOWORD(dw1)`, `HIWORD(dw2)`, `LOWORD(dw2)`.</span></span> |
| <span data-ttu-id="20ea0-126"> *Versione* di ProductVersion</span><span class="sxs-lookup"><span data-stu-id="20ea0-126">**PRODUCTVERSION** *version*</span></span>      | <span data-ttu-id="20ea0-127">Numero di versione binario per il prodotto con cui il file viene distribuito.</span><span class="sxs-lookup"><span data-stu-id="20ea0-127">Binary version number for the product with which the file is distributed.</span></span> <span data-ttu-id="20ea0-128">Il parametro *Version* è integer a 2 32 bit, definiti da integer a 4 16 bit.</span><span class="sxs-lookup"><span data-stu-id="20ea0-128">The *version* parameter is two 32-bit integers, defined by four 16-bit integers.</span></span> <span data-ttu-id="20ea0-129">Per ulteriori informazioni sulla *versione*, vedere la descrizione di **fileversion** .</span><span class="sxs-lookup"><span data-stu-id="20ea0-129">For more information about *version*, see the **FILEVERSION** description.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="20ea0-130"> *FILEFLAGSMASK* FILEFLAGSMASK</span><span class="sxs-lookup"><span data-stu-id="20ea0-130">**FILEFLAGSMASK** *fileflagsmask*</span></span> | <span data-ttu-id="20ea0-131">Indica i bit nell'istruzione **FILEflags** validi.</span><span class="sxs-lookup"><span data-stu-id="20ea0-131">Indicates which bits in the **FILEFLAGS** statement are valid.</span></span> <span data-ttu-id="20ea0-132">Per Windows a 16 bit, questo valore è 0x3F.</span><span class="sxs-lookup"><span data-stu-id="20ea0-132">For 16-bit Windows, this value is 0x3f.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="20ea0-133">*Flag* **fileflag** FILEFLAGS</span><span class="sxs-lookup"><span data-stu-id="20ea0-133">**FILEFLAGS** *fileflags*</span></span>         | <span data-ttu-id="20ea0-134">Attributi del file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-134">Attributes of the file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="20ea0-135">*FILEOS* di **FILEOS**</span><span class="sxs-lookup"><span data-stu-id="20ea0-135">**FILEOS** *fileos*</span></span>               | <span data-ttu-id="20ea0-136">Sistema operativo per il quale è stato progettato questo file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-136">Operating system for which this file was designed.</span></span> <span data-ttu-id="20ea0-137">Il parametro *FILEOS* può essere uno dei valori del sistema operativo specificati nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="20ea0-137">The *fileos* parameter can be one of the operating system values given in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="20ea0-138">**FileType**  filetype</span><span class="sxs-lookup"><span data-stu-id="20ea0-138">**FILETYPE** *filetype*</span></span>           | <span data-ttu-id="20ea0-139">Tipo generale di file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-139">General type of file.</span></span> <span data-ttu-id="20ea0-140">Il parametro *FileType* può essere uno dei valori dei tipi di file elencati nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="20ea0-140">The *filetype* parameter can be one of the file type values listed in the Remarks section.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="20ea0-141">Sottotipo **FILESUBTYPE** </span><span class="sxs-lookup"><span data-stu-id="20ea0-141">**FILESUBTYPE** *subtype*</span></span>         | <span data-ttu-id="20ea0-142">Funzione del file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-142">Function of the file.</span></span> <span data-ttu-id="20ea0-143">Il parametro del *sottotipo* è zero a meno che il parametro *FileType* **nell'istruzione filetype non** sia VFT \_ drv, VFT \_ font o VFT \_ vxd.</span><span class="sxs-lookup"><span data-stu-id="20ea0-143">The *subtype* parameter is zero unless the *filetype* parameter in the **FILETYPE** statement is VFT\_DRV, VFT\_FONT, or VFT\_VXD.</span></span> <span data-ttu-id="20ea0-144">Per un elenco di valori dei sottotipi di file, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="20ea0-144">For a list of file subtype values, see the Remarks section.</span></span>                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="20ea0-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-Statement*</span><span class="sxs-lookup"><span data-stu-id="20ea0-145"><span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-146">Specifica uno o più blocchi di informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-146">Specifies one or more version-information blocks.</span></span> <span data-ttu-id="20ea0-147">Un blocco può contenere informazioni sulle stringhe o informazioni sulle variabili.</span><span class="sxs-lookup"><span data-stu-id="20ea0-147">A block can contain string information or variable information.</span></span> <span data-ttu-id="20ea0-148">Per altre informazioni, vedere blocco [**StringFileInfo**](stringfileinfo-block.md) o [**VarFileInfo**](varfileinfo-block.md).</span><span class="sxs-lookup"><span data-stu-id="20ea0-148">For more information, see [**StringFileInfo Block**](stringfileinfo-block.md) or [**VarFileInfo Block**](varfileinfo-block.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20ea0-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="20ea0-149">Remarks</span></span>

<span data-ttu-id="20ea0-150">Per usare le costanti specificate con l'istruzione **VERSIONINFO** , è necessario includere il file di intestazione winver. h o Windows. h nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="20ea0-150">To use the constants specified with the **VERSIONINFO** statement, you must include the Winver.h or Windows.h header file in the resource-definition file.</span></span>

<span data-ttu-id="20ea0-151">Nell'elenco seguente vengono descritti i parametri utilizzati nell'istruzione **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="20ea0-151">The following list describes the parameters used in the **VERSIONINFO** statement:</span></span>

<dl> <dt>

<span data-ttu-id="20ea0-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*FILEFLAGS*</span><span class="sxs-lookup"><span data-stu-id="20ea0-152"><span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-153">Una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-153">A combination of the following values.</span></span>



| <span data-ttu-id="20ea0-154">Valore</span><span class="sxs-lookup"><span data-stu-id="20ea0-154">Value</span></span>                      | <span data-ttu-id="20ea0-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-155">Description</span></span>                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ea0-156">**DEBUG di VS \_ FF \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-156">**VS\_FF\_DEBUG**</span></span>          | <span data-ttu-id="20ea0-157">Il file contiene informazioni di debug o è compilato con funzionalità di debug abilitate.</span><span class="sxs-lookup"><span data-stu-id="20ea0-157">File contains debugging information or is compiled with debugging features enabled.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="20ea0-158">**con \_ patch di vs FF \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-158">**VS\_FF\_PATCHED**</span></span>        | <span data-ttu-id="20ea0-159">Il file è stato modificato e non è identico al file di spedizione originale con lo stesso numero di versione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-159">File has been modified and is not identical to the original shipping file of the same version number.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="20ea0-160">**\_ \_ versione preliminare di vs FF**</span><span class="sxs-lookup"><span data-stu-id="20ea0-160">**VS\_FF\_PRERELEASE**</span></span>     | <span data-ttu-id="20ea0-161">Il file è una versione di sviluppo, non un prodotto rilasciato commercialmente.</span><span class="sxs-lookup"><span data-stu-id="20ea0-161">File is a development version, not a commercially released product.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="20ea0-162">**VS \_ FF \_ PRIVATEBUILD**</span><span class="sxs-lookup"><span data-stu-id="20ea0-162">**VS\_FF\_PRIVATEBUILD**</span></span>   | <span data-ttu-id="20ea0-163">Il file non è stato compilato con procedure di rilascio standard.</span><span class="sxs-lookup"><span data-stu-id="20ea0-163">File was not built using standard release procedures.</span></span> <span data-ttu-id="20ea0-164">Se questo valore viene specificato, il [**blocco StringFileInfo**](stringfileinfo-block.md) deve contenere una stringa **PrivateBuild** .</span><span class="sxs-lookup"><span data-stu-id="20ea0-164">If this value is given, the [**StringFileInfo block**](stringfileinfo-block.md) must contain a **PrivateBuild** string.</span></span>                                                                                              |
| <span data-ttu-id="20ea0-165">**VS \_ FF \_ SPECIALBUILD**</span><span class="sxs-lookup"><span data-stu-id="20ea0-165">**VS\_FF\_SPECIALBUILD**</span></span>   | <span data-ttu-id="20ea0-166">Il file è stato compilato dall'azienda originale usando le procedure di rilascio standard, ma è una variante del file standard con lo stesso numero di versione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-166">File was built by the original company using standard release procedures but is a variation of the standard file of the same version number.</span></span> <span data-ttu-id="20ea0-167">Se questo valore viene specificato, il blocco del [blocco **StringFileInfo**](stringfileinfo-block.md) deve contenere una stringa **SpecialBuild** .</span><span class="sxs-lookup"><span data-stu-id="20ea0-167">If this value is given, the [**StringFileInfo** block](stringfileinfo-block.md) block must contain a **SpecialBuild** string.</span></span> |
| <span data-ttu-id="20ea0-168">**VS \_ \_ FILEFLAGSMASK**</span><span class="sxs-lookup"><span data-stu-id="20ea0-168">**VS\_FFI\_FILEFLAGSMASK**</span></span> | <span data-ttu-id="20ea0-169">Combinazione di tutti i valori precedenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-169">A combination of all the preceding values.</span></span>                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="20ea0-170"><span id="fileos"></span><span id="FILEOS"></span>*FILEOS*</span><span class="sxs-lookup"><span data-stu-id="20ea0-170"><span id="fileos"></span><span id="FILEOS"></span>*fileos*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-171">Uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-171">One of the following values.</span></span>



| <span data-ttu-id="20ea0-172">Valore</span><span class="sxs-lookup"><span data-stu-id="20ea0-172">Value</span></span>                   | <span data-ttu-id="20ea0-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-173">Description</span></span>                                                      |
|-------------------------|------------------------------------------------------------------|
| <span data-ttu-id="20ea0-174">**VOS \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="20ea0-174">**VOS\_UNKNOWN**</span></span>        | <span data-ttu-id="20ea0-175">Il sistema operativo per il quale è stato progettato il file è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20ea0-175">The operating system for which the file was designed is unknown.</span></span> |
| <span data-ttu-id="20ea0-176">**\_DOS vos**</span><span class="sxs-lookup"><span data-stu-id="20ea0-176">**VOS\_DOS**</span></span>            | <span data-ttu-id="20ea0-177">Il file è stato progettato per MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="20ea0-177">File was designed for MS-DOS.</span></span>                                    |
| <span data-ttu-id="20ea0-178">**VOS \_ NT**</span><span class="sxs-lookup"><span data-stu-id="20ea0-178">**VOS\_NT**</span></span>             | <span data-ttu-id="20ea0-179">Il file è stato progettato per Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="20ea0-179">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="20ea0-180">**\_ \_ WINDOWS16 vos**</span><span class="sxs-lookup"><span data-stu-id="20ea0-180">**VOS\_\_WINDOWS16**</span></span>    | <span data-ttu-id="20ea0-181">Il file è stato progettato per Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="20ea0-181">File was designed for 16-bit Windows.</span></span>                            |
| <span data-ttu-id="20ea0-182">**\_ \_ WINDOWS32 vos**</span><span class="sxs-lookup"><span data-stu-id="20ea0-182">**VOS\_\_WINDOWS32**</span></span>    | <span data-ttu-id="20ea0-183">Il file è stato progettato per Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="20ea0-183">File was designed for 32-bit Windows.</span></span>                            |
| <span data-ttu-id="20ea0-184">**VOS \_ DOS \_ WINDOWS16**</span><span class="sxs-lookup"><span data-stu-id="20ea0-184">**VOS\_DOS\_WINDOWS16**</span></span> | <span data-ttu-id="20ea0-185">Il file è stato progettato per Windows a 16 bit in esecuzione con MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="20ea0-185">File was designed for 16-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="20ea0-186">**VOS \_ DOS \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="20ea0-186">**VOS\_DOS\_WINDOWS32**</span></span> | <span data-ttu-id="20ea0-187">Il file è stato progettato per Windows a 32 bit in esecuzione con MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="20ea0-187">File was designed for 32-bit Windows running with MS-DOS.</span></span>        |
| <span data-ttu-id="20ea0-188">**VOS \_ NT \_ WINDOWS32**</span><span class="sxs-lookup"><span data-stu-id="20ea0-188">**VOS\_NT\_WINDOWS32**</span></span>  | <span data-ttu-id="20ea0-189">Il file è stato progettato per Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="20ea0-189">File was designed for 32-bit Windows.</span></span>                            |



 

<span data-ttu-id="20ea0-190">I valori 0x00002L, 0x00003L, 0x20000L e 0x30000L sono riservati.</span><span class="sxs-lookup"><span data-stu-id="20ea0-190">The values 0x00002L, 0x00003L, 0x20000L and 0x30000L are reserved.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span><span class="sxs-lookup"><span data-stu-id="20ea0-191"><span id="filetype"></span><span id="FILETYPE"></span>*filetype*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-192">Uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-192">One of the following values.</span></span>



| <span data-ttu-id="20ea0-193">Valore</span><span class="sxs-lookup"><span data-stu-id="20ea0-193">Value</span></span>                | <span data-ttu-id="20ea0-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-194">Description</span></span>                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ea0-195">**VFT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="20ea0-195">**VFT\_UNKNOWN**</span></span>     | <span data-ttu-id="20ea0-196">Tipo di file sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20ea0-196">File type is unknown.</span></span>                                                                                                       |
| <span data-ttu-id="20ea0-197">**\_app VFT**</span><span class="sxs-lookup"><span data-stu-id="20ea0-197">**VFT\_APP**</span></span>         | <span data-ttu-id="20ea0-198">Il file contiene un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-198">File contains an application.</span></span>                                                                                               |
| <span data-ttu-id="20ea0-199">**\_dll VFT**</span><span class="sxs-lookup"><span data-stu-id="20ea0-199">**VFT\_DLL**</span></span>         | <span data-ttu-id="20ea0-200">Il file contiene una libreria di collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="20ea0-200">File contains a dynamic-link library (DLL).</span></span>                                                                                 |
| <span data-ttu-id="20ea0-201">**VFT \_ drv**</span><span class="sxs-lookup"><span data-stu-id="20ea0-201">**VFT\_DRV**</span></span>         | <span data-ttu-id="20ea0-202">Il file contiene un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20ea0-202">File contains a device driver.</span></span> <span data-ttu-id="20ea0-203">Se *FileType è* **VFT \_ drv**, il *sottotipo* contiene una descrizione più specifica del driver.</span><span class="sxs-lookup"><span data-stu-id="20ea0-203">If *filetype* is **VFT\_DRV**, *subtype* contains a more specific description of the driver.</span></span> |
| <span data-ttu-id="20ea0-204">**\_tipo di carattere VFT**</span><span class="sxs-lookup"><span data-stu-id="20ea0-204">**VFT\_FONT**</span></span>        | <span data-ttu-id="20ea0-205">Il file contiene un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="20ea0-205">File contains a font.</span></span> <span data-ttu-id="20ea0-206">Se *FileType* è \_ un tipo di carattere VFT, il *sottotipo* contiene una descrizione più specifica del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="20ea0-206">If *filetype* is VFT\_FONT, *subtype* contains a more specific description of the font.</span></span>               |
| <span data-ttu-id="20ea0-207">**\_vxd VFT**</span><span class="sxs-lookup"><span data-stu-id="20ea0-207">**VFT\_VXD**</span></span>         | <span data-ttu-id="20ea0-208">Il file contiene un dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="20ea0-208">File contains a virtual device.</span></span>                                                                                             |
| <span data-ttu-id="20ea0-209">**\_lib VFT statica \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-209">**VFT\_STATIC\_LIB**</span></span> | <span data-ttu-id="20ea0-210">Il file contiene una libreria a collegamento statico.</span><span class="sxs-lookup"><span data-stu-id="20ea0-210">File contains a static-link library.</span></span>                                                                                        |



 

<span data-ttu-id="20ea0-211">Tutti gli altri valori sono riservati per l'utilizzo da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20ea0-211">All other values are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-212"><span id="subtype"></span><span id="SUBTYPE"></span>*sottotipo*</span><span class="sxs-lookup"><span data-stu-id="20ea0-212"><span id="subtype"></span><span id="SUBTYPE"></span>*subtype*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-213">Informazioni aggiuntive sul tipo di file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-213">Additional information about the file type.</span></span>

<span data-ttu-id="20ea0-214">Se *FileType* specifica **VFT \_ drv**, questo parametro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-214">If *filetype* specifies **VFT\_DRV**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="20ea0-215">Valore</span><span class="sxs-lookup"><span data-stu-id="20ea0-215">Value</span></span>                             | <span data-ttu-id="20ea0-216">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-216">Description</span></span>                               |
|-----------------------------------|-------------------------------------------|
| <span data-ttu-id="20ea0-217">**VFT2 \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="20ea0-217">**VFT2\_UNKNOWN**</span></span>                 | <span data-ttu-id="20ea0-218">Il tipo di driver è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20ea0-218">Driver type is unknown.</span></span>                   |
| <span data-ttu-id="20ea0-219">**VFT2 \_ drv \_ comm**</span><span class="sxs-lookup"><span data-stu-id="20ea0-219">**VFT2\_DRV\_COMM**</span></span>               | <span data-ttu-id="20ea0-220">Il file contiene un driver di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-220">File contains a communications driver.</span></span>    |
| <span data-ttu-id="20ea0-221">**\_Stampante VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-221">**VFT2\_DRV\_PRINTER**</span></span>            | <span data-ttu-id="20ea0-222">Il file contiene un driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="20ea0-222">File contains a printer driver.</span></span>           |
| <span data-ttu-id="20ea0-223">**\_Tastiera VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-223">**VFT2\_DRV\_KEYBOARD**</span></span>           | <span data-ttu-id="20ea0-224">Il file contiene un driver della tastiera.</span><span class="sxs-lookup"><span data-stu-id="20ea0-224">File contains a keyboard driver.</span></span>          |
| <span data-ttu-id="20ea0-225">**\_Linguaggio VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-225">**VFT2\_DRV\_LANGUAGE**</span></span>           | <span data-ttu-id="20ea0-226">Il file contiene un driver di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="20ea0-226">File contains a language driver.</span></span>          |
| <span data-ttu-id="20ea0-227">**\_Visualizzazione VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-227">**VFT2\_DRV\_DISPLAY**</span></span>            | <span data-ttu-id="20ea0-228">Il file contiene un driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-228">File contains a display driver.</span></span>           |
| <span data-ttu-id="20ea0-229">**\_Mouse VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-229">**VFT2\_DRV\_MOUSE**</span></span>              | <span data-ttu-id="20ea0-230">Il file contiene un driver del mouse.</span><span class="sxs-lookup"><span data-stu-id="20ea0-230">File contains a mouse driver.</span></span>             |
| <span data-ttu-id="20ea0-231">**\_Rete VFT2 DRV \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-231">**VFT2\_DRV\_NETWORK**</span></span>            | <span data-ttu-id="20ea0-232">Il file contiene un driver di rete.</span><span class="sxs-lookup"><span data-stu-id="20ea0-232">File contains a network driver.</span></span>           |
| <span data-ttu-id="20ea0-233">**\_Sistema DRV \_ VFT2**</span><span class="sxs-lookup"><span data-stu-id="20ea0-233">**VFT2\_DRV\_SYSTEM**</span></span>             | <span data-ttu-id="20ea0-234">Il file contiene un driver di sistema.</span><span class="sxs-lookup"><span data-stu-id="20ea0-234">File contains a system driver.</span></span>            |
| <span data-ttu-id="20ea0-235">**VFT2 \_ drv \_ installabile**</span><span class="sxs-lookup"><span data-stu-id="20ea0-235">**VFT2\_DRV\_INSTALLABLE**</span></span>        | <span data-ttu-id="20ea0-236">Il file contiene un driver installabile.</span><span class="sxs-lookup"><span data-stu-id="20ea0-236">File contains an installable driver.</span></span>      |
| <span data-ttu-id="20ea0-237">**VFT2 \_ drv \_ audio**</span><span class="sxs-lookup"><span data-stu-id="20ea0-237">**VFT2\_DRV\_SOUND**</span></span>              | <span data-ttu-id="20ea0-238">Il file contiene un driver audio.</span><span class="sxs-lookup"><span data-stu-id="20ea0-238">File contains a sound driver.</span></span>             |
| <span data-ttu-id="20ea0-239">**\_Stampante VFT2 DRV con \_ versione \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-239">**VFT2\_DRV\_VERSIONED\_PRINTER**</span></span> | <span data-ttu-id="20ea0-240">Il file contiene un driver della stampante con versione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-240">File contains a versioned printer driver.</span></span> |



 

<span data-ttu-id="20ea0-241">Se *FileType* specifica il **\_ tipo di carattere VFT**, questo parametro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-241">If *filetype* specifies **VFT\_FONT**, this parameter can be one of the following values.</span></span>



| <span data-ttu-id="20ea0-242">Valore</span><span class="sxs-lookup"><span data-stu-id="20ea0-242">Value</span></span>                    | <span data-ttu-id="20ea0-243">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-243">Description</span></span>                    |
|--------------------------|--------------------------------|
| <span data-ttu-id="20ea0-244">**VFT2 \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="20ea0-244">**VFT2\_UNKNOWN**</span></span>        | <span data-ttu-id="20ea0-245">Il tipo di carattere è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20ea0-245">Font type is unknown.</span></span>          |
| <span data-ttu-id="20ea0-246">**\_Raster carattere \_ VFT2**</span><span class="sxs-lookup"><span data-stu-id="20ea0-246">**VFT2\_FONT\_RASTER**</span></span>   | <span data-ttu-id="20ea0-247">Il file contiene un tipo di carattere raster.</span><span class="sxs-lookup"><span data-stu-id="20ea0-247">File contains a raster font.</span></span>   |
| <span data-ttu-id="20ea0-248">**\_Vettore del tipo di carattere VFT2 \_**</span><span class="sxs-lookup"><span data-stu-id="20ea0-248">**VFT2\_FONT\_VECTOR**</span></span>   | <span data-ttu-id="20ea0-249">Il file contiene un tipo di carattere vettoriale.</span><span class="sxs-lookup"><span data-stu-id="20ea0-249">File contains a vector font.</span></span>   |
| <span data-ttu-id="20ea0-250">**\_Tipo di carattere VFT2 \_ TrueType**</span><span class="sxs-lookup"><span data-stu-id="20ea0-250">**VFT2\_FONT\_TRUETYPE**</span></span> | <span data-ttu-id="20ea0-251">Il file contiene un tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="20ea0-251">File contains a TrueType font.</span></span> |



 

<span data-ttu-id="20ea0-252">Se *FileType* specifica VFT \_ vxd, questo parametro deve corrispondere all'identificatore del dispositivo virtuale incluso nel blocco di controllo del dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="20ea0-252">If *filetype* specifies VFT\_VXD, this parameter must be the virtual-device identifier included in the virtual-device control block.</span></span>

<span data-ttu-id="20ea0-253">Tutti i valori dei *sottotipi* non elencati sono riservati per l'utilizzo da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20ea0-253">All *subtype* values not listed here are reserved for use by Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="20ea0-254"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-255">Uno dei seguenti codici di lingua.</span><span class="sxs-lookup"><span data-stu-id="20ea0-255">One of the following language codes.</span></span>



| <span data-ttu-id="20ea0-256">Codice</span><span class="sxs-lookup"><span data-stu-id="20ea0-256">Code</span></span>   | <span data-ttu-id="20ea0-257">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="20ea0-257">Language</span></span>            | <span data-ttu-id="20ea0-258">Codice</span><span class="sxs-lookup"><span data-stu-id="20ea0-258">Code</span></span>   | <span data-ttu-id="20ea0-259">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="20ea0-259">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="20ea0-260">0x0401</span><span class="sxs-lookup"><span data-stu-id="20ea0-260">0x0401</span></span> | <span data-ttu-id="20ea0-261">Arabo</span><span class="sxs-lookup"><span data-stu-id="20ea0-261">Arabic</span></span>              | <span data-ttu-id="20ea0-262">0x0415</span><span class="sxs-lookup"><span data-stu-id="20ea0-262">0x0415</span></span> | <span data-ttu-id="20ea0-263">Polacco</span><span class="sxs-lookup"><span data-stu-id="20ea0-263">Polish</span></span>                    |
| <span data-ttu-id="20ea0-264">0x0402</span><span class="sxs-lookup"><span data-stu-id="20ea0-264">0x0402</span></span> | <span data-ttu-id="20ea0-265">Bulgaro</span><span class="sxs-lookup"><span data-stu-id="20ea0-265">Bulgarian</span></span>           | <span data-ttu-id="20ea0-266">0x0416</span><span class="sxs-lookup"><span data-stu-id="20ea0-266">0x0416</span></span> | <span data-ttu-id="20ea0-267">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="20ea0-267">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="20ea0-268">0x0403</span><span class="sxs-lookup"><span data-stu-id="20ea0-268">0x0403</span></span> | <span data-ttu-id="20ea0-269">Catalano</span><span class="sxs-lookup"><span data-stu-id="20ea0-269">Catalan</span></span>             | <span data-ttu-id="20ea0-270">0x0417</span><span class="sxs-lookup"><span data-stu-id="20ea0-270">0x0417</span></span> | <span data-ttu-id="20ea0-271">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="20ea0-271">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="20ea0-272">0x0404</span><span class="sxs-lookup"><span data-stu-id="20ea0-272">0x0404</span></span> | <span data-ttu-id="20ea0-273">Cinese tradizionale</span><span class="sxs-lookup"><span data-stu-id="20ea0-273">Traditional Chinese</span></span> | <span data-ttu-id="20ea0-274">0x0418</span><span class="sxs-lookup"><span data-stu-id="20ea0-274">0x0418</span></span> | <span data-ttu-id="20ea0-275">Romeno</span><span class="sxs-lookup"><span data-stu-id="20ea0-275">Romanian</span></span>                  |
| <span data-ttu-id="20ea0-276">0x0405</span><span class="sxs-lookup"><span data-stu-id="20ea0-276">0x0405</span></span> | <span data-ttu-id="20ea0-277">Ceco</span><span class="sxs-lookup"><span data-stu-id="20ea0-277">Czech</span></span>               | <span data-ttu-id="20ea0-278">0x0419</span><span class="sxs-lookup"><span data-stu-id="20ea0-278">0x0419</span></span> | <span data-ttu-id="20ea0-279">Russo</span><span class="sxs-lookup"><span data-stu-id="20ea0-279">Russian</span></span>                   |
| <span data-ttu-id="20ea0-280">0x0406</span><span class="sxs-lookup"><span data-stu-id="20ea0-280">0x0406</span></span> | <span data-ttu-id="20ea0-281">Danese</span><span class="sxs-lookup"><span data-stu-id="20ea0-281">Danish</span></span>              | <span data-ttu-id="20ea0-282">0x041A</span><span class="sxs-lookup"><span data-stu-id="20ea0-282">0x041A</span></span> | <span data-ttu-id="20ea0-283">Croato-Serbian (alfabeto latino)</span><span class="sxs-lookup"><span data-stu-id="20ea0-283">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="20ea0-284">0x0407</span><span class="sxs-lookup"><span data-stu-id="20ea0-284">0x0407</span></span> | <span data-ttu-id="20ea0-285">Tedesco</span><span class="sxs-lookup"><span data-stu-id="20ea0-285">German</span></span>              | <span data-ttu-id="20ea0-286">0x041B</span><span class="sxs-lookup"><span data-stu-id="20ea0-286">0x041B</span></span> | <span data-ttu-id="20ea0-287">Slovacco</span><span class="sxs-lookup"><span data-stu-id="20ea0-287">Slovak</span></span>                    |
| <span data-ttu-id="20ea0-288">0x0408</span><span class="sxs-lookup"><span data-stu-id="20ea0-288">0x0408</span></span> | <span data-ttu-id="20ea0-289">Greco</span><span class="sxs-lookup"><span data-stu-id="20ea0-289">Greek</span></span>               | <span data-ttu-id="20ea0-290">0x041C</span><span class="sxs-lookup"><span data-stu-id="20ea0-290">0x041C</span></span> | <span data-ttu-id="20ea0-291">Albanese</span><span class="sxs-lookup"><span data-stu-id="20ea0-291">Albanian</span></span>                  |
| <span data-ttu-id="20ea0-292">0x0409</span><span class="sxs-lookup"><span data-stu-id="20ea0-292">0x0409</span></span> | <span data-ttu-id="20ea0-293">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="20ea0-293">U.S. English</span></span>        | <span data-ttu-id="20ea0-294">0x041D</span><span class="sxs-lookup"><span data-stu-id="20ea0-294">0x041D</span></span> | <span data-ttu-id="20ea0-295">Svedese</span><span class="sxs-lookup"><span data-stu-id="20ea0-295">Swedish</span></span>                   |
| <span data-ttu-id="20ea0-296">0x040A</span><span class="sxs-lookup"><span data-stu-id="20ea0-296">0x040A</span></span> | <span data-ttu-id="20ea0-297">Spagnolo castigliano</span><span class="sxs-lookup"><span data-stu-id="20ea0-297">Castilian Spanish</span></span>   | <span data-ttu-id="20ea0-298">0x041E</span><span class="sxs-lookup"><span data-stu-id="20ea0-298">0x041E</span></span> | <span data-ttu-id="20ea0-299">Thai</span><span class="sxs-lookup"><span data-stu-id="20ea0-299">Thai</span></span>                      |
| <span data-ttu-id="20ea0-300">0x040B</span><span class="sxs-lookup"><span data-stu-id="20ea0-300">0x040B</span></span> | <span data-ttu-id="20ea0-301">Finlandese</span><span class="sxs-lookup"><span data-stu-id="20ea0-301">Finnish</span></span>             | <span data-ttu-id="20ea0-302">0x041F</span><span class="sxs-lookup"><span data-stu-id="20ea0-302">0x041F</span></span> | <span data-ttu-id="20ea0-303">Turco</span><span class="sxs-lookup"><span data-stu-id="20ea0-303">Turkish</span></span>                   |
| <span data-ttu-id="20ea0-304">0x040C</span><span class="sxs-lookup"><span data-stu-id="20ea0-304">0x040C</span></span> | <span data-ttu-id="20ea0-305">Francese</span><span class="sxs-lookup"><span data-stu-id="20ea0-305">French</span></span>              | <span data-ttu-id="20ea0-306">0x0420</span><span class="sxs-lookup"><span data-stu-id="20ea0-306">0x0420</span></span> | <span data-ttu-id="20ea0-307">Urdu</span><span class="sxs-lookup"><span data-stu-id="20ea0-307">Urdu</span></span>                      |
| <span data-ttu-id="20ea0-308">0x040D</span><span class="sxs-lookup"><span data-stu-id="20ea0-308">0x040D</span></span> | <span data-ttu-id="20ea0-309">Ebraico</span><span class="sxs-lookup"><span data-stu-id="20ea0-309">Hebrew</span></span>              | <span data-ttu-id="20ea0-310">0x0421</span><span class="sxs-lookup"><span data-stu-id="20ea0-310">0x0421</span></span> | <span data-ttu-id="20ea0-311">Bahasa</span><span class="sxs-lookup"><span data-stu-id="20ea0-311">Bahasa</span></span>                    |
| <span data-ttu-id="20ea0-312">0x040E</span><span class="sxs-lookup"><span data-stu-id="20ea0-312">0x040E</span></span> | <span data-ttu-id="20ea0-313">Ungherese</span><span class="sxs-lookup"><span data-stu-id="20ea0-313">Hungarian</span></span>           | <span data-ttu-id="20ea0-314">0x0804</span><span class="sxs-lookup"><span data-stu-id="20ea0-314">0x0804</span></span> | <span data-ttu-id="20ea0-315">Cinese semplificato</span><span class="sxs-lookup"><span data-stu-id="20ea0-315">Simplified Chinese</span></span>        |
| <span data-ttu-id="20ea0-316">0x040F</span><span class="sxs-lookup"><span data-stu-id="20ea0-316">0x040F</span></span> | <span data-ttu-id="20ea0-317">Islandese</span><span class="sxs-lookup"><span data-stu-id="20ea0-317">Icelandic</span></span>           | <span data-ttu-id="20ea0-318">0x0807</span><span class="sxs-lookup"><span data-stu-id="20ea0-318">0x0807</span></span> | <span data-ttu-id="20ea0-319">Tedesco svizzero</span><span class="sxs-lookup"><span data-stu-id="20ea0-319">Swiss German</span></span>              |
| <span data-ttu-id="20ea0-320">0x0410</span><span class="sxs-lookup"><span data-stu-id="20ea0-320">0x0410</span></span> | <span data-ttu-id="20ea0-321">Italiano</span><span class="sxs-lookup"><span data-stu-id="20ea0-321">Italian</span></span>             | <span data-ttu-id="20ea0-322">0x0809</span><span class="sxs-lookup"><span data-stu-id="20ea0-322">0x0809</span></span> | <span data-ttu-id="20ea0-323">Regno Unito.</span><span class="sxs-lookup"><span data-stu-id="20ea0-323">U.K.</span></span> <span data-ttu-id="20ea0-324">Inglese</span><span class="sxs-lookup"><span data-stu-id="20ea0-324">English</span></span>              |
| <span data-ttu-id="20ea0-325">0x0411</span><span class="sxs-lookup"><span data-stu-id="20ea0-325">0x0411</span></span> | <span data-ttu-id="20ea0-326">Giapponese</span><span class="sxs-lookup"><span data-stu-id="20ea0-326">Japanese</span></span>            | <span data-ttu-id="20ea0-327">0x080A</span><span class="sxs-lookup"><span data-stu-id="20ea0-327">0x080A</span></span> | <span data-ttu-id="20ea0-328">Spagnolo (Messico)</span><span class="sxs-lookup"><span data-stu-id="20ea0-328">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="20ea0-329">0x0412</span><span class="sxs-lookup"><span data-stu-id="20ea0-329">0x0412</span></span> | <span data-ttu-id="20ea0-330">Coreano</span><span class="sxs-lookup"><span data-stu-id="20ea0-330">Korean</span></span>              | <span data-ttu-id="20ea0-331">0x080C</span><span class="sxs-lookup"><span data-stu-id="20ea0-331">0x080C</span></span> | <span data-ttu-id="20ea0-332">Francese belga</span><span class="sxs-lookup"><span data-stu-id="20ea0-332">Belgian French</span></span>            |
| <span data-ttu-id="20ea0-333">0x0413</span><span class="sxs-lookup"><span data-stu-id="20ea0-333">0x0413</span></span> | <span data-ttu-id="20ea0-334">Olandese</span><span class="sxs-lookup"><span data-stu-id="20ea0-334">Dutch</span></span>               | <span data-ttu-id="20ea0-335">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="20ea0-335">0x0C0C</span></span> | <span data-ttu-id="20ea0-336">Francese (Canada)</span><span class="sxs-lookup"><span data-stu-id="20ea0-336">Canadian French</span></span>           |
| <span data-ttu-id="20ea0-337">0x0414</span><span class="sxs-lookup"><span data-stu-id="20ea0-337">0x0414</span></span> | <span data-ttu-id="20ea0-338">Norvegese?</span><span class="sxs-lookup"><span data-stu-id="20ea0-338">Norwegian ?</span></span> <span data-ttu-id="20ea0-339">Bokmal</span><span class="sxs-lookup"><span data-stu-id="20ea0-339">Bokmal</span></span>  | <span data-ttu-id="20ea0-340">0x100C</span><span class="sxs-lookup"><span data-stu-id="20ea0-340">0x100C</span></span> | <span data-ttu-id="20ea0-341">Francese svizzero</span><span class="sxs-lookup"><span data-stu-id="20ea0-341">Swiss French</span></span>              |
| <span data-ttu-id="20ea0-342">0x0810</span><span class="sxs-lookup"><span data-stu-id="20ea0-342">0x0810</span></span> | <span data-ttu-id="20ea0-343">Italiano svizzero</span><span class="sxs-lookup"><span data-stu-id="20ea0-343">Swiss Italian</span></span>       | <span data-ttu-id="20ea0-344">0x0816</span><span class="sxs-lookup"><span data-stu-id="20ea0-344">0x0816</span></span> | <span data-ttu-id="20ea0-345">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="20ea0-345">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="20ea0-346">0x0813</span><span class="sxs-lookup"><span data-stu-id="20ea0-346">0x0813</span></span> | <span data-ttu-id="20ea0-347">Olandese belga</span><span class="sxs-lookup"><span data-stu-id="20ea0-347">Belgian Dutch</span></span>       | <span data-ttu-id="20ea0-348">0x081A</span><span class="sxs-lookup"><span data-stu-id="20ea0-348">0x081A</span></span> | <span data-ttu-id="20ea0-349">Serbo-Croatian (alfabeto cirillico)</span><span class="sxs-lookup"><span data-stu-id="20ea0-349">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="20ea0-350">0x0814</span><span class="sxs-lookup"><span data-stu-id="20ea0-350">0x0814</span></span> | <span data-ttu-id="20ea0-351">Norvegese?</span><span class="sxs-lookup"><span data-stu-id="20ea0-351">Norwegian ?</span></span> <span data-ttu-id="20ea0-352">Nynorsk</span><span class="sxs-lookup"><span data-stu-id="20ea0-352">Nynorsk</span></span> |        |                           |



 

</dd> <dt>

<span data-ttu-id="20ea0-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="20ea0-353"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-354">Uno dei seguenti identificatori di set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="20ea0-354">One of the following character-set identifiers.</span></span>



| <span data-ttu-id="20ea0-355">Decimal</span><span class="sxs-lookup"><span data-stu-id="20ea0-355">Decimal</span></span> | <span data-ttu-id="20ea0-356">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="20ea0-356">Hexadecimal</span></span> | <span data-ttu-id="20ea0-357">Set di caratteri</span><span class="sxs-lookup"><span data-stu-id="20ea0-357">Character Set</span></span>              |
|---------|-------------|----------------------------|
| <span data-ttu-id="20ea0-358">0</span><span class="sxs-lookup"><span data-stu-id="20ea0-358">0</span></span>       | <span data-ttu-id="20ea0-359">0000</span><span class="sxs-lookup"><span data-stu-id="20ea0-359">0000</span></span>        | <span data-ttu-id="20ea0-360">ASCII a 7 bit</span><span class="sxs-lookup"><span data-stu-id="20ea0-360">7-bit ASCII</span></span>                |
| <span data-ttu-id="20ea0-361">932</span><span class="sxs-lookup"><span data-stu-id="20ea0-361">932</span></span>     | <span data-ttu-id="20ea0-362">03A4</span><span class="sxs-lookup"><span data-stu-id="20ea0-362">03A4</span></span>        | <span data-ttu-id="20ea0-363">Giappone (turno?</span><span class="sxs-lookup"><span data-stu-id="20ea0-363">Japan (Shift ?</span></span> <span data-ttu-id="20ea0-364">JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="20ea0-364">JIS X-0208)</span></span> |
| <span data-ttu-id="20ea0-365">949</span><span class="sxs-lookup"><span data-stu-id="20ea0-365">949</span></span>     | <span data-ttu-id="20ea0-366">03B5</span><span class="sxs-lookup"><span data-stu-id="20ea0-366">03B5</span></span>        | <span data-ttu-id="20ea0-367">Corea (Shift?</span><span class="sxs-lookup"><span data-stu-id="20ea0-367">Korea (Shift ?</span></span> <span data-ttu-id="20ea0-368">KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="20ea0-368">KSC 5601)</span></span>   |
| <span data-ttu-id="20ea0-369">950</span><span class="sxs-lookup"><span data-stu-id="20ea0-369">950</span></span>     | <span data-ttu-id="20ea0-370">03B6</span><span class="sxs-lookup"><span data-stu-id="20ea0-370">03B6</span></span>        | <span data-ttu-id="20ea0-371">Taiwan (Big5)</span><span class="sxs-lookup"><span data-stu-id="20ea0-371">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="20ea0-372">1200</span><span class="sxs-lookup"><span data-stu-id="20ea0-372">1200</span></span>    | <span data-ttu-id="20ea0-373">04B0</span><span class="sxs-lookup"><span data-stu-id="20ea0-373">04B0</span></span>        | <span data-ttu-id="20ea0-374">Unicode</span><span class="sxs-lookup"><span data-stu-id="20ea0-374">Unicode</span></span>                    |
| <span data-ttu-id="20ea0-375">1250</span><span class="sxs-lookup"><span data-stu-id="20ea0-375">1250</span></span>    | <span data-ttu-id="20ea0-376">04E2</span><span class="sxs-lookup"><span data-stu-id="20ea0-376">04E2</span></span>        | <span data-ttu-id="20ea0-377">Latino 2 (Europa orientale)</span><span class="sxs-lookup"><span data-stu-id="20ea0-377">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="20ea0-378">1251</span><span class="sxs-lookup"><span data-stu-id="20ea0-378">1251</span></span>    | <span data-ttu-id="20ea0-379">04E3</span><span class="sxs-lookup"><span data-stu-id="20ea0-379">04E3</span></span>        | <span data-ttu-id="20ea0-380">Cirillico</span><span class="sxs-lookup"><span data-stu-id="20ea0-380">Cyrillic</span></span>                   |
| <span data-ttu-id="20ea0-381">1252</span><span class="sxs-lookup"><span data-stu-id="20ea0-381">1252</span></span>    | <span data-ttu-id="20ea0-382">04E4</span><span class="sxs-lookup"><span data-stu-id="20ea0-382">04E4</span></span>        | <span data-ttu-id="20ea0-383">Multilingue</span><span class="sxs-lookup"><span data-stu-id="20ea0-383">Multilingual</span></span>               |
| <span data-ttu-id="20ea0-384">1253</span><span class="sxs-lookup"><span data-stu-id="20ea0-384">1253</span></span>    | <span data-ttu-id="20ea0-385">04E5</span><span class="sxs-lookup"><span data-stu-id="20ea0-385">04E5</span></span>        | <span data-ttu-id="20ea0-386">Greco</span><span class="sxs-lookup"><span data-stu-id="20ea0-386">Greek</span></span>                      |
| <span data-ttu-id="20ea0-387">1254</span><span class="sxs-lookup"><span data-stu-id="20ea0-387">1254</span></span>    | <span data-ttu-id="20ea0-388">04E6</span><span class="sxs-lookup"><span data-stu-id="20ea0-388">04E6</span></span>        | <span data-ttu-id="20ea0-389">Turco</span><span class="sxs-lookup"><span data-stu-id="20ea0-389">Turkish</span></span>                    |
| <span data-ttu-id="20ea0-390">1255</span><span class="sxs-lookup"><span data-stu-id="20ea0-390">1255</span></span>    | <span data-ttu-id="20ea0-391">04E7</span><span class="sxs-lookup"><span data-stu-id="20ea0-391">04E7</span></span>        | <span data-ttu-id="20ea0-392">Ebraico</span><span class="sxs-lookup"><span data-stu-id="20ea0-392">Hebrew</span></span>                     |
| <span data-ttu-id="20ea0-393">1256</span><span class="sxs-lookup"><span data-stu-id="20ea0-393">1256</span></span>    | <span data-ttu-id="20ea0-394">04E8</span><span class="sxs-lookup"><span data-stu-id="20ea0-394">04E8</span></span>        | <span data-ttu-id="20ea0-395">Arabo</span><span class="sxs-lookup"><span data-stu-id="20ea0-395">Arabic</span></span>                     |



 

</dd> <dt>

<span data-ttu-id="20ea0-396"><span id="string-name"></span><span id="STRING-NAME"></span>*nome stringa*</span><span class="sxs-lookup"><span data-stu-id="20ea0-396"><span id="string-name"></span><span id="STRING-NAME"></span>*string-name*</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-397">Uno dei seguenti nomi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-397">One of the following predefined names.</span></span>



| <span data-ttu-id="20ea0-398">Nome</span><span class="sxs-lookup"><span data-stu-id="20ea0-398">Name</span></span>                 | <span data-ttu-id="20ea0-399">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ea0-399">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ea0-400">**Commenti**</span><span class="sxs-lookup"><span data-stu-id="20ea0-400">**Comments**</span></span>         | <span data-ttu-id="20ea0-401">Informazioni aggiuntive da visualizzare per scopi diagnostici.</span><span class="sxs-lookup"><span data-stu-id="20ea0-401">Additional information that should be displayed for diagnostic purposes.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="20ea0-402">**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="20ea0-402">**CompanyName**</span></span>      | <span data-ttu-id="20ea0-403">Società che ha prodotto il file? ad esempio, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="20ea0-403">Company that produced the file?for example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span> <span data-ttu-id="20ea0-404">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-404">This string is required.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="20ea0-405">**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="20ea0-405">**FileDescription**</span></span>  | <span data-ttu-id="20ea0-406">Descrizione del file da presentare agli utenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-406">File description to be presented to users.</span></span> <span data-ttu-id="20ea0-407">Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare, ad esempio "driver tastiera per AT-Style tastiere".</span><span class="sxs-lookup"><span data-stu-id="20ea0-407">This string may be displayed in a list box when the user is choosing files to install?for example, "Keyboard Driver for AT-Style Keyboards".</span></span> <span data-ttu-id="20ea0-408">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-408">This string is required.</span></span>                                                                                            |
| <span data-ttu-id="20ea0-409">**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="20ea0-409">**FileVersion**</span></span>      | <span data-ttu-id="20ea0-410">Numero di versione del file, ad esempio "3,10" o "5.00. RC2".</span><span class="sxs-lookup"><span data-stu-id="20ea0-410">Version number of the file?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="20ea0-411">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-411">This string is required.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="20ea0-412">**InternalName**</span><span class="sxs-lookup"><span data-stu-id="20ea0-412">**InternalName**</span></span>     | <span data-ttu-id="20ea0-413">Nome interno del file, se presente? ad esempio, un nome di modulo se il file è una libreria a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="20ea0-413">Internal name of the file, if one exists?for example, a module name if the file is a dynamic-link library.</span></span> <span data-ttu-id="20ea0-414">Se il file non ha un nome interno, la stringa deve essere il nome file originale, senza estensione.</span><span class="sxs-lookup"><span data-stu-id="20ea0-414">If the file has no internal name, this string should be the original filename, without extension.</span></span> <span data-ttu-id="20ea0-415">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-415">This string is required.</span></span>                                                                       |
| <span data-ttu-id="20ea0-416">**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="20ea0-416">**LegalCopyright**</span></span>   | <span data-ttu-id="20ea0-417">Note sul copyright applicabili al file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-417">Copyright notices that apply to the file.</span></span> <span data-ttu-id="20ea0-418">Questo deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright e così via.</span><span class="sxs-lookup"><span data-stu-id="20ea0-418">This should include the full text of all notices, legal symbols, copyright dates, and so on.</span></span> <span data-ttu-id="20ea0-419">Questa stringa è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="20ea0-419">This string is optional.</span></span>                                                                                                                                             |
| <span data-ttu-id="20ea0-420">**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="20ea0-420">**LegalTrademarks**</span></span>  | <span data-ttu-id="20ea0-421">Marchi e marchi registrati applicabili al file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-421">Trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="20ea0-422">Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via.</span><span class="sxs-lookup"><span data-stu-id="20ea0-422">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="20ea0-423">Questa stringa è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="20ea0-423">This string is optional.</span></span>                                                                                                                        |
| <span data-ttu-id="20ea0-424">**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="20ea0-424">**OriginalFilename**</span></span> | <span data-ttu-id="20ea0-425">Nome originale del file senza includere un percorso.</span><span class="sxs-lookup"><span data-stu-id="20ea0-425">Original name of the file, not including a path.</span></span> <span data-ttu-id="20ea0-426">Queste informazioni consentono a un'applicazione di determinare se un file è stato rinominato da un utente.</span><span class="sxs-lookup"><span data-stu-id="20ea0-426">This information enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="20ea0-427">Il formato del nome dipende dalla file system per cui è stato creato il file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-427">The format of the name depends on the file system for which the file was created.</span></span> <span data-ttu-id="20ea0-428">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-428">This string is required.</span></span>                                                 |
| <span data-ttu-id="20ea0-429">**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="20ea0-429">**PrivateBuild**</span></span>     | <span data-ttu-id="20ea0-430">Informazioni su una versione privata del file, ad esempio "compilato da TESTER1 su banco di controllo \\ ".</span><span class="sxs-lookup"><span data-stu-id="20ea0-430">Information about a private version of the file?for example, "Built by TESTER1 on \\TESTBED".</span></span> <span data-ttu-id="20ea0-431">Questa stringa deve essere presente solo se **vs \_ FF \_ PRIVATEBUILD** è specificato nel parametro *FILEFLAGS* del blocco radice.</span><span class="sxs-lookup"><span data-stu-id="20ea0-431">This string should be present only if **VS\_FF\_PRIVATEBUILD** is specified in the *fileflags* parameter of the root block.</span></span>                                                                                   |
| <span data-ttu-id="20ea0-432">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="20ea0-432">**ProductName**</span></span>      | <span data-ttu-id="20ea0-433">Nome del prodotto con cui viene distribuito il file.</span><span class="sxs-lookup"><span data-stu-id="20ea0-433">Name of the product with which the file is distributed.</span></span> <span data-ttu-id="20ea0-434">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-434">This string is required.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="20ea0-435">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="20ea0-435">**ProductVersion**</span></span>   | <span data-ttu-id="20ea0-436">Versione del prodotto con cui viene distribuito il file, ad esempio "3,10" o "5.00. RC2".</span><span class="sxs-lookup"><span data-stu-id="20ea0-436">Version of the product with which the file is distributed?for example, "3.10" or "5.00.RC2".</span></span> <span data-ttu-id="20ea0-437">Questa stringa è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="20ea0-437">This string is required.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="20ea0-438">**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="20ea0-438">**SpecialBuild**</span></span>     | <span data-ttu-id="20ea0-439">Testo che indica la differenza tra la versione del file e la versione standard, ad esempio "compilazione privata per TESTER1 risoluzione dei problemi del mouse nei computer M250 e M250E".</span><span class="sxs-lookup"><span data-stu-id="20ea0-439">Text that indicates how this version of the file differs from the standard version?for example, "Private build for TESTER1 solving mouse problems on M250 and M250E computers".</span></span> <span data-ttu-id="20ea0-440">Questa stringa deve essere presente solo se **vs \_ FF \_ SPECIALBUILD** è specificato nel parametro *FILEFLAGS* del blocco radice.</span><span class="sxs-lookup"><span data-stu-id="20ea0-440">This string should be present only if **VS\_FF\_SPECIALBUILD** is specified in the *fileflags* parameter of the root block.</span></span> |



 

</dd> </dl>

<span data-ttu-id="20ea0-441">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="20ea0-441">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="20ea0-442">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="20ea0-442">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="20ea0-443">Esempio</span><span class="sxs-lookup"><span data-stu-id="20ea0-443">Examples</span></span>

<span data-ttu-id="20ea0-444">Nell'esempio seguente viene definita una risorsa **VERSIONINFO** :</span><span class="sxs-lookup"><span data-stu-id="20ea0-444">The following example defines a **VERSIONINFO** resource:</span></span>

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a><span data-ttu-id="20ea0-445">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20ea0-445">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ea0-446">Utilizzo delle informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="20ea0-446">Using Version Information</span></span>](./using-version-information.md)
</dt> <dt>

[<span data-ttu-id="20ea0-447">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="20ea0-447">Version Information</span></span>](./version-information.md)
</dt> </dl>

 

 