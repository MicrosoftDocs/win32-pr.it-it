---
title: File di libreria, file di intestazione e impostazioni del compilatore
description: File di libreria, file di intestazione e impostazioni del compilatore
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media Format SDK, file di libreria DRM
- Windows Media Format SDK, file di libreria
- Windows Media Format SDK, file di intestazione DRM
- Windows Media Format SDK, file di intestazione
- Windows Media Format SDK, impostazioni del compilatore DRM
- Windows Media Format SDK, impostazioni del compilatore
- Digital Rights Management (DRM), file di libreria
- DRM (Digital Rights Management), file di libreria
- Digital Rights Management (DRM), file di intestazione
- DRM (Digital Rights Management), file di intestazione
- Digital Rights Management (DRM), impostazioni del compilatore
- DRM (Digital Rights Management), impostazioni del compilatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116856"
---
# <a name="library-files-header-files-and-compiler-settings"></a><span data-ttu-id="4b3b9-115">File di libreria, file di intestazione e impostazioni del compilatore</span><span class="sxs-lookup"><span data-stu-id="4b3b9-115">Library Files, Header Files, and Compiler Settings</span></span>

<span data-ttu-id="4b3b9-116">I componenti di programmazione delle API estese del client Windows Media DRM sono definiti nel file di intestazione wmdrmsdk. h e sono implementati nelle librerie wmdrmsdk. lib e mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-116">The programming components of the Windows Media DRM Client Extended APIs are defined in the wmdrmsdk.h header file, and implemented in the wmdrmsdk.lib and mfuuid.lib libraries.</span></span>

<span data-ttu-id="4b3b9-117">Per alcune delle funzionalità delle API estese del client Windows Media DRM è necessario ottenere una libreria protetta da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-117">Some of the functionality of the Windows Media DRM Client Extended APIs requires that you obtain a protected library from Microsoft.</span></span> <span data-ttu-id="4b3b9-118">Questa libreria, denominata libreria stub in questa documentazione, è specifica del destinatario e specifica il livello di sicurezza dell'applicazione per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-118">This library, called the stub library in this documentation, is specific to the recipient and specifies the application security level for your applications.</span></span> <span data-ttu-id="4b3b9-119">La libreria stub sostituisce wmdrmsdk. lib; non è mai necessario collegarsi a entrambi.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-119">The stub library replaces wmdrmsdk.lib; you should never link to both.</span></span>

<span data-ttu-id="4b3b9-120">**Nota** La libreria stub DRM è separata dalla libreria stub utilizzata dal resto di Windows Media Format SDK, ma è concessa in licenza con lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-120">**Note** The DRM stub library is separate from the stub library used by the rest of the Windows Media Format SDK but is licensed using the same method.</span></span>

<span data-ttu-id="4b3b9-121">**Nota** La libreria stub DRM deve essere collegata all'applicazione dopo il file di libreria MSVCRT. lib per evitare errori del linker.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-121">**Note** The DRM stub library must be linked into your application after the library file msvcrt.lib to avoid linker errors.</span></span>

<span data-ttu-id="4b3b9-122">La libreria stub contiene un certificato incorporato che può essere revocato da Microsoft se non si rispettano i termini e le condizioni del contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-122">The stub library contains an embedded certificate which can be revoked by Microsoft if you fail to comply with the terms and conditions of the license agreement.</span></span>

<span data-ttu-id="4b3b9-123">I metodi specifici che richiedono la libreria stub sono contrassegnati nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-123">Specific methods that require the stub library are labeled in the documentation.</span></span> <span data-ttu-id="4b3b9-124">Se si tenta di usare un metodo di questo tipo senza collegarsi alla libreria stub, verrà restituito un \_ errore STUBLIB di NS E \_ DRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4b3b9-124">If you try to use such a method without linking to the stub library, it will return an NS\_E\_DRM\_STUBLIB\_REQUIRED error.</span></span>

<span data-ttu-id="4b3b9-125">Non è possibile usare il sottosistema DRM in una compilazione di debug.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-125">The DRM subsystem can not be used in a debug build.</span></span> <span data-ttu-id="4b3b9-126">Se si tenta di eseguire questa operazione, i metodi dell'API restituiranno l'errore di debug di NS \_ E \_ DRM \_ \_ non \_ consentito.</span><span class="sxs-lookup"><span data-stu-id="4b3b9-126">If this is attempted, methods of the API will return the NS\_E\_DRM\_DEBUGGING\_NOT\_ALLOWED error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b3b9-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4b3b9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b3b9-128">**Per iniziare**</span><span class="sxs-lookup"><span data-stu-id="4b3b9-128">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="4b3b9-129">**File di libreria e impostazioni del compilatore**</span><span class="sxs-lookup"><span data-stu-id="4b3b9-129">**Library Files and Compiler Settings**</span></span>](library-files-and-compiler-settings.md)
</dt> <dt>

[<span data-ttu-id="4b3b9-130">**Ottenere la libreria DRM necessaria**</span><span class="sxs-lookup"><span data-stu-id="4b3b9-130">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




