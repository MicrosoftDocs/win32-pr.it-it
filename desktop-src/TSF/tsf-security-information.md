---
title: Considerazioni sulla sicurezza Framework servizi di testo
description: Considerazioni sulla sicurezza Framework servizi di testo
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Framework servizi di testo (TSF), sicurezza
- TSF (Framework di servizi di testo), sicurezza
- Servizi di testo, sicurezza
- Applicazioni abilitate per TSF, sicurezza
- sicurezza per TSF
- Framework servizi di testo (TSF), procedure consigliate
- TSF (Framework di servizi di testo), procedure consigliate
- Applicazioni abilitate per TSF, procedure consigliate
- Servizi di testo, procedure consigliate
- procedure consigliate per TSF
- Framework servizi di testo (TSF), controllo degli errori
- TSF (Framework dei servizi di testo), controllo degli errori
- Applicazioni abilitate per TSF, controllo degli errori
- Servizi di testo, controllo degli errori
- controllo degli errori
- Framework servizi di testo (TSF), firme digitali
- TSF (Text Services Framework), firme digitali
- Servizi di testo, firme digitali
- Applicazioni abilitate per TSF, firme digitali
- firme digitali
- Framework servizi di testo (TSF), chiamate LoadLibrary
- TSF (Framework di servizi di testo), chiamate LoadLibrary
- Servizi di testo, chiamate LoadLibrary
- Applicazioni abilitate per TSF, chiamate LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299866"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="2a3f8-127">Considerazioni sulla sicurezza: Framework dei servizi di testo</span><span class="sxs-lookup"><span data-stu-id="2a3f8-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="2a3f8-128">Procedure consigliate per lo sviluppo con TSF</span><span class="sxs-lookup"><span data-stu-id="2a3f8-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="2a3f8-129">**Firme digitali:** I provider di servizi di testo devono fornire firme digitali con i rispettivi file eseguibili binari.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="2a3f8-130">Un servizio di testo registrato può accedere ai thread di sistema e potrebbe esporre informazioni che altrimenti non sarebbero accessibili.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="2a3f8-131">Per garantire un'operazione stabile e sicura, l'utente deve verificare la firma digitale di un servizio di testo prima che il servizio di testo possa essere caricato.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="2a3f8-132">Per la procedura appropriata per la creazione di una firma digitale, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2a3f8-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="2a3f8-133">**Controllo errori:** Ogni metodo o chiamata di funzione deve essere verificata in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="2a3f8-134">In caso di errore, le chiamate al metodo o alla funzione rimanenti devono essere ignorate.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="2a3f8-135">La maggior parte degli esempi di codice in questa documentazione ha un controllo degli errori limitato o nessuno, per evitare di nascondere il punto da illustrare.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="2a3f8-136">Non è consigliabile incollare esempi dalla documentazione direttamente nel codice di produzione; è invece consigliabile migliorare gli esempi aggiungendo il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="2a3f8-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="2a3f8-137">**Chiamate LoadLibrary:** Per ottenere un puntatore a una qualsiasi delle [funzioni TSF](text-services-framework-functions.md), è necessario usare [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="2a3f8-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="2a3f8-138">Tuttavia, è importante attenersi alle procedure per formattare il nome del percorso della DLL, come indicato nella documentazione di **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="2a3f8-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a3f8-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a3f8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a3f8-140">Procedure di sicurezza consigliate</span><span class="sxs-lookup"><span data-stu-id="2a3f8-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="2a3f8-141">[Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a3f8-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2a3f8-142">Funzioni TSF</span><span class="sxs-lookup"><span data-stu-id="2a3f8-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="2a3f8-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="2a3f8-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="2a3f8-144">GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="2a3f8-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 