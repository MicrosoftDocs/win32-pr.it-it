---
title: Struttura di stringhe
description: Rappresenta l'organizzazione dei dati in una risorsa di versione del file. Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le notifiche sul copyright o i relativi marchi.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menu struttura stringa e altre risorse
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301193"
---
# <a name="string-structure"></a><span data-ttu-id="7db67-105">Struttura di stringhe</span><span class="sxs-lookup"><span data-stu-id="7db67-105">String structure</span></span>

<span data-ttu-id="7db67-106">Rappresenta l'organizzazione dei dati in una risorsa di versione del file.</span><span class="sxs-lookup"><span data-stu-id="7db67-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="7db67-107">Contiene una stringa che descrive un aspetto specifico di un file, ad esempio la versione di un file, le notifiche sul copyright o i relativi marchi.</span><span class="sxs-lookup"><span data-stu-id="7db67-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db67-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7db67-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="7db67-109">Members</span><span class="sxs-lookup"><span data-stu-id="7db67-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7db67-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="7db67-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="7db67-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="7db67-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7db67-112">Lunghezza, in byte, della struttura di **stringa** .</span><span class="sxs-lookup"><span data-stu-id="7db67-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7db67-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="7db67-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="7db67-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="7db67-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7db67-115">Dimensione, in parole, del membro del **valore** .</span><span class="sxs-lookup"><span data-stu-id="7db67-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="7db67-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="7db67-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="7db67-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="7db67-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7db67-118">Tipo di dati nella risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="7db67-118">The type of data in the version resource.</span></span> <span data-ttu-id="7db67-119">Questo membro è 1 se la risorsa della versione contiene dati di testo e 0 se la risorsa della versione contiene dati binari.</span><span class="sxs-lookup"><span data-stu-id="7db67-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="7db67-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="7db67-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="7db67-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="7db67-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="7db67-122">Stringa Unicode arbitraria.</span><span class="sxs-lookup"><span data-stu-id="7db67-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="7db67-123">Il membro **szKey** può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7db67-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="7db67-124">Questi valori sono solo linee guida.</span><span class="sxs-lookup"><span data-stu-id="7db67-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="7db67-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Commenti**</span><span class="sxs-lookup"><span data-stu-id="7db67-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-126">Il membro **value** contiene informazioni aggiuntive da visualizzare per scopi diagnostici.</span><span class="sxs-lookup"><span data-stu-id="7db67-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="7db67-127">Questa stringa può essere di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="7db67-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="7db67-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span><span class="sxs-lookup"><span data-stu-id="7db67-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-129">Il membro **value** identifica la società che ha generato il file.</span><span class="sxs-lookup"><span data-stu-id="7db67-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="7db67-130">Ad esempio, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc."</span><span class="sxs-lookup"><span data-stu-id="7db67-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="7db67-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="7db67-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-132">Il membro del **valore** descrive il file in modo che possa essere presentato agli utenti.</span><span class="sxs-lookup"><span data-stu-id="7db67-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="7db67-133">Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare.</span><span class="sxs-lookup"><span data-stu-id="7db67-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="7db67-134">Ad esempio, "driver tastiera per le tastiere in stile" o "Microsoft Word per Windows".</span><span class="sxs-lookup"><span data-stu-id="7db67-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="7db67-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="7db67-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-136">Il membro del **valore** identifica la versione del file.</span><span class="sxs-lookup"><span data-stu-id="7db67-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="7db67-137">Ad esempio, il **valore** potrebbe essere "3.00 a" o "5.00. RC2".</span><span class="sxs-lookup"><span data-stu-id="7db67-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="7db67-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span><span class="sxs-lookup"><span data-stu-id="7db67-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-139">Il membro **value** identifica il nome interno del file, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="7db67-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="7db67-140">Ad esempio, questa stringa può contenere il nome del modulo per una DLL, un nome di dispositivo virtuale per un dispositivo virtuale Windows o un nome dispositivo per un driver di dispositivo MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="7db67-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="7db67-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="7db67-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-142">Il membro del **valore** descrive tutte le comunicazioni di copyright, i marchi e i marchi registrati applicabili al file.</span><span class="sxs-lookup"><span data-stu-id="7db67-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="7db67-143">Deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright, i numeri dei marchi e così via.</span><span class="sxs-lookup"><span data-stu-id="7db67-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="7db67-144">In inglese, questa stringa deve avere il formato "Copyright Microsoft Corp. 1990 1994".</span><span class="sxs-lookup"><span data-stu-id="7db67-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="7db67-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="7db67-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-146">Il membro **valore** descrive tutti i marchi e i marchi registrati che si applicano al file.</span><span class="sxs-lookup"><span data-stu-id="7db67-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="7db67-147">Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via.</span><span class="sxs-lookup"><span data-stu-id="7db67-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="7db67-148">In inglese questa stringa dovrebbe essere "Windows is a trademark of Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="7db67-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="7db67-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="7db67-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-150">Il membro del **valore** identifica il nome originale del file, escluso il percorso.</span><span class="sxs-lookup"><span data-stu-id="7db67-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="7db67-151">Questo consente a un'applicazione di determinare se un file è stato rinominato da un utente.</span><span class="sxs-lookup"><span data-stu-id="7db67-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="7db67-152">Questo nome non può essere in formato MS-DOS 8,3 Se il file è specifico di un file system non FAT.</span><span class="sxs-lookup"><span data-stu-id="7db67-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="7db67-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="7db67-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-154">Il membro del **valore** descrive chi, dove e perché è stata compilata la versione privata del file.</span><span class="sxs-lookup"><span data-stu-id="7db67-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="7db67-155">Questa stringa deve essere presente solo se il **flag \_ \_ PRIVATEBUILD di vs FF** è impostato nel membro **dwFileFlags** della struttura [**vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="7db67-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="7db67-156">Ad esempio, il **valore** potrebbe essere "compilato da Oscar in \\ OSCAR2".</span><span class="sxs-lookup"><span data-stu-id="7db67-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="7db67-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span><span class="sxs-lookup"><span data-stu-id="7db67-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-158">Il membro **valore** identifica il nome del prodotto con cui viene distribuito questo file.</span><span class="sxs-lookup"><span data-stu-id="7db67-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="7db67-159">Questa stringa, ad esempio, potrebbe essere "Microsoft Windows".</span><span class="sxs-lookup"><span data-stu-id="7db67-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="7db67-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="7db67-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-161">Il membro **valore** identifica la versione del prodotto con cui viene distribuito questo file.</span><span class="sxs-lookup"><span data-stu-id="7db67-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="7db67-162">Ad esempio, il **valore** potrebbe essere "3.00 a" o "5.00. RC2".</span><span class="sxs-lookup"><span data-stu-id="7db67-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="7db67-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="7db67-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="7db67-164">Il membro del **valore** descrive il modo in cui la versione del file è diversa dalla versione normale.</span><span class="sxs-lookup"><span data-stu-id="7db67-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="7db67-165">Questa voce deve essere presente solo se il **flag \_ \_ SPECIALBUILD di vs FF** è impostato nel membro **dwFileFlags** della struttura [**vs \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) .</span><span class="sxs-lookup"><span data-stu-id="7db67-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="7db67-166">Ad esempio, il **valore** potrebbe essere "compilazione privata per Olivetti risoluzione dei problemi del mouse nei computer M250 e M250E".</span><span class="sxs-lookup"><span data-stu-id="7db67-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7db67-167">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="7db67-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="7db67-168">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="7db67-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7db67-169">Il numero di parole necessarie per allineare il membro del **valore** a un limite di 32 bit è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="7db67-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="7db67-170">**Valore**</span><span class="sxs-lookup"><span data-stu-id="7db67-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="7db67-171">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="7db67-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="7db67-172">Stringa con terminazione zero.</span><span class="sxs-lookup"><span data-stu-id="7db67-172">A zero-terminated string.</span></span> <span data-ttu-id="7db67-173">Per ulteriori informazioni, vedere la descrizione del membro **szKey** .</span><span class="sxs-lookup"><span data-stu-id="7db67-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7db67-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="7db67-174">Remarks</span></span>

<span data-ttu-id="7db67-175">Questa struttura non è una vera struttura del linguaggio C perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="7db67-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="7db67-176">Questa struttura è stata creata esclusivamente per rappresentare l'organizzazione dei dati in una risorsa di versione e non viene visualizzata in alcun file di intestazione fornito con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="7db67-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="7db67-177">Una struttura di **stringa** può avere un valore **szKey** , ad esempio "CompanyName" e un **valore** "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="7db67-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="7db67-178">Un'altra struttura di **stringa** con lo stesso valore **szKey** potrebbe contenere un **valore** di "Microsoft GmbH".</span><span class="sxs-lookup"><span data-stu-id="7db67-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="7db67-179">Questo problema può verificarsi se la seconda struttura di **stringhe** è stata associata a una struttura [**un'STRINGTABLE**](stringtable.md) il cui valore **szKey** è 040704b0, tedesco/Unicode.</span><span class="sxs-lookup"><span data-stu-id="7db67-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db67-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7db67-180">Requirements</span></span>



| <span data-ttu-id="7db67-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="7db67-181">Requirement</span></span> | <span data-ttu-id="7db67-182">Valore</span><span class="sxs-lookup"><span data-stu-id="7db67-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7db67-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7db67-183">Minimum supported client</span></span><br/> | <span data-ttu-id="7db67-184">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7db67-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7db67-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7db67-185">Minimum supported server</span></span><br/> | <span data-ttu-id="7db67-186">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7db67-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7db67-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7db67-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="7db67-188">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7db67-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7db67-189">**Un'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="7db67-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="7db67-190">**VS \_ informazione FixedFileInfo**</span><span class="sxs-lookup"><span data-stu-id="7db67-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="7db67-191">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="7db67-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="7db67-192">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="7db67-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="7db67-193">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7db67-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7db67-194">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="7db67-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





