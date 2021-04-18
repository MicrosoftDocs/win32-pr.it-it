---
description: Crea un certificato X. 509, firmato dalla chiave radice del test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307692"
---
# <a name="makecert"></a><span data-ttu-id="26082-104">MakeCert</span><span class="sxs-lookup"><span data-stu-id="26082-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="26082-105">MakeCert è deprecato.</span><span class="sxs-lookup"><span data-stu-id="26082-105">MakeCert is deprecated.</span></span> <span data-ttu-id="26082-106">Per creare certificati autofirmati, usare il cmdlet di PowerShell [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span><span class="sxs-lookup"><span data-stu-id="26082-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="26082-107">Lo strumento MakeCert crea un certificato [*X. 509*](../secgloss/x-gly.md) , firmato dalla chiave radice del test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi.</span><span class="sxs-lookup"><span data-stu-id="26082-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="26082-108">Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="26082-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="26082-109">Lo strumento viene installato nella \\ cartella bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="26082-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="26082-110">Lo strumento MakeCert usa la sintassi del comando seguente:</span><span class="sxs-lookup"><span data-stu-id="26082-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="26082-111">**Makecert** \[ *BasicOptions* \| *ExtendedOptions* \] *Outputfile*</span><span class="sxs-lookup"><span data-stu-id="26082-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="26082-112">*Outputfile* è il nome del file in cui verrà scritto il certificato.</span><span class="sxs-lookup"><span data-stu-id="26082-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="26082-113">È possibile omettere *outputfile* se il certificato non deve essere scritto in un file.</span><span class="sxs-lookup"><span data-stu-id="26082-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="26082-114">Opzioni</span><span class="sxs-lookup"><span data-stu-id="26082-114">Options</span></span>

<span data-ttu-id="26082-115">MakeCert include opzioni di base ed estese.</span><span class="sxs-lookup"><span data-stu-id="26082-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="26082-116">Le opzioni di base sono quelle più frequentemente usate nella creazione di certificati.</span><span class="sxs-lookup"><span data-stu-id="26082-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="26082-117">Le opzioni estese offrono una maggiore flessibilità.</span><span class="sxs-lookup"><span data-stu-id="26082-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="26082-118">Le opzioni per MakeCert sono divise anche in tre gruppi funzionali:</span><span class="sxs-lookup"><span data-stu-id="26082-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="26082-119">Opzioni di base specifiche solo per la tecnologia dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="26082-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="26082-120">Opzioni estese specifiche solo per la tecnologia del file SPC e della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="26082-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="26082-121">Opzioni estese applicabili alla tecnologia del file SPC, della chiave privata e dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="26082-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="26082-122">Le opzioni fornite nelle tabelle seguenti possono essere utilizzate solo con Internet Explorer 4,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="26082-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26082-123">Opzione di base</span><span class="sxs-lookup"><span data-stu-id="26082-123">Basic option</span></span></th>
<th><span data-ttu-id="26082-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26082-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26082-125"><strong>-a</strong> <strong></strong> <em>Algoritmo</em> di</span><span class="sxs-lookup"><span data-stu-id="26082-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="26082-126">Algoritmo <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> .</span><span class="sxs-lookup"><span data-stu-id="26082-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="26082-127">Deve essere impostato su <strong>SHA-1</strong> o <strong>MD5</strong> (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="26082-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="26082-128">Per informazioni su MD5, vedere <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span><span class="sxs-lookup"><span data-stu-id="26082-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="26082-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="26082-130">Data in cui il certificato diventa prima valido.</span><span class="sxs-lookup"><span data-stu-id="26082-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="26082-131">Il valore predefinito è quando viene creato il certificato.</span><span class="sxs-lookup"><span data-stu-id="26082-131">The default is when the certificate is created.</span></span> <span data-ttu-id="26082-132">Il formato di <em>dateStart</em> è mm/gg/aaaa.</span><span class="sxs-lookup"><span data-stu-id="26082-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-133"><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="26082-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="26082-134">Tipo di certificato.</span><span class="sxs-lookup"><span data-stu-id="26082-134">Certificate type.</span></span> <span data-ttu-id="26082-135"><em>CertificateTypes</em> può essere <strong>end</strong> per l'entità finale o l' <strong>autorità</strong> per l' <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>.</span><span class="sxs-lookup"><span data-stu-id="26082-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="26082-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="26082-137">Data di fine del periodo di validità.</span><span class="sxs-lookup"><span data-stu-id="26082-137">Date when the validity period ends.</span></span> <span data-ttu-id="26082-138">Il valore predefinito è l'anno 2039.</span><span class="sxs-lookup"><span data-stu-id="26082-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-139"><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="26082-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="26082-140">Inserisce nel certificato un elenco di uno o più <a href="/windows/desktop/SecGloss/e-gly"><em></em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>identificatori di oggetto</em></a> con valori delimitati da virgole (OID).</span><span class="sxs-lookup"><span data-stu-id="26082-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="26082-141">Ad esempio, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> inserisce l'OID di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="26082-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="26082-142">Per le definizioni dei OID consentiti, vedere il file Wincrypt. h in CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="26082-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="26082-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="26082-144">Altezza massima dell'albero al di sotto del certificato.</span><span class="sxs-lookup"><span data-stu-id="26082-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="26082-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="26082-146">Collegamento alle informazioni sui criteri dell'Agenzia SPC, ad esempio un URL.</span><span class="sxs-lookup"><span data-stu-id="26082-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="26082-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="26082-148">Durata del periodo di validità.</span><span class="sxs-lookup"><span data-stu-id="26082-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-149"><strong>-n</strong> <strong>&quot;</strong> <em>Nome</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="26082-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="26082-150">Nome del certificato dell'autore.</span><span class="sxs-lookup"><span data-stu-id="26082-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="26082-151">Questo nome deve essere conforme allo standard <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> .</span><span class="sxs-lookup"><span data-stu-id="26082-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="26082-152">Il metodo più semplice consiste nell'usare il &quot; formato CN =<em>nome</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="26082-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="26082-153">Ad esempio: <strong>-n &quot; CN = test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="26082-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="26082-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="26082-155">È necessario includere l'estensione di autenticazione client Netscape.</span><span class="sxs-lookup"><span data-stu-id="26082-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-156"><strong>-PE</strong></span><span class="sxs-lookup"><span data-stu-id="26082-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="26082-157">Contrassegna la chiave privata come esportabile.</span><span class="sxs-lookup"><span data-stu-id="26082-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="26082-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="26082-159">Crea un certificato autofirmato.</span><span class="sxs-lookup"><span data-stu-id="26082-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-160"><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="26082-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="26082-161">Nome del file del certificato con la chiave pubblica del soggetto esistente da usare.</span><span class="sxs-lookup"><span data-stu-id="26082-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-162"><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></span><span class="sxs-lookup"><span data-stu-id="26082-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="26082-163">Posizione del contenitore di chiavi del soggetto che include la <a href="/windows/desktop/SecGloss/p-gly"><em>chiave privata</em></a>.</span><span class="sxs-lookup"><span data-stu-id="26082-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="26082-164">Se non esiste alcun contenitore di chiavi, ne viene creato uno.</span><span class="sxs-lookup"><span data-stu-id="26082-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="26082-165">Se non si usa l'opzione <strong>-SK</strong> o <strong>-SV</strong> , viene creato e usato per impostazione predefinita un contenitore di chiavi predefinito.</span><span class="sxs-lookup"><span data-stu-id="26082-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-166"><strong>-Sky</strong> <strong></strong> <em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="26082-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="26082-167">Specifica della chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26082-167">Subject's key specification.</span></span> <span data-ttu-id="26082-168"><em>SubjectKeySpec</em> deve essere uno dei tre valori possibili:</span><span class="sxs-lookup"><span data-stu-id="26082-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="26082-169"><strong>Firma</strong> (specifica chiave AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="26082-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="26082-170"><strong>Exchange</strong> (specifica chiave AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="26082-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="26082-171">Integer, ad esempio <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="26082-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="26082-172">Per ulteriori informazioni, vedere la nota che segue questa tabella.</span><span class="sxs-lookup"><span data-stu-id="26082-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-173"><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="26082-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="26082-174">Provider CryptoAPI per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26082-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="26082-175">Il valore predefinito è il provider dell'utente.</span><span class="sxs-lookup"><span data-stu-id="26082-175">The default is the user's provider.</span></span> <span data-ttu-id="26082-176">Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="26082-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-177"><strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="26082-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="26082-178">Percorso del registro di sistema dell'archivio certificati dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26082-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="26082-179"><em>SubjectCertStoreLocation</em> deve essere <strong>LocalMachine</strong> (chiave del registro di sistema HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (chiave del registro di sistema HKEY_CURRENT_USER).</span><span class="sxs-lookup"><span data-stu-id="26082-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="26082-180"><strong>CurrentUser</strong> è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="26082-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-181"><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="26082-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="26082-182">Nome dell'archivio certificati dell'oggetto in cui verrà archiviato il certificato generato.</span><span class="sxs-lookup"><span data-stu-id="26082-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-183"><strong>-SV</strong> <strong></strong> <em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="26082-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="26082-184">Nome del file con estensione PVK dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26082-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="26082-185">Se non si usa l'opzione <strong>-SK</strong> o <strong>-SV</strong> , viene creato e usato per impostazione predefinita un contenitore di chiavi predefinito.</span><span class="sxs-lookup"><span data-stu-id="26082-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-186"><strong>-SY</strong> <strong></strong> <em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="26082-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="26082-187">Tipo di provider CryptoAPI per subject.</span><span class="sxs-lookup"><span data-stu-id="26082-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="26082-188">Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="26082-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="26082-189">Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="26082-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="26082-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="26082-191">Numero di serie del certificato.</span><span class="sxs-lookup"><span data-stu-id="26082-191">Serial number of the certificate.</span></span> <span data-ttu-id="26082-192">Il valore massimo è 2 ^ 31.</span><span class="sxs-lookup"><span data-stu-id="26082-192">The maximum value is 2^31.</span></span> <span data-ttu-id="26082-193">Il valore predefinito è un valore generato dallo strumento che garantisce l'univocità.</span><span class="sxs-lookup"><span data-stu-id="26082-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="26082-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="26082-195">Tipo di <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>.</span><span class="sxs-lookup"><span data-stu-id="26082-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="26082-196"><em>CertificateAuthority</em> deve essere impostato su <strong>Commercial</strong> (per i certificati utilizzati dagli editori di software commerciale) o su <strong>singoli</strong> (per i certificati che devono essere utilizzati da autori di software singoli).</span><span class="sxs-lookup"><span data-stu-id="26082-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="26082-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="26082-198">Consente di visualizzare le opzioni di base.</span><span class="sxs-lookup"><span data-stu-id="26082-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="26082-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="26082-200">Consente di visualizzare le opzioni estese.</span><span class="sxs-lookup"><span data-stu-id="26082-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="26082-201">Se in Internet Explorer versione 4,0 o successiva viene utilizzata l'opzione di specifica della chiave **-Sky** , la specifica deve corrispondere alla specifica della chiave indicata dal file di [*chiave privata*](../secgloss/p-gly.md) o dal [*contenitore di chiavi*](../secgloss/k-gly.md)private.</span><span class="sxs-lookup"><span data-stu-id="26082-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="26082-202">Se non si utilizza l'opzione relativa alla specifica della chiave, verrà utilizzata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="26082-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="26082-203">Se il contenitore di chiavi contiene più di una specifica chiave, MakeCert tenterà innanzitutto di usare la \_ specifica della chiave di firma.</span><span class="sxs-lookup"><span data-stu-id="26082-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="26082-204">Se l'operazione ha esito negativo, MakeCert tenterà di utilizzare in caso di scambio delle corrispondenze \_ .</span><span class="sxs-lookup"><span data-stu-id="26082-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="26082-205">Poiché la maggior parte degli utenti ha una chiave di \_ firma o una chiave di scambio delle chiavi \_ , questa opzione non deve essere utilizzata nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="26082-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="26082-206">Le opzioni seguenti sono destinate solo ai file del [*certificato di pubblicazione software*](../secgloss/s-gly.md) (SPC) e alla tecnologia di chiave privata.</span><span class="sxs-lookup"><span data-stu-id="26082-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26082-207">Opzione SPC e chiave privata</span><span class="sxs-lookup"><span data-stu-id="26082-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="26082-208">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26082-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26082-209"><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="26082-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="26082-210">Posizione del certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="26082-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="26082-212">Percorso del contenitore di chiavi dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-212">Location of the issuer's key container.</span></span> <span data-ttu-id="26082-213">Il valore predefinito è la chiave radice del test.</span><span class="sxs-lookup"><span data-stu-id="26082-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="26082-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="26082-215">Specifica della chiave dell'autorità emittente, che deve essere uno dei tre valori possibili:</span><span class="sxs-lookup"><span data-stu-id="26082-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="26082-216"><strong>Firma</strong> (specifica chiave AT_SIGNATURE)</span><span class="sxs-lookup"><span data-stu-id="26082-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="26082-217"><strong>Exchange</strong> (specifica chiave AT_KEYEXCHANGE)</span><span class="sxs-lookup"><span data-stu-id="26082-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="26082-218">Integer, ad esempio <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="26082-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="26082-219">Per ulteriori informazioni, vedere la nota che segue questa tabella.</span><span class="sxs-lookup"><span data-stu-id="26082-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-220"><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="26082-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="26082-221">Provider CryptoAPI per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="26082-222">Il valore predefinito è il provider dell'utente.</span><span class="sxs-lookup"><span data-stu-id="26082-222">The default is the user's provider.</span></span> <span data-ttu-id="26082-223">Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="26082-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26082-224"><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="26082-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="26082-225">File di chiave privata dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-225">Issuer's private key file.</span></span> <span data-ttu-id="26082-226">Il valore predefinito è la radice del test.</span><span class="sxs-lookup"><span data-stu-id="26082-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26082-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="26082-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="26082-228">Tipo di provider CryptoAPI per Issuer.</span><span class="sxs-lookup"><span data-stu-id="26082-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="26082-229">Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="26082-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="26082-230">Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="26082-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="26082-231">Se si usa l'opzione di specifica della chiave **-iky** in Internet Explorer 4,0 o versione successiva, la specifica deve corrispondere alla specifica della chiave indicata dal file di [*chiave privata*](../secgloss/p-gly.md) o dal [*contenitore di chiavi*](../secgloss/k-gly.md)private.</span><span class="sxs-lookup"><span data-stu-id="26082-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="26082-232">Se non si utilizza l'opzione relativa alla specifica della chiave, verrà utilizzata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="26082-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="26082-233">Se il contenitore di chiavi contiene più di una specifica chiave, MakeCert tenterà innanzitutto di usare la \_ specifica della chiave di firma.</span><span class="sxs-lookup"><span data-stu-id="26082-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="26082-234">Se l'operazione ha esito negativo, MakeCert tenterà di utilizzare in caso di scambio delle corrispondenze \_ .</span><span class="sxs-lookup"><span data-stu-id="26082-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="26082-235">Poiché la maggior parte degli utenti ha una chiave di \_ firma o una chiave di scambio delle chiavi \_ , questa opzione non deve essere utilizzata nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="26082-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="26082-236">Le opzioni seguenti sono destinate solo alla tecnologia dell' [*archivio certificati*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="26082-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="26082-237">Opzione archivio certificati</span><span class="sxs-lookup"><span data-stu-id="26082-237">Certificate store option</span></span>          | <span data-ttu-id="26082-238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26082-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26082-239">**-** *IssuerCertFile* IC</span><span class="sxs-lookup"><span data-stu-id="26082-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="26082-240">File che contiene il certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="26082-241">MakeCert effettuerà la ricerca nell'archivio certificati per un certificato con una corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="26082-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="26082-242">**-in** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="26082-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="26082-243">Nome comune del certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="26082-244">MakeCert effettuerà la ricerca nell'archivio certificati per un certificato il cui nome comune include *IssuerNameString*.</span><span class="sxs-lookup"><span data-stu-id="26082-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="26082-245">**-** *IssuerCertStoreLocation* IR</span><span class="sxs-lookup"><span data-stu-id="26082-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="26082-246">Percorso del registro di sistema dell'archivio certificati dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="26082-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="26082-247">*IssuerCertStoreLocation* deve essere **LocalMachine** (chiave del registro di sistema HKEY \_ Local \_ computer) o **CURRENTUSER** (chiave del registro di sistema HKEY \_ Current \_ User).</span><span class="sxs-lookup"><span data-stu-id="26082-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="26082-248">**CurrentUser** è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="26082-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="26082-249">**-è** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="26082-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="26082-250">Archivio certificati dell'autorità emittente che include il certificato dell'autorità emittente e le informazioni sulla chiave privata associata.</span><span class="sxs-lookup"><span data-stu-id="26082-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="26082-251">Se è presente più di un certificato nell'archivio, è necessario che l'utente lo identifichi in modo univoco utilizzando l'opzione **-IC** o **-in** .</span><span class="sxs-lookup"><span data-stu-id="26082-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="26082-252">Se il certificato nell'archivio certificati non è identificato in modo univoco, MakeCert avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="26082-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
