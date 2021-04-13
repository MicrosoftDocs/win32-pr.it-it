---
title: Backup e ripristino di licenze DRM
description: Backup e ripristino di licenze DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK, backup di licenze DRM
- Windows Media Format SDK, ripristino di licenze DRM
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Windows Media Format SDK, funzionalità di ripristino di backup
- Windows Media Format SDK, servizio di gestione delle licenze
- Windows Media Format SDK, rilevamento di frodi
- Digital Rights Management (DRM), backup delle licenze
- DRM (Digital Rights Management), backup delle licenze
- Digital Rights Management (DRM), ripristino di licenze
- DRM (Digital Rights Management), ripristino di licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), funzionalità di ripristino del backup
- DRM (Digital Rights Management), funzionalità di ripristino del backup
- Digital Rights Management (DRM), servizio gestione licenze
- DRM (Digital Rights Management), servizio di gestione delle licenze
- Digital Rights Management (DRM), rilevamento di frodi
- DRM (Digital Rights Management), rilevamento di frodi
- backup di licenze DRM
- ripristino di licenze DRM
- licenze, DRM
- licenze, backup di DRM
- licenze, ripristino di DRM
- Funzionalità Ripristino backup
- Servizio gestione licenze
- rilevamento di frodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104339495"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="1c79f-130">Backup e ripristino di licenze DRM</span><span class="sxs-lookup"><span data-stu-id="1c79f-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="1c79f-131">Con la funzionalità di ripristino del backup, gli utenti possono eseguire il backup e il ripristino delle [*licenze*](wmformat-glossary.md) nello stesso computer o in altri computer.</span><span class="sxs-lookup"><span data-stu-id="1c79f-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="1c79f-132">Questa funzionalità consente agli utenti di trasferire le licenze in un nuovo computer o di nuovo nello stesso computer, ad esempio dopo aver riformattato il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="1c79f-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="1c79f-133">Inoltre, gli utenti possono riprodurre file ASF protetti in più di un computer.</span><span class="sxs-lookup"><span data-stu-id="1c79f-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="1c79f-134">Per incoraggiare l'utilizzo legittimo di una licenza, i criteri di rilevamento delle frodi limitano il numero di volte che è possibile ripristinare una licenza.</span><span class="sxs-lookup"><span data-stu-id="1c79f-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="1c79f-135">Microsoft fornisce un servizio che tiene traccia del numero di computer a cui è stata ripristinata una licenza; Se viene raggiunto un limite, l'utente non potrà ripristinare la licenza.</span><span class="sxs-lookup"><span data-stu-id="1c79f-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="1c79f-136">Consentire o impedire il diritto di eseguire il backup e il ripristino</span><span class="sxs-lookup"><span data-stu-id="1c79f-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="1c79f-137">La funzionalità di ripristino del backup funziona solo per le licenze per le quali viene assegnato il diritto di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="1c79f-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="1c79f-138">Se i proprietari del contenuto o le autorità emittenti di licenze non desiderano questa funzionalità o se emettono licenze che contengono uno stato sicuro (ad esempio, operazioni conteggiate o tempo limitato), possono impedire questo diritto.</span><span class="sxs-lookup"><span data-stu-id="1c79f-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="1c79f-139">Quando non è possibile ripristinare una licenza perché un utente non dispone del diritto, all'applicazione viene passato un [*ID chiave*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="1c79f-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="1c79f-140">Come minimo, l'utente deve ricevere una notifica che non è stato possibile eseguire il backup di alcune licenze, anche se l'utente non è in grado di stabilire a quali licenze si riferisce questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="1c79f-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="1c79f-141">Se si conosce l'ID chiave per i file protetti disponibili, è possibile sviluppare una soluzione più affidabile per informare l'utente.</span><span class="sxs-lookup"><span data-stu-id="1c79f-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="1c79f-142">Ad esempio, un giocatore può essere sviluppato per un'etichetta di record che fornisce canzoni protette su Internet.</span><span class="sxs-lookup"><span data-stu-id="1c79f-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="1c79f-143">È possibile tenere traccia di questi brani e dei relativi ID chiave in un database.</span><span class="sxs-lookup"><span data-stu-id="1c79f-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="1c79f-144">Se non è stato possibile eseguire il backup di alcune licenze, l'applicazione lettore può usare l'ID chiave per eseguire una query sul database per il nome dei brani, quindi informare l'utente per quali brani non è possibile eseguire il backup delle licenze.</span><span class="sxs-lookup"><span data-stu-id="1c79f-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="1c79f-145">In alternativa, è possibile creare una raccolta musicale per ogni utente localmente e l'ID chiave può essere usato per recuperare altre informazioni sulle licenze di cui non è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="1c79f-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="1c79f-146">Il servizio gestione licenze</span><span class="sxs-lookup"><span data-stu-id="1c79f-146">The License Management Service</span></span>

<span data-ttu-id="1c79f-147">Quando viene implementata la funzionalità di ripristino del backup, un servizio di gestione delle licenze ospitato da Microsoft gestisce il ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="1c79f-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="1c79f-148">In primo luogo, gli utenti eseguono il backup delle licenze nell'applicazione, ad esempio scegliendo un'opzione di menu.</span><span class="sxs-lookup"><span data-stu-id="1c79f-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="1c79f-149">Viene eseguito il backup di tutte le licenze del computer in un percorso specifico, ad esempio un disco floppy.</span><span class="sxs-lookup"><span data-stu-id="1c79f-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="1c79f-150">Quindi, gli utenti ripristinano le licenze utilizzando l'applicazione, ad esempio scegliendo un'opzione di menu e specificando il percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="1c79f-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="1c79f-151">A questo punto, l'utente deve essere connesso a Internet. una richiesta dell'applicazione viene inviata al servizio di gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="1c79f-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="1c79f-152">Se il computer da cui è stato eseguito il backup della licenza è diverso dal computer originale (oppure il computer originale è stato riformattato), il servizio di gestione delle licenze rilascia una nuova licenza per il nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="1c79f-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="1c79f-153">In caso contrario, la licenza che è stata rilasciata in precedenza a tale computer viene rilasciata.</span><span class="sxs-lookup"><span data-stu-id="1c79f-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="1c79f-154">Poiché il servizio gestione licenze recupera le informazioni dall'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel [sito Web Microsoft](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="1c79f-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="1c79f-155">Quando un utente finale ripristina una licenza in un computer diverso e la licenza richiede l'individualizzazione, l'utente finale deve autorizzare i componenti DRM da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1c79f-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="1c79f-156">Per supportare questa funzionalità, è necessario implementare un processo nell'applicazione del lettore.</span><span class="sxs-lookup"><span data-stu-id="1c79f-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="1c79f-157">Rilevamento di illeciti</span><span class="sxs-lookup"><span data-stu-id="1c79f-157">Detecting Fraud</span></span>

<span data-ttu-id="1c79f-158">L'utente è autorizzato a ripristinare una licenza per un numero limitato di volte.</span><span class="sxs-lookup"><span data-stu-id="1c79f-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="1c79f-159">Ogni volta che viene ripristinata una licenza, il servizio di gestione delle licenze lo tiene traccia e incrementa il conteggio di una licenza.</span><span class="sxs-lookup"><span data-stu-id="1c79f-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="1c79f-160">Quando si ripristina una licenza in un computer in cui la licenza è stata ripristinata in precedenza (ad esempio, il computer da cui è stato eseguito il backup della licenza), il conteggio non viene aumentato.</span><span class="sxs-lookup"><span data-stu-id="1c79f-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="1c79f-161">Un computer viene considerato diverso se dispone di un nuovo sistema operativo o se il sistema operativo è stato reinstallato.</span><span class="sxs-lookup"><span data-stu-id="1c79f-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="1c79f-162">In conformità ai criteri di rilevamento delle frodi di Microsoft, quando una licenza è stata ripristinata un determinato numero di volte, l'applicazione riceve un URL dai componenti DRM ed è responsabile dell'apertura di un browser e della visualizzazione della pagina Web, che indica che il contratto di licenza potrebbe essere stato violato.</span><span class="sxs-lookup"><span data-stu-id="1c79f-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="1c79f-163">L'utente deve contattare il distributore di licenze, che deve stabilire se la richiesta è valida.</span><span class="sxs-lookup"><span data-stu-id="1c79f-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="1c79f-164">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="1c79f-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1c79f-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c79f-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c79f-166">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="1c79f-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1c79f-167">**Backup e ripristino di licenze**</span><span class="sxs-lookup"><span data-stu-id="1c79f-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




