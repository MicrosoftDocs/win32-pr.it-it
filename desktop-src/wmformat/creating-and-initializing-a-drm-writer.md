---
title: Creazione e inizializzazione di un writer DRM
description: Creazione e inizializzazione di un writer DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK, writer DRM
- Digital Rights Management (DRM), creazione di writer DRM
- DRM (Digital Rights Management), creazione di writer DRM
- Digital Rights Management (DRM), inizializzazione di writer DRM
- DRM (Digital Rights Management), inizializzazione di writer DRM
- API estese del client DRM, writer DRM
- API estese client, writer DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300614"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="5cb42-110">Creazione e inizializzazione di un writer DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="5cb42-111">I passaggi seguenti sono necessari per inizializzare un oggetto writer ASF per l'importazione di esempi di supporti crittografati in Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="5cb42-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="5cb42-112">Eseguire i passaggi da 1 a 4 di [importazione della licenza e del materiale della chiave](importing-license-and-key-material.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="5cb42-113">Creare e inizializzare un oggetto writer ASF utilizzando il materiale della chiave DRM di Windows Media appropriato.</span><span class="sxs-lookup"><span data-stu-id="5cb42-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="5cb42-114">Per ulteriori informazioni, vedere [Abilitazione del supporto DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="5cb42-115">Impostare ciascuno dei seguenti attributi chiamando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span><span class="sxs-lookup"><span data-stu-id="5cb42-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="5cb42-116">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="5cb42-117">\_V1LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="5cb42-118">\_KEYID DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="5cb42-119">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="5cb42-120">Se una versione con licenza di Windows Media Rights Manager non è installata nel computer in cui è in esecuzione il software, è necessario impostare anche i quattro attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5cb42-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="5cb42-121">\_LASIGNATUREROOTCERT DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="5cb42-122">\_LASIGNATURECERT DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="5cb42-123">\_LASIGNATURELICSRVCERT DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="5cb42-124">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="5cb42-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="5cb42-125">Per completare l'applicazione per i certificati di crittografia necessari, compilare il [contratto di licenza di Windows Media (WMLA)](https://www.microsoft.com/licensing/default) online.</span><span class="sxs-lookup"><span data-stu-id="5cb42-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="5cb42-126">Creare una chiave di sessione e compilare una struttura di [**\_ chiave della \_ sessione \_ di importazione WMDRM**](wmdrm-import-session-key.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb42-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="5cb42-127">La chiave della sessione verrà usata per crittografare una chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="5cb42-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="5cb42-128">Per un esempio, vedere [esempio di creazione](create-session-key-example.md)di una chiave di sessione.</span><span class="sxs-lookup"><span data-stu-id="5cb42-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="5cb42-129">Creare una chiave simmetrica da un vettore di inizializzazione RC4 casuale e compilare una struttura [**WMDRM \_ import \_ Content \_ Key**](wmdrm-import-content-key.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb42-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="5cb42-130">La chiave simmetrica viene usata per crittografare gli esempi di contenuti multimediali.</span><span class="sxs-lookup"><span data-stu-id="5cb42-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="5cb42-131">Per un esempio, vedere [creare una chiave](create-content-key-example.md)simmetrica di esempio.</span><span class="sxs-lookup"><span data-stu-id="5cb42-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="5cb42-132">Crittografare la chiave simmetrica con la chiave della sessione, usando la crittografia RC4.</span><span class="sxs-lookup"><span data-stu-id="5cb42-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="5cb42-133">Estrarre la chiave di raccolta del certificato del computer.</span><span class="sxs-lookup"><span data-stu-id="5cb42-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="5cb42-134">Per un esempio, vedere [ottenere un certificato del computer](get-machine-certificate-example.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="5cb42-135">Crittografare la chiave della sessione con la chiave pubblica estratta dal certificato.</span><span class="sxs-lookup"><span data-stu-id="5cb42-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="5cb42-136">Compilare una struttura [**\_ \_ \_ struct di importazione WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="5cb42-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="5cb42-137">Chiamare il metodo [**IWMDRMWriter3:: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) per inviare una notifica all'SDK che i campioni che entrano nel writer sono già protetti e devono essere inviati direttamente al client Windows Media DRM per l'importazione.</span><span class="sxs-lookup"><span data-stu-id="5cb42-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="5cb42-138">Chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="5cb42-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="5cb42-139">I passaggi rimanenti per la creazione di un file protetto da DRM sono documentati nella Guida alla programmazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5cb42-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="5cb42-140">Per ulteriori informazioni, vedere [creazione di file protetti](creating-protected-files.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="5cb42-141">Il passaggio successivo consiste nell'eseguire l'iterazione di ogni esempio multimediale, crittografarlo e passarlo all'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="5cb42-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="5cb42-142">Per ulteriori informazioni, vedere la pagina relativa alla [crittografia e all'importazione di esempi di supporti](encrypting-and-importing-media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cb42-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cb42-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cb42-144">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="5cb42-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="5cb42-145">**Importazione DRM**</span><span class="sxs-lookup"><span data-stu-id="5cb42-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




