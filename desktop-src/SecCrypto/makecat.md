---
description: Strumento CryptoAPI che consente di creare un file di catalogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879486"
---
# <a name="makecat"></a><span data-ttu-id="ce998-103">MakeCat</span><span class="sxs-lookup"><span data-stu-id="ce998-103">MakeCat</span></span>

<span data-ttu-id="ce998-104">Lo strumento MakeCat è uno strumento CryptoAPI che consente di creare un file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="ce998-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="ce998-105">MakeCat è disponibile come parte di Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0 ed è installato, per impostazione predefinita, nella \\ cartella bin del percorso di installazione di SDK.</span><span class="sxs-lookup"><span data-stu-id="ce998-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="ce998-106">Lo strumento MakeCat usa la sintassi del comando seguente:</span><span class="sxs-lookup"><span data-stu-id="ce998-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="ce998-107">**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nome file*</span><span class="sxs-lookup"><span data-stu-id="ce998-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="ce998-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce998-108">Parameters</span></span>



| <span data-ttu-id="ce998-109">Parametro</span><span class="sxs-lookup"><span data-stu-id="ce998-109">Parameter</span></span>             | <span data-ttu-id="ce998-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce998-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce998-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="ce998-111">**-n**</span></span><br/>     | <span data-ttu-id="ce998-112">Non arrestare in caso di errore reversibile.</span><span class="sxs-lookup"><span data-stu-id="ce998-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="ce998-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="ce998-113">**-r**</span></span><br/>     | <span data-ttu-id="ce998-114">Impone la chiusura di MakeCat se rileva errori reversibili.</span><span class="sxs-lookup"><span data-stu-id="ce998-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="ce998-115">In particolare, termina quando si elaborano le voci nella sezione dei file di catalogo di un file con estensione CDF.</span><span class="sxs-lookup"><span data-stu-id="ce998-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="ce998-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="ce998-116">**-v**</span></span><br/>     | <span data-ttu-id="ce998-117">Dettagliato.</span><span class="sxs-lookup"><span data-stu-id="ce998-117">Verbose.</span></span> <span data-ttu-id="ce998-118">Visualizza tutti i messaggi di stato e di errore.</span><span class="sxs-lookup"><span data-stu-id="ce998-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="ce998-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ce998-119">*FileName*</span></span><br/> | <span data-ttu-id="ce998-120">Nome del file con estensione CDF da analizzare.</span><span class="sxs-lookup"><span data-stu-id="ce998-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="ce998-121">Per la struttura e il contenuto richiesti, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ce998-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="ce998-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce998-122">Remarks</span></span>

<span data-ttu-id="ce998-123">Il file con estensione CDF deve essere compilato con le specifiche seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce998-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="ce998-124">L'ultima voce nel file con estensione CDF deve avere sempre un carattere di nuova riga esplicito alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="ce998-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="ce998-125">La \[ \] sezione CatalogHeader definisce le informazioni sull'intero file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="ce998-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="ce998-126">Opzione</span><span class="sxs-lookup"><span data-stu-id="ce998-126">Option</span></span>                    | <span data-ttu-id="ce998-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce998-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce998-128">Nome</span><span class="sxs-lookup"><span data-stu-id="ce998-128">Name</span></span><br/>           | <span data-ttu-id="ce998-129">Nome del file di catalogo, inclusa la relativa estensione.</span><span class="sxs-lookup"><span data-stu-id="ce998-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ce998-130">ResultDir</span><span class="sxs-lookup"><span data-stu-id="ce998-130">ResultDir</span></span><br/>      | <span data-ttu-id="ce998-131">Directory in cui verrà inserito il file con estensione cat creato.</span><span class="sxs-lookup"><span data-stu-id="ce998-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="ce998-132">Se non è indicato, viene utilizzata la directory corrente predefinita.</span><span class="sxs-lookup"><span data-stu-id="ce998-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="ce998-133">Se la directory non esiste, viene creata.</span><span class="sxs-lookup"><span data-stu-id="ce998-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ce998-134">PublicVersion</span><span class="sxs-lookup"><span data-stu-id="ce998-134">PublicVersion</span></span><br/>  | <span data-ttu-id="ce998-135">Questa opzione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ce998-135">This option is not supported.</span></span> <br/> <span data-ttu-id="ce998-136">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Versione del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ce998-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="ce998-137">Se viene lasciato vuoto, viene usato il valore predefinito 1.</span><span class="sxs-lookup"><span data-stu-id="ce998-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ce998-138">CatalogVersion</span><span class="sxs-lookup"><span data-stu-id="ce998-138">CatalogVersion</span></span><br/> | <span data-ttu-id="ce998-139">Versione del catalogo.</span><span class="sxs-lookup"><span data-stu-id="ce998-139">Catalog version.</span></span> <span data-ttu-id="ce998-140">Se la versione non è presente o è impostata su 1, "0x100" viene passato al parametro *dwPublicVersion* della funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e viene creato un file di catalogo della versione 1.</span><span class="sxs-lookup"><span data-stu-id="ce998-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="ce998-141">L'opzione HashAlgorithms deve essere vuota o contenere SHA1.</span><span class="sxs-lookup"><span data-stu-id="ce998-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="ce998-142">Se la versione è impostata su 2, "0x200" viene passato al parametro *dwPublicVersion* della funzione [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e viene creato un file di catalogo della versione 2.</span><span class="sxs-lookup"><span data-stu-id="ce998-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="ce998-143">L'opzione HashAlgorithms deve contenere SHA256.</span><span class="sxs-lookup"><span data-stu-id="ce998-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="ce998-144">Se questa opzione è presente ma contiene un valore diverso da 1 o 2, lo strumento MakeCat verrà visualizzato in errore.</span><span class="sxs-lookup"><span data-stu-id="ce998-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="ce998-145">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questa opzione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ce998-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="ce998-146">HashAlgorithms</span><span class="sxs-lookup"><span data-stu-id="ce998-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="ce998-147">Nome dell'algoritmo hash utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ce998-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="ce998-148">Per ulteriori informazioni, vedere l'opzione CatalogVersion.</span><span class="sxs-lookup"><span data-stu-id="ce998-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="ce998-149">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questa opzione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ce998-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ce998-150">PageHashes</span><span class="sxs-lookup"><span data-stu-id="ce998-150">PageHashes</span></span><br/>     | <span data-ttu-id="ce998-151">Specifica se eseguire l'hashing dei file elencati nell' <HASH> opzione nella \[ sezione CatalogFiles \]</span><span class="sxs-lookup"><span data-stu-id="ce998-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="ce998-152">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questa opzione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ce998-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ce998-153">EncodingType</span><span class="sxs-lookup"><span data-stu-id="ce998-153">EncodingType</span></span><br/>   | <span data-ttu-id="ce998-154">Tipo di codifica del messaggio utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ce998-154">Type of message encoding used.</span></span> <span data-ttu-id="ce998-155">Se viene lasciato vuoto, il valore predefinito di EncodingType è PKCS \_ 7 \_ ASN \_ Encoding \| X509 \_ ASN \_ Encoding, 0x00010001.</span><span class="sxs-lookup"><span data-stu-id="ce998-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="ce998-156">La \[ \] sezione CatalogFiles definisce ogni membro del file di catalogo con file di diversi tipi e attributi di diversi tipi in gruppi distinti.</span><span class="sxs-lookup"><span data-stu-id="ce998-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce998-157">Opzione</span><span class="sxs-lookup"><span data-stu-id="ce998-157">Option</span></span></th>
<th><span data-ttu-id="ce998-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce998-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce998-159">Tag di riferimento</span><span class="sxs-lookup"><span data-stu-id="ce998-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="ce998-160">Riferimento di testo al file.</span><span class="sxs-lookup"><span data-stu-id="ce998-160">Text reference to the file.</span></span> <span data-ttu-id="ce998-161">Può includere qualsiasi carattere di testo ASCII eccetto il segno di uguale (=).</span><span class="sxs-lookup"><span data-stu-id="ce998-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="ce998-162">Il sistema deve essere in grado di riprodurre questo tag dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ce998-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="ce998-163">Utilizzare <HASH> come prefisso del nome file.</span><span class="sxs-lookup"><span data-stu-id="ce998-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="ce998-164">In questo modo il tag è l'hash del file nel formato stringa ASCII.</span><span class="sxs-lookup"><span data-stu-id="ce998-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce998-165">nome e percorso del file</span><span class="sxs-lookup"><span data-stu-id="ce998-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="ce998-166">Nome del file, inclusa l'estensione da analizzare e il percorso relativo del file.</span><span class="sxs-lookup"><span data-stu-id="ce998-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="ce998-167">Tutti i tipi di file che possono essere firmati con SignTool possono essere aggiunti a un catalogo.</span><span class="sxs-lookup"><span data-stu-id="ce998-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="ce998-168">Ad esempio, i nomi di file con le seguenti estensioni, tra gli altri, possono essere aggiunti a un catalogo:. exe,. cab,. cat,. ocx,. dll e. STL.</span><span class="sxs-lookup"><span data-stu-id="ce998-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce998-169">ALTSIPID</span><span class="sxs-lookup"><span data-stu-id="ce998-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="ce998-170">GUID SIP da usare per l'hashing anziché il SIP standard in base al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="ce998-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="ce998-171">Questa voce è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="ce998-171">This entry is optional.</span></span> <span data-ttu-id="ce998-172">Se questa voce viene omessa, verrà eseguito l'hashing del membro utilizzando il SIP predefinito.</span><span class="sxs-lookup"><span data-stu-id="ce998-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="ce998-173">Se non viene trovato alcun SIP installato predefinito, verrà usato il SIP flat.</span><span class="sxs-lookup"><span data-stu-id="ce998-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce998-174">guid</span><span class="sxs-lookup"><span data-stu-id="ce998-174">guid</span></span><br/></td>
<td><span data-ttu-id="ce998-175">Rappresentazione testuale di un GUID.</span><span class="sxs-lookup"><span data-stu-id="ce998-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce998-176">ATTRx</span><span class="sxs-lookup"><span data-stu-id="ce998-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="ce998-177">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ce998-177">Optional.</span></span> <span data-ttu-id="ce998-178">Attributo o istruzione relativa al file o al contenuto.</span><span class="sxs-lookup"><span data-stu-id="ce998-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="ce998-179">Può essere presente un numero qualsiasi di attributi, incluso None.</span><span class="sxs-lookup"><span data-stu-id="ce998-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce998-180">tipo</span><span class="sxs-lookup"><span data-stu-id="ce998-180">type</span></span><br/></td>
<td><span data-ttu-id="ce998-181">Definisce il tipo di attributo da aggiungere nel formato 0x00000000 (testo).</span><span class="sxs-lookup"><span data-stu-id="ce998-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="ce998-182">Questa opzione può essere una combinazione OR bit per bit di<strong>zero o più</strong> dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce998-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="ce998-183">attributo autenticato 0x10000000 (firmato, incluso nell'hash).</span><span class="sxs-lookup"><span data-stu-id="ce998-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="ce998-184">0x20000000 attributo non autenticato (senza segno, non incluso nell'hash, non verificabile).</span><span class="sxs-lookup"><span data-stu-id="ce998-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="ce998-185">l'attributo 0x01000000 non verrà replicato in voci SHA1 in un catalogo CatalogVersion 2.</span><span class="sxs-lookup"><span data-stu-id="ce998-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="ce998-186">l'attributo 0x00010000 è rappresentato in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ce998-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="ce998-187">Non verrà eseguita alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="ce998-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="ce998-188">l'attributo 0x00020000 è rappresentato nella codifica base-64.</span><span class="sxs-lookup"><span data-stu-id="ce998-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="ce998-189">Viene utilizzato per rappresentare i dati binari.</span><span class="sxs-lookup"><span data-stu-id="ce998-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="ce998-190">l'attributo 0x00000001 è una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="ce998-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="ce998-191">Usare l'opzione OID per il nome.</span><span class="sxs-lookup"><span data-stu-id="ce998-191">Use the oid option for the name.</span></span> <span data-ttu-id="ce998-192">Questo attributo è lento; Pertanto, utilizzare questa opzione con moderazione.</span><span class="sxs-lookup"><span data-stu-id="ce998-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="ce998-193">all'attributo 0x00000002 viene fatto riferimento da un <a href="/windows/desktop/SecGloss/o-gly"><em>identificatore di oggetto</em></a> (OID).</span><span class="sxs-lookup"><span data-stu-id="ce998-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce998-194">oid</span><span class="sxs-lookup"><span data-stu-id="ce998-194">oid</span></span><br/></td>
<td><span data-ttu-id="ce998-195">Rappresentazione testuale della chiave di riferimento dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="ce998-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="ce998-196">Si tratta di un OID sotto forma di una stringa di testo in notazione Quad punteggiata (ad esempio, a. b. c. d) o di un nome di testo.</span><span class="sxs-lookup"><span data-stu-id="ce998-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce998-197">Valore</span><span class="sxs-lookup"><span data-stu-id="ce998-197">value</span></span><br/></td>
<td><span data-ttu-id="ce998-198">Rappresentazione testuale del valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="ce998-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="ce998-199">Il tipo di rappresentazione testuale utilizzato dipende dal valore dell'opzione Type.</span><span class="sxs-lookup"><span data-stu-id="ce998-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="ce998-200">I caratteri EOL determinano la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="ce998-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="ce998-201">Hashing del file specificato.</span><span class="sxs-lookup"><span data-stu-id="ce998-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce998-202">Il file di catalogo generato è senza segno.</span><span class="sxs-lookup"><span data-stu-id="ce998-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="ce998-203">Se deve essere firmato prima della trasmissione, viene firmato usando [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="ce998-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
