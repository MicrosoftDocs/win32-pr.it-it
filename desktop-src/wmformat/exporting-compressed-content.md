---
title: Esportazione di contenuto compresso
description: Esportazione di contenuto compresso
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK, esportazione DRM
- Windows Media Format SDK, esportazione
- Windows Media Format SDK, contenuto compresso
- Digital Rights Management (DRM), esportazione
- DRM (Digital Rights Management), esportazione
- Digital Rights Management (DRM), contenuto compresso
- DRM (Digital Rights Management), contenuto compresso
- API estese del client DRM, contenuto compresso
- API estese client, contenuto compresso
- API estese del client DRM, esportazione
- API estese client, esportazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855918"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="29891-114">Esportazione di contenuto compresso</span><span class="sxs-lookup"><span data-stu-id="29891-114">Exporting Compressed Content</span></span>

<span data-ttu-id="29891-115">In questa sezione viene descritta l'esportazione di supporti DRM protetti con Windows Media in un file Windows Media in cui l'applicazione riceve dati multimediali digitali compressi.</span><span class="sxs-lookup"><span data-stu-id="29891-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="29891-116">A tale scopo, l'applicazione deve eseguire la decrittografia inline di tutti i payload crittografati DRM di Windows Media in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="29891-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="29891-117">Una libreria di analisi ASF viene fornita all'utente come parte del contratto di esportazione DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="29891-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="29891-118">I passaggi principali necessari per esportare il contenuto compresso sono:</span><span class="sxs-lookup"><span data-stu-id="29891-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="29891-119">Se necessario, eseguire l'individualizzazione DRM.</span><span class="sxs-lookup"><span data-stu-id="29891-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="29891-120">Verificare che lo schema di protezione del contenuto di destinazione sia consentito in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="29891-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="29891-121">Creare un oggetto di decrittografia per decrittografare ogni payload ASF.</span><span class="sxs-lookup"><span data-stu-id="29891-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="29891-122">Il sistema DRM transcrypta ogni payload ASF da Windows Media DRM in RC4 prima di passarlo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="29891-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="29891-123">Se l'applicazione modifica la dimensione di un payload ASF durante la transcryption, è necessario rimultiplexare anche il file ASF.</span><span class="sxs-lookup"><span data-stu-id="29891-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="29891-124">Passare alla libreria stub un certificato dell'applicazione Windows Media DRM Export.</span><span class="sxs-lookup"><span data-stu-id="29891-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="29891-125">Il certificato viene verificato e, se è valido, il sistema DRM genera un vettore di inizializzazione e lo crittografa usando RSA OAEP.</span><span class="sxs-lookup"><span data-stu-id="29891-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="29891-126">Viene creata una chiave di sessione RC4 per ogni payload concatenando il vettore di inizializzazione e un valore salt.</span><span class="sxs-lookup"><span data-stu-id="29891-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="29891-127">Il valore salt viene fornito all'API di decrittografia ed è necessario incrementarlo per un valore integer positivo diverso da zero per ogni payload.</span><span class="sxs-lookup"><span data-stu-id="29891-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="29891-128">Verrà fornito uno strumento di Microsoft nell'ambito del contratto di esportazione DRM di Windows Media che consente di generare una coppia di chiavi pubblica/privata RSA personalizzata.</span><span class="sxs-lookup"><span data-stu-id="29891-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="29891-129">Si invierà la chiave pubblica a Microsoft, in cui Microsoft la inserirà in un certificato dell'applicazione Windows Media DRM firmato e lo restituirà.</span><span class="sxs-lookup"><span data-stu-id="29891-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="29891-130">Ogni payload, dopo essere stato decrittografato con la chiave di decrittografia RC4, deve essere immediatamente crittografato nel CPS di output.</span><span class="sxs-lookup"><span data-stu-id="29891-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="29891-131">Esistono altre restrizioni sulla gestione dei payload non crittografati descritti nelle regole di affidabilità e conformità, che accompagnano il contratto di esportazione di Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="29891-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29891-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29891-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29891-133">**Decrittografia e ricrittografia del payload ASF**</span><span class="sxs-lookup"><span data-stu-id="29891-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="29891-134">**Esportazione DRM**</span><span class="sxs-lookup"><span data-stu-id="29891-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="29891-135">**Esecuzione dell'individualizzazione DRM**</span><span class="sxs-lookup"><span data-stu-id="29891-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="29891-136">**Verifica e inizializzazione**</span><span class="sxs-lookup"><span data-stu-id="29891-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 




