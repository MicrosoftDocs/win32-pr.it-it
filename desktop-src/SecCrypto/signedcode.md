---
description: Fornisce funzionalità per la firma di file eseguibili con una firma digitale Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Oggetto SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332833"
---
# <a name="signedcode-object"></a><span data-ttu-id="7ec3a-103">Oggetto SignedCode</span><span class="sxs-lookup"><span data-stu-id="7ec3a-103">SignedCode object</span></span>

<span data-ttu-id="7ec3a-104">\[L'oggetto **SignedCode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-104">\[The **SignedCode** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ec3a-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="7ec3a-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ec3a-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7ec3a-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="7ec3a-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7ec3a-108">L'oggetto **SignedCode** fornisce la funzionalità per la firma dei file eseguibili con una firma digitale Authenticode.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-108">The **SignedCode** object provides functionality for signing executable files with an Authenticode digital signature.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7ec3a-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="7ec3a-109">When to use</span></span>

<span data-ttu-id="7ec3a-110">L'oggetto **SignedCode** viene usato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ec3a-110">The **SignedCode** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="7ec3a-111">Firma i file eseguibili.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-111">Sign executable files.</span></span>
-   <span data-ttu-id="7ec3a-112">File eseguibili timestamp.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-112">Time stamp executable files.</span></span>
-   <span data-ttu-id="7ec3a-113">Determinare se la firma del file eseguibile è valida.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-113">Determine whether the signature of the executable file is valid.</span></span>
-   <span data-ttu-id="7ec3a-114">Consente di impostare o recuperare il percorso del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-114">Set or retrieve the path to the executable file.</span></span>
-   <span data-ttu-id="7ec3a-115">Recuperare il firmatario e l'indicatore di data e ora del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-115">Retrieve the signer and time stamper of the executable file.</span></span>
-   <span data-ttu-id="7ec3a-116">Recuperare una raccolta di certificati per il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-116">Retrieve a collection of the certificates for the executable file.</span></span>
-   <span data-ttu-id="7ec3a-117">Recuperare una descrizione o l'URL per la descrizione del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-117">Retrieve a description or the URL to the description of the executable file.</span></span>

## <a name="members"></a><span data-ttu-id="7ec3a-118">Membri</span><span class="sxs-lookup"><span data-stu-id="7ec3a-118">Members</span></span>

<span data-ttu-id="7ec3a-119">L'oggetto **SignedCode** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7ec3a-119">The **SignedCode** object has these types of members:</span></span>

-   [<span data-ttu-id="7ec3a-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="7ec3a-120">Methods</span></span>](#methods)
-   [<span data-ttu-id="7ec3a-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ec3a-121">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7ec3a-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="7ec3a-122">Methods</span></span>

<span data-ttu-id="7ec3a-123">L'oggetto **SignedCode** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-123">The **SignedCode** object has these methods.</span></span>



| <span data-ttu-id="7ec3a-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="7ec3a-124">Method</span></span>                                    | <span data-ttu-id="7ec3a-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ec3a-125">Description</span></span>                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ec3a-126">**Sign**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-126">**Sign**</span></span>](signedcode-sign.md)           | <span data-ttu-id="7ec3a-127">Crea una firma digitale Authenticode e firma il file eseguibile specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec3a-127">Creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>    |
| [<span data-ttu-id="7ec3a-128">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-128">**Timestamp**</span></span>](signedcode-timestamp.md) | <span data-ttu-id="7ec3a-129">Crea una firma di timestamp Authenticode sul file eseguibile firmato specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec3a-129">Creates an Authenticode time stamp signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/> |
| [<span data-ttu-id="7ec3a-130">**Verificare**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-130">**Verify**</span></span>](signedcode-verify.md)       | <span data-ttu-id="7ec3a-131">Verifica la firma Authenticode nel file eseguibile firmato specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="7ec3a-131">Verifies the Authenticode signature on the signed executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="7ec3a-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ec3a-132">Properties</span></span>

<span data-ttu-id="7ec3a-133">L'oggetto **SignedCode** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-133">The **SignedCode** object has these properties.</span></span>



| <span data-ttu-id="7ec3a-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ec3a-134">Property</span></span>                                                       | <span data-ttu-id="7ec3a-135">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7ec3a-135">Access type</span></span>           | <span data-ttu-id="7ec3a-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ec3a-136">Description</span></span>                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ec3a-137">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-137">**Certificates**</span></span>](signedcode-certificates.md)<br/>     | <span data-ttu-id="7ec3a-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ec3a-138">Read-only</span></span><br/>  | <span data-ttu-id="7ec3a-139">Raccolta di [**certificati**](certificates.md) che contiene tutti i certificati nel file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-139">A [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span><br/>             |
| [<span data-ttu-id="7ec3a-140">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-140">**Description**</span></span>](signedcode-description.md)<br/>       | <span data-ttu-id="7ec3a-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7ec3a-141">Read/write</span></span><br/> | <span data-ttu-id="7ec3a-142">Stringa che contiene una descrizione del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-142">A string that contains a description of the signed executable file.</span></span><br/>                                                             |
| [<span data-ttu-id="7ec3a-143">**DescriptionURL**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-143">**DescriptionURL**</span></span>](signedcode-descriptionurl.md)<br/> | <span data-ttu-id="7ec3a-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7ec3a-144">Read/write</span></span><br/> | <span data-ttu-id="7ec3a-145">Stringa che contiene l'indirizzo HTTP a una descrizione del file eseguibile firmato.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-145">A string that contains the HTTP address to a description of the signed executable file.</span></span><br/>                                         |
| [<span data-ttu-id="7ec3a-146">**FileName**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-146">**FileName**</span></span>](signedcode-filename.md)<br/>             | <span data-ttu-id="7ec3a-147">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7ec3a-147">Read/write</span></span><br/> | <span data-ttu-id="7ec3a-148">Stringa che contiene il percorso del file di contenuto contenente il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-148">A string that contains the path to the content file that contains the executable file.</span></span><br/> <span data-ttu-id="7ec3a-149">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-149">This is the default property.</span></span><br/> |
| [<span data-ttu-id="7ec3a-150">**Firmatario**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-150">**Signer**</span></span>](signedcode-signer.md)<br/>                 | <span data-ttu-id="7ec3a-151">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ec3a-151">Read-only</span></span><br/>  | <span data-ttu-id="7ec3a-152">Oggetto [**firmatario**](signer.md) che fornisce l'accesso al firmatario del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-152">A [**Signer**](signer.md) object that provides access to the signer of the executable file.</span></span><br/>                                    |
| [<span data-ttu-id="7ec3a-153">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="7ec3a-153">**Timestamper**</span></span>](signedcode-timestamper.md)<br/>       | <span data-ttu-id="7ec3a-154">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ec3a-154">Read-only</span></span><br/>  | <span data-ttu-id="7ec3a-155">Oggetto [**firmatario**](signer.md) che fornisce l'accesso al timestamp del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-155">A [**Signer**](signer.md) object that provides access to the time stamper of the executable file.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="7ec3a-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ec3a-156">Remarks</span></span>

<span data-ttu-id="7ec3a-157">È possibile creare l'oggetto **SignedCode** e non è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-157">The **SignedCode** object can be created, and is not safe for scripting.</span></span> <span data-ttu-id="7ec3a-158">Il ProgID per l'oggetto **SignedCode** è capicom. SignedCode. 1.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-158">The ProgID for the **SignedCode** object is CAPICOM.SignedCode.1.</span></span>

<span data-ttu-id="7ec3a-159">Il file eseguibile deve essere di un tipo che può essere firmato con la tecnologia Authenticode, ad esempio i file con estensione cab, cat, exe, dll, vbs o ocx.</span><span class="sxs-lookup"><span data-stu-id="7ec3a-159">The executable file should be of a type that can be signed with Authenticode technology, for example, files that have a file name extension of .cab, .cat, .exe, .dll, .vbs, or .ocx.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec3a-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ec3a-160">Requirements</span></span>



| <span data-ttu-id="7ec3a-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ec3a-161">Requirement</span></span> | <span data-ttu-id="7ec3a-162">Valore</span><span class="sxs-lookup"><span data-stu-id="7ec3a-162">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec3a-163">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7ec3a-163">Redistributable</span></span><br/> | <span data-ttu-id="7ec3a-164">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ec3a-164">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7ec3a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec3a-165">DLL</span></span><br/>             | <dl> <span data-ttu-id="7ec3a-166"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec3a-166"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
