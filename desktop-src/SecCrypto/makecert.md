---
description: Crea un certificato X.509, firmato dalla chiave radice di test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi. Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: Makecert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461c15db364066d9edadb6a0c4d2c24dceab5cc9
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327145"
---
# <a name="makecert"></a><span data-ttu-id="3d108-104">Makecert</span><span class="sxs-lookup"><span data-stu-id="3d108-104">MakeCert</span></span>

> [!Note]  
> <span data-ttu-id="3d108-105">MakeCert è deprecato.</span><span class="sxs-lookup"><span data-stu-id="3d108-105">MakeCert is deprecated.</span></span> <span data-ttu-id="3d108-106">Per creare certificati autofirmati, usare il cmdlet di PowerShell [New-SelfSignedCertificate.](/powershell/module/pki/new-selfsignedcertificate)</span><span class="sxs-lookup"><span data-stu-id="3d108-106">To create self-signed certificates, use the Powershell Cmdlet [New-SelfSignedCertificate](/powershell/module/pki/new-selfsignedcertificate).</span></span>

 

<span data-ttu-id="3d108-107">Lo strumento MakeCert crea un certificato [*X.509,*](../secgloss/x-gly.md) firmato dalla chiave radice di test o da un'altra chiave specificata, che associa il nome alla parte pubblica della coppia di chiavi.</span><span class="sxs-lookup"><span data-stu-id="3d108-107">The MakeCert tool creates an [*X.509*](../secgloss/x-gly.md) certificate, signed by the test root key or other specified key, that binds your name to the public part of the key pair.</span></span> <span data-ttu-id="3d108-108">Il certificato viene salvato in un file, in un archivio certificati di sistema o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="3d108-108">The certificate is saved to a file, a system certificate store, or both.</span></span> <span data-ttu-id="3d108-109">Lo strumento viene installato nella cartella Bin del percorso di \\ installazione di Microsoft Windows Software Development Kit (Windows SDK) (SDK).</span><span class="sxs-lookup"><span data-stu-id="3d108-109">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="3d108-110">Lo strumento MakeCert usa la sintassi di comando seguente:</span><span class="sxs-lookup"><span data-stu-id="3d108-110">The MakeCert tool uses the following command syntax:</span></span>

<span data-ttu-id="3d108-111">**MakeCert** \[ *Opzioni di base* \| *ExtendedOptions* \] *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="3d108-111">**MakeCert** \[*BasicOptions*\|*ExtendedOptions*\] *OutputFile*</span></span>

<span data-ttu-id="3d108-112">*OutputFile* è il nome del file in cui verrà scritto il certificato.</span><span class="sxs-lookup"><span data-stu-id="3d108-112">*OutputFile* is the name of the file where the certificate will be written.</span></span> <span data-ttu-id="3d108-113">È possibile omettere *OutputFile* se il certificato non deve essere scritto in un file.</span><span class="sxs-lookup"><span data-stu-id="3d108-113">You can omit *OutputFile* if the certificate is not to be written to a file.</span></span>

## <a name="options"></a><span data-ttu-id="3d108-114">Opzioni</span><span class="sxs-lookup"><span data-stu-id="3d108-114">Options</span></span>

<span data-ttu-id="3d108-115">MakeCert include opzioni di base ed estese.</span><span class="sxs-lookup"><span data-stu-id="3d108-115">MakeCert includes basic and extended options.</span></span> <span data-ttu-id="3d108-116">Le opzioni di base sono quelle più frequentemente usate nella creazione di certificati.</span><span class="sxs-lookup"><span data-stu-id="3d108-116">Basic options are those most commonly used to create a certificate.</span></span> <span data-ttu-id="3d108-117">Le opzioni estese offrono una maggiore flessibilità.</span><span class="sxs-lookup"><span data-stu-id="3d108-117">Extended options provide more flexibility.</span></span>

<span data-ttu-id="3d108-118">Le opzioni per MakeCert sono suddivise anche in tre gruppi funzionali:</span><span class="sxs-lookup"><span data-stu-id="3d108-118">The options for MakeCert are also divided into three functional groups:</span></span>

-   <span data-ttu-id="3d108-119">Opzioni di base specifiche della tecnologia dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="3d108-119">Basic options specific to certificate store technology only.</span></span>
-   <span data-ttu-id="3d108-120">Opzioni estese specifiche della tecnologia SPC-file e della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="3d108-120">Extended options specific to SPC-file and private key technology only.</span></span>
-   <span data-ttu-id="3d108-121">Opzioni estese applicabili alla tecnologia SPC-file, chiave privata e archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="3d108-121">Extended options applicable to SPC-file, private key, and certificate store technology.</span></span>

<span data-ttu-id="3d108-122">Le opzioni fornite nelle tabelle seguenti possono essere usate solo con Internet Explorer 4.0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="3d108-122">Options given in the following tables can be used only with Internet Explorer 4.0 or later.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d108-123">Opzione di base</span><span class="sxs-lookup"><span data-stu-id="3d108-123">Basic option</span></span></th>
<th><span data-ttu-id="3d108-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d108-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d108-125"><strong>-a</strong> <strong></strong> <em>Algoritmo</em></span><span class="sxs-lookup"><span data-stu-id="3d108-125"><strong>-a</strong> <strong></strong> <em>Algorithm</em></span></span></td>
<td><span data-ttu-id="3d108-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Algoritmo</em></a> hash.</span><span class="sxs-lookup"><span data-stu-id="3d108-126"><a href="/windows/desktop/SecGloss/h-gly"><em>Hash</em></a> algorithm.</span></span> <span data-ttu-id="3d108-127">Deve essere impostato su <strong>SHA-1</strong> o <strong>MD5</strong> (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="3d108-127">Must be set to either <strong>SHA-1</strong> or <strong>MD5</strong> (default).</span></span> <span data-ttu-id="3d108-128">Per informazioni su MD5, vedere <a href="/windows/desktop/SecGloss/m-gly"><em>MD5.</em></a></span><span class="sxs-lookup"><span data-stu-id="3d108-128">For information about MD5, see <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span><span class="sxs-lookup"><span data-stu-id="3d108-129"><strong>-b</strong> <strong></strong> <em>DateStart</em></span></span></td>
<td><span data-ttu-id="3d108-130">Data in cui il certificato diventa valido per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="3d108-130">Date the certificate first becomes valid.</span></span> <span data-ttu-id="3d108-131">Il valore predefinito è quando viene creato il certificato.</span><span class="sxs-lookup"><span data-stu-id="3d108-131">The default is when the certificate is created.</span></span> <span data-ttu-id="3d108-132">Il formato di <em>DateStart</em> è mm/gg/aaaaa.</span><span class="sxs-lookup"><span data-stu-id="3d108-132">The format of <em>DateStart</em> is mm/dd/yyyy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span><span class="sxs-lookup"><span data-stu-id="3d108-133"><strong>-cy</strong> <strong></strong> <em>CertificateTypes</em></span></span></td>
<td><span data-ttu-id="3d108-134">Tipo di certificato.</span><span class="sxs-lookup"><span data-stu-id="3d108-134">Certificate type.</span></span> <span data-ttu-id="3d108-135"><em>CertificateTypes può</em> essere <strong>l'entità</strong> finale o l'autorità <strong>per</strong> <a href="/windows/desktop/SecGloss/c-gly"><em>l'autorità di certificazione</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3d108-135"><em>CertificateTypes</em> can be <strong>end</strong> for end-entity, or <strong>authority</strong> for <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span><span class="sxs-lookup"><span data-stu-id="3d108-136"><strong>-e</strong> <strong></strong> <em>DateEnd</em></span></span></td>
<td><span data-ttu-id="3d108-137">Data di fine del periodo di validità.</span><span class="sxs-lookup"><span data-stu-id="3d108-137">Date when the validity period ends.</span></span> <span data-ttu-id="3d108-138">Il valore predefinito è l'anno 2039.</span><span class="sxs-lookup"><span data-stu-id="3d108-138">The default is the year 2039.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</span><span class="sxs-lookup"><span data-stu-id="3d108-139"><strong>-eku</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> …</span></span></td>
<td><span data-ttu-id="3d108-140">Inserisce nel certificato un elenco di uno o più OID <a href="/windows/desktop/SecGloss/e-gly"><em>(Key Usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>Object Identifier)</em></a> delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="3d108-140">Inserts a list of one or more comma-separated, <a href="/windows/desktop/SecGloss/e-gly"><em>enhanced key usage</em></a> <a href="/windows/desktop/SecGloss/o-gly"><em>object identifiers</em></a> (OIDs) into the certificate.</span></span> <span data-ttu-id="3d108-141">Ad esempio, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserisce l'OID di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="3d108-141">For example, <strong>-eku 1.3.6.1.5.5.7.3.2</strong> inserts the client authentication OID.</span></span> <span data-ttu-id="3d108-142">Per le definizioni degli OID consentiti, vedere il file Wincrypt.h in CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="3d108-142">For definitions of allowable OIDs, see the Wincrypt.h file in CryptoAPI 2.0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span><span class="sxs-lookup"><span data-stu-id="3d108-143"><strong>-h</strong> <strong></strong> <em>NumChildren</em></span></span></td>
<td><span data-ttu-id="3d108-144">Altezza massima dell'albero sotto questo certificato.</span><span class="sxs-lookup"><span data-stu-id="3d108-144">Maximum height of the tree below this certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span><span class="sxs-lookup"><span data-stu-id="3d108-145"><strong>-l</strong> <strong></strong> <em>PolicyLink</em></span></span></td>
<td><span data-ttu-id="3d108-146">Collegamento alle informazioni sui criteri dell'agenzia SPC (ad esempio, un URL).</span><span class="sxs-lookup"><span data-stu-id="3d108-146">Link to SPC agency policy information (for example, a URL).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span><span class="sxs-lookup"><span data-stu-id="3d108-147"><strong>-m</strong> <strong></strong> <em>nMonths</em></span></span></td>
<td><span data-ttu-id="3d108-148">Durata del periodo di validità.</span><span class="sxs-lookup"><span data-stu-id="3d108-148">Duration of the validity period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-149"><strong>-n</strong> <strong>&quot;</strong> <em>Nome</em><strong>&quot;</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-149"><strong>-n</strong> <strong>&quot;</strong><em>Name</em><strong>&quot;</strong></span></span></td>
<td><span data-ttu-id="3d108-150">Nome del certificato dell'editore.</span><span class="sxs-lookup"><span data-stu-id="3d108-150">Name for the publisher's certificate.</span></span> <span data-ttu-id="3d108-151">Questo nome deve essere conforme allo standard <a href="/windows/desktop/SecGloss/x-gly"><em>X.500.</em></a></span><span class="sxs-lookup"><span data-stu-id="3d108-151">This name must conform to the <a href="/windows/desktop/SecGloss/x-gly"><em>X.500</em></a> standard.</span></span> <span data-ttu-id="3d108-152">Il metodo più semplice è usare il &quot; formato CN=<em>MyName.</em> &quot;</span><span class="sxs-lookup"><span data-stu-id="3d108-152">The simplest method is to use the &quot;CN=<em>MyName</em>&quot; format.</span></span> <span data-ttu-id="3d108-153">Ad esempio: <strong>-n &quot; CN=Test &quot; </strong>.</span><span class="sxs-lookup"><span data-stu-id="3d108-153">For example: <strong>-n &quot;CN=Test&quot;</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-154"><strong>-nscp</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-154"><strong>-nscp</strong></span></span></td>
<td><span data-ttu-id="3d108-155">È necessario includere l'estensione di autenticazione client Netscape.</span><span class="sxs-lookup"><span data-stu-id="3d108-155">The Netscape client authentication extension should be included.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-156"><strong>-pe</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-156"><strong>-pe</strong></span></span></td>
<td><span data-ttu-id="3d108-157">Contrassegna la chiave privata come esportabile.</span><span class="sxs-lookup"><span data-stu-id="3d108-157">Marks the private key as exportable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-158"><strong>-r</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-158"><strong>-r</strong></span></span></td>
<td><span data-ttu-id="3d108-159">Crea un certificato autofirmato.</span><span class="sxs-lookup"><span data-stu-id="3d108-159">Creates a self-signed certificate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span><span class="sxs-lookup"><span data-stu-id="3d108-160"><strong>-sc</strong> <strong></strong> <em>SubjectCertFile</em></span></span></td>
<td><span data-ttu-id="3d108-161">Nome file del certificato con la chiave pubblica del soggetto esistente da usare.</span><span class="sxs-lookup"><span data-stu-id="3d108-161">Certificate file name with the existing subject public key to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-162"><strong>-sk</strong> <strong></strong> <em>Chiave oggetto</em></span><span class="sxs-lookup"><span data-stu-id="3d108-162"><strong>-sk</strong> <strong></strong> <em>SubjectKey</em></span></span></td>
<td><span data-ttu-id="3d108-163">Posizione del contenitore di chiavi dell'oggetto che contiene la <a href="/windows/desktop/SecGloss/p-gly"><em>chiave privata</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3d108-163">Location of the subject's key container which holds the <a href="/windows/desktop/SecGloss/p-gly"><em>private key</em></a>.</span></span> <span data-ttu-id="3d108-164">Se non esiste alcun contenitore di chiavi, ne viene creato uno.</span><span class="sxs-lookup"><span data-stu-id="3d108-164">If a key container does not exist, one is created.</span></span> <span data-ttu-id="3d108-165">Se non si <strong>usa l'opzione -sk</strong> o <strong>-sv,</strong> per impostazione predefinita viene creato e usato un contenitore di chiavi predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d108-165">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="3d108-166"><strong>-sky</strong> <strong></strong> <em>SubjectKeySpec</em></span></span></td>
<td><span data-ttu-id="3d108-167">Specifica della chiave del soggetto.</span><span class="sxs-lookup"><span data-stu-id="3d108-167">Subject's key specification.</span></span> <span data-ttu-id="3d108-168"><em>SubjectKeySpec</em> deve essere uno dei tre valori possibili:</span><span class="sxs-lookup"><span data-stu-id="3d108-168"><em>SubjectKeySpec</em> must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="3d108-169"><strong>Firma</strong> (AT_SIGNATURE specifica della chiave)</span><span class="sxs-lookup"><span data-stu-id="3d108-169"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="3d108-170"><strong>Exchange</strong> (AT_KEYEXCHANGE specifica della chiave)</span><span class="sxs-lookup"><span data-stu-id="3d108-170"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="3d108-171">Intero, ad esempio <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-171">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="3d108-172">Per altre informazioni, vedere la nota che segue questa tabella.</span><span class="sxs-lookup"><span data-stu-id="3d108-172">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span><span class="sxs-lookup"><span data-stu-id="3d108-173"><strong>-sp</strong> <strong></strong> <em>SubjectProviderName</em></span></span></td>
<td><span data-ttu-id="3d108-174">Provider CryptoAPI per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d108-174">CryptoAPI provider for subject.</span></span> <span data-ttu-id="3d108-175">Il valore predefinito è il provider dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3d108-175">The default is the user's provider.</span></span> <span data-ttu-id="3d108-176">Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="3d108-176">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span><span class="sxs-lookup"><span data-stu-id="3d108-177"><strong>-sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></span></span></td>
<td><span data-ttu-id="3d108-178">Percorso del Registro di sistema dell'archivio certificati del soggetto.</span><span class="sxs-lookup"><span data-stu-id="3d108-178">Registry location of the subject's certificate store.</span></span> <span data-ttu-id="3d108-179"><em>SubjectCertStoreLocation</em> deve essere <strong>LocalMachine (chiave</strong> del Registro di sistema HKEY_LOCAL_MACHINE) o <strong>CurrentUser</strong> (chiave del Registro di sistema HKEY_CURRENT_USER).</span><span class="sxs-lookup"><span data-stu-id="3d108-179"><em>SubjectCertStoreLocation</em> must be either <strong>LocalMachine</strong> (registry key HKEY_LOCAL_MACHINE) or <strong>CurrentUser</strong> (registry key HKEY_CURRENT_USER).</span></span> <span data-ttu-id="3d108-180"><strong>CurrentUser</strong> è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3d108-180"><strong>CurrentUser</strong> is the default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span><span class="sxs-lookup"><span data-stu-id="3d108-181"><strong>-ss</strong> <strong></strong> <em>SubjectCertStoreName</em></span></span></td>
<td><span data-ttu-id="3d108-182">Nome dell'archivio certificati del soggetto in cui verrà archiviato il certificato generato.</span><span class="sxs-lookup"><span data-stu-id="3d108-182">Name of the subject's certificate store where the generated certificate will be stored.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="3d108-183"><strong>-sv</strong> <strong></strong> <em>SubjectKeyFile</em></span></span></td>
<td><span data-ttu-id="3d108-184">Nome del file con estensione pvk dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d108-184">Name of the subject's .pvk file.</span></span> <span data-ttu-id="3d108-185">Se non viene <strong>usata l'opzione -sk</strong> o <strong>-sv,</strong> per impostazione predefinita viene creato e usato un contenitore di chiavi predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d108-185">If neither the <strong>-sk</strong> or <strong>-sv</strong> option is used, a default key container is created and used by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span><span class="sxs-lookup"><span data-stu-id="3d108-186"><strong>-sy</strong> <strong></strong> <em>nSubjectProviderType</em></span></span></td>
<td><span data-ttu-id="3d108-187">Tipo di provider CryptoAPI per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d108-187">CryptoAPI provider type for subject.</span></span> <span data-ttu-id="3d108-188">Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3d108-188">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="3d108-189">Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0 cryptoapi.</span><span class="sxs-lookup"><span data-stu-id="3d108-189">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-190"><strong>-#</strong><strong></strong> <em>SerialNumber</em></span><span class="sxs-lookup"><span data-stu-id="3d108-190"><strong>-#</strong> <strong></strong> <em>SerialNumber</em></span></span></td>
<td><span data-ttu-id="3d108-191">Numero di serie del certificato.</span><span class="sxs-lookup"><span data-stu-id="3d108-191">Serial number of the certificate.</span></span> <span data-ttu-id="3d108-192">Il valore massimo è 2^31.</span><span class="sxs-lookup"><span data-stu-id="3d108-192">The maximum value is 2^31.</span></span> <span data-ttu-id="3d108-193">Il valore predefinito è un valore generato dallo strumento che è garantito come univoco.</span><span class="sxs-lookup"><span data-stu-id="3d108-193">The default is a value generated by the tool that is guaranteed to be unique.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-194"><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></span><span class="sxs-lookup"><span data-stu-id="3d108-194"><strong>-$</strong> <strong></strong> <em>CertificateAuthority</em></span></span></td>
<td><span data-ttu-id="3d108-195">Tipo di <a href="/windows/desktop/SecGloss/c-gly"><em>autorità di certificazione</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3d108-195">Type of <a href="/windows/desktop/SecGloss/c-gly"><em>certification authority</em></a>.</span></span> <span data-ttu-id="3d108-196"><em>CertificateAuthority</em> deve essere impostato su <strong>commerciale</strong> (per i certificati che devono essere usati da editori di software commerciali) o su <strong>singolo</strong> (per i certificati che devono essere usati da singoli editori di software).</span><span class="sxs-lookup"><span data-stu-id="3d108-196"><em>CertificateAuthority</em> must be set to either <strong>commercial</strong> (for certificates to be used by commercial software publishers) or <strong>individual</strong> (for certificates to be used by individual software publishers).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-197"><strong>-?</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-197"><strong>-?</strong></span></span></td>
<td><span data-ttu-id="3d108-198">Visualizza le opzioni di base.</span><span class="sxs-lookup"><span data-stu-id="3d108-198">Displays the basic options.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-199"><strong>-!</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-199"><strong>-!</strong></span></span></td>
<td><span data-ttu-id="3d108-200">Visualizza le opzioni estese.</span><span class="sxs-lookup"><span data-stu-id="3d108-200">Displays the extended options.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="3d108-201">Se l'opzione **-sky** key specification viene usata in Internet Explorer versione 4.0 o successiva, la specifica deve corrispondere alla specifica della chiave indicata dal [*file*](../secgloss/p-gly.md) di chiave privata o dal contenitore di [*chiavi private*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3d108-201">If the **-sky** key specification option is used in Internet Explorer version 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="3d108-202">Se l'opzione di specifica della chiave non viene usata, verrà usata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="3d108-202">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="3d108-203">Se nel contenitore di chiavi sono presenti più specifiche di chiave, MakeCert tenterà prima di tutto di usare la specifica della chiave AT \_ SIGNATURE.</span><span class="sxs-lookup"><span data-stu-id="3d108-203">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="3d108-204">Se l'operazione non riesce, MakeCert tenterà di usare AT \_ KEYEXCHANGE.</span><span class="sxs-lookup"><span data-stu-id="3d108-204">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="3d108-205">Poiché la maggior parte degli utenti ha una chiave AT SIGNATURE o una chiave AT KEYEXCHANGE, questa opzione non deve essere usata nella maggior \_ \_ parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="3d108-205">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="3d108-206">Le opzioni seguenti sono disponibili solo per i file SPC [*(Software Publisher Certificate)*](../secgloss/s-gly.md) e la tecnologia della chiave privata.</span><span class="sxs-lookup"><span data-stu-id="3d108-206">The following options are only for [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) files and private key technology.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d108-207">Opzione SPC e chiave privata</span><span class="sxs-lookup"><span data-stu-id="3d108-207">SPC and private key option</span></span></th>
<th><span data-ttu-id="3d108-208">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d108-208">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d108-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span><span class="sxs-lookup"><span data-stu-id="3d108-209"><strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em></span></span></td>
<td><span data-ttu-id="3d108-210">Percorso del certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-210">Location of the issuer's certificate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span><span class="sxs-lookup"><span data-stu-id="3d108-211"><strong>-ik</strong> <strong></strong> <em>IssuerKey</em></span></span></td>
<td><span data-ttu-id="3d108-212">Percorso del contenitore di chiavi dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-212">Location of the issuer's key container.</span></span> <span data-ttu-id="3d108-213">Il valore predefinito è la chiave radice di test.</span><span class="sxs-lookup"><span data-stu-id="3d108-213">The default is the test root key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span><span class="sxs-lookup"><span data-stu-id="3d108-214"><strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em></span></span></td>
<td><span data-ttu-id="3d108-215">Specifica della chiave dell'autorità emittente, che deve essere uno dei tre valori possibili:</span><span class="sxs-lookup"><span data-stu-id="3d108-215">Issuer's key specification, which must be one of three possible values:</span></span><br/>
<ul>
<li><span data-ttu-id="3d108-216"><strong>Firma</strong> (AT_SIGNATURE specifica della chiave)</span><span class="sxs-lookup"><span data-stu-id="3d108-216"><strong>Signature</strong> (AT_SIGNATURE key specification)</span></span></li>
<li><span data-ttu-id="3d108-217"><strong>Exchange</strong> (AT_KEYEXCHANGE specifica della chiave)</span><span class="sxs-lookup"><span data-stu-id="3d108-217"><strong>Exchange</strong> (AT_KEYEXCHANGE key specification)</span></span></li>
<li><span data-ttu-id="3d108-218">Intero, ad esempio <strong>3</strong></span><span class="sxs-lookup"><span data-stu-id="3d108-218">An integer, such as <strong>3</strong></span></span></li>
</ul>
<span data-ttu-id="3d108-219">Per altre informazioni, vedere la nota che segue questa tabella.</span><span class="sxs-lookup"><span data-stu-id="3d108-219">For more information, see the Note that follows this table.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span><span class="sxs-lookup"><span data-stu-id="3d108-220"><strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em></span></span></td>
<td><span data-ttu-id="3d108-221">Provider CryptoAPI per l'autorità di emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-221">CryptoAPI provider for issuer.</span></span> <span data-ttu-id="3d108-222">Il valore predefinito è il provider dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3d108-222">The default is the user's provider.</span></span> <span data-ttu-id="3d108-223">Per informazioni sui provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="3d108-223">For information about CryptoAPI providers, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d108-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span><span class="sxs-lookup"><span data-stu-id="3d108-224"><strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em></span></span></td>
<td><span data-ttu-id="3d108-225">File di chiave privata dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-225">Issuer's private key file.</span></span> <span data-ttu-id="3d108-226">Il valore predefinito è la radice del test.</span><span class="sxs-lookup"><span data-stu-id="3d108-226">The default is the test root.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d108-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span><span class="sxs-lookup"><span data-stu-id="3d108-227"><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></span></span></td>
<td><span data-ttu-id="3d108-228">Tipo di provider CryptoAPI per l'autorità di emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-228">CryptoAPI provider type for issuer.</span></span> <span data-ttu-id="3d108-229">Il valore predefinito è <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span><span class="sxs-lookup"><span data-stu-id="3d108-229">The default is <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>.</span></span> <span data-ttu-id="3d108-230">Per informazioni sui tipi di provider CryptoAPI, vedere la documentazione CryptoAPI 2.0.</span><span class="sxs-lookup"><span data-stu-id="3d108-230">For information about CryptoAPI provider types, see the CryptoAPI 2.0 documentation.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="3d108-231">Se l'opzione **-iky** key specification viene usata in Internet Explorer 4.0 o versione successiva, la specifica deve corrispondere alla specifica della chiave indicata dal [*file*](../secgloss/p-gly.md) di chiave privata o dal contenitore di [*chiavi private*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3d108-231">If the **-iky** key specification option is used in Internet Explorer 4.0 or later, the specification must match the key specification indicated by the [*private key*](../secgloss/p-gly.md) file or private [*key container*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="3d108-232">Se l'opzione di specifica della chiave non viene usata, verrà usata la specifica della chiave indicata dal file di chiave privata o dal contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="3d108-232">If the key specification option is not used, the key specification indicated by the private key file or private key container will be used.</span></span> <span data-ttu-id="3d108-233">Se nel contenitore di chiavi sono presenti più specifiche di chiave, MakeCert tenterà prima di tutto di usare la specifica della chiave AT \_ SIGNATURE.</span><span class="sxs-lookup"><span data-stu-id="3d108-233">If there is more than one key specification in the key container, MakeCert will first attempt to use the AT\_SIGNATURE key specification.</span></span> <span data-ttu-id="3d108-234">Se l'operazione non riesce, MakeCert tenterà di usare AT \_ KEYEXCHANGE.</span><span class="sxs-lookup"><span data-stu-id="3d108-234">If that fails, MakeCert will try to use AT\_KEYEXCHANGE.</span></span> <span data-ttu-id="3d108-235">Poiché la maggior parte degli utenti ha una chiave AT SIGNATURE o una chiave AT KEYEXCHANGE, questa opzione non deve essere usata nella maggior \_ \_ parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="3d108-235">Because most users have either an AT\_SIGNATURE key or an AT\_KEYEXCHANGE key, this option does not need to be used in most cases.</span></span>

 

<span data-ttu-id="3d108-236">Le opzioni seguenti sono solo per la [*tecnologia dell'archivio*](../secgloss/c-gly.md) certificati.</span><span class="sxs-lookup"><span data-stu-id="3d108-236">The following options are for [*certificate store*](../secgloss/c-gly.md) technology only.</span></span>



| <span data-ttu-id="3d108-237">Opzione dell'archivio certificati</span><span class="sxs-lookup"><span data-stu-id="3d108-237">Certificate store option</span></span>          | <span data-ttu-id="3d108-238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d108-238">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d108-239">**-ic** *IssuerCertFile*</span><span class="sxs-lookup"><span data-stu-id="3d108-239">**-ic** *IssuerCertFile*</span></span>          | <span data-ttu-id="3d108-240">File contenente il certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-240">File that contains the issuer's certificate.</span></span> <span data-ttu-id="3d108-241">MakeCert cerca nell'archivio certificati un certificato con una corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="3d108-241">MakeCert will search in the certificate store for a certificate with an exact match.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="3d108-242">**-in** *IssuerNameString*</span><span class="sxs-lookup"><span data-stu-id="3d108-242">**-in** *IssuerNameString*</span></span>        | <span data-ttu-id="3d108-243">Nome comune del certificato dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-243">Common name of the issuer's certificate.</span></span> <span data-ttu-id="3d108-244">MakeCert cerca nell'archivio certificati un certificato il cui nome comune include *IssuerNameString*.</span><span class="sxs-lookup"><span data-stu-id="3d108-244">MakeCert will search in the certificate store for a certificate whose common name includes *IssuerNameString*.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="3d108-245">**-ir** *IssuerCertStoreLocation*</span><span class="sxs-lookup"><span data-stu-id="3d108-245">**-ir** *IssuerCertStoreLocation*</span></span> | <span data-ttu-id="3d108-246">Percorso del Registro di sistema dell'archivio certificati dell'autorità emittente.</span><span class="sxs-lookup"><span data-stu-id="3d108-246">Registry location of the issuer's certificate store.</span></span> <span data-ttu-id="3d108-247">*IssuerCertStoreLocation* deve essere **LocalMachine** (chiave del Registro di sistema HKEY LOCAL MACHINE) o \_ \_ **CurrentUser** (chiave del Registro di sistema HKEY \_ CURRENT \_ USER).</span><span class="sxs-lookup"><span data-stu-id="3d108-247">*IssuerCertStoreLocation* must be either **LocalMachine** (registry key HKEY\_LOCAL\_MACHINE) or **CurrentUser** (registry key HKEY\_CURRENT\_USER).</span></span> <span data-ttu-id="3d108-248">**CurrentUser** è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3d108-248">**CurrentUser** is the default.</span></span>                                                                                                |
| <span data-ttu-id="3d108-249">**-is** *IssuerCertStoreName*</span><span class="sxs-lookup"><span data-stu-id="3d108-249">**-is** *IssuerCertStoreName*</span></span>     | <span data-ttu-id="3d108-250">Archivio certificati dell'autorità emittente che include il certificato dell'autorità emittente e le informazioni sulla chiave privata associata.</span><span class="sxs-lookup"><span data-stu-id="3d108-250">Issuer's certificate store that includes the issuer's certificate and its associated private key information.</span></span> <span data-ttu-id="3d108-251">Se nell'archivio sono presenti più certificati, l'utente deve identificarlo in modo univoco usando l'opzione **-ic** o **-in.**</span><span class="sxs-lookup"><span data-stu-id="3d108-251">If there is more than one certificate in the store, the user must uniquely identify it by using the **-ic** or **-in** option.</span></span> <span data-ttu-id="3d108-252">Se il certificato nell'archivio certificati non è identificato in modo univoco, MakeCert avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3d108-252">If the certificate in the certificate store is not uniquely identified, MakeCert will fail.</span></span> |



 

 

 
