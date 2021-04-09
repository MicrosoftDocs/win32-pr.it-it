---
description: Microsoft Windows fornisce alcune proprietà di sistema che è possibile utilizzare per i formati di file.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Proprietà di System-Defined per formati di file personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128518"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="bbf62-103">Proprietà di System-Defined per formati di file personalizzati</span><span class="sxs-lookup"><span data-stu-id="bbf62-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="bbf62-104">Microsoft Windows fornisce alcune proprietà di sistema che è possibile utilizzare per i formati di file.</span><span class="sxs-lookup"><span data-stu-id="bbf62-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="bbf62-105">Se si sta creando un formato di file personalizzato, è necessario supportare tutte le proprietà definite dal sistema come possibile.</span><span class="sxs-lookup"><span data-stu-id="bbf62-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="bbf62-106">Prima di creare un gestore di proprietà personalizzato, è consigliabile esaminare i gestori forniti dal sistema per verificare se è possibile utilizzarne uno anziché scriverne di propri.</span><span class="sxs-lookup"><span data-stu-id="bbf62-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="bbf62-107">La tabella seguente classifica i formati di file e quindi elenca le proprietà di sistema più importanti che il formato di file deve supportare.</span><span class="sxs-lookup"><span data-stu-id="bbf62-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="bbf62-108">Per garantire un'esperienza utente ottimale, è necessario supportare tutte le proprietà Priority 1 e 2 per la categoria del formato di file.</span><span class="sxs-lookup"><span data-stu-id="bbf62-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="bbf62-109">Comunicazioni</span><span class="sxs-lookup"><span data-stu-id="bbf62-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="bbf62-110">Contatti</span><span class="sxs-lookup"><span data-stu-id="bbf62-110">Contacts</span></span>](#contacts)
-   <span data-ttu-id="bbf62-111">[Documents](#documents) (Documenti)</span><span class="sxs-lookup"><span data-stu-id="bbf62-111">[Documents](#documents)</span></span>
-   [<span data-ttu-id="bbf62-112">Generico</span><span class="sxs-lookup"><span data-stu-id="bbf62-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="bbf62-113">Musica</span><span class="sxs-lookup"><span data-stu-id="bbf62-113">Music</span></span>](#music)
-   [<span data-ttu-id="bbf62-114">Immagini</span><span class="sxs-lookup"><span data-stu-id="bbf62-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="bbf62-115">Video</span><span class="sxs-lookup"><span data-stu-id="bbf62-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="bbf62-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbf62-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="bbf62-117">Comunicazioni</span><span class="sxs-lookup"><span data-stu-id="bbf62-117">Communications</span></span>



| <span data-ttu-id="bbf62-118">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-118">Name</span></span>            | <span data-ttu-id="bbf62-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-119">Property</span></span>                               | <span data-ttu-id="bbf62-120">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="bbf62-121">Data di ricezione</span><span class="sxs-lookup"><span data-stu-id="bbf62-121">Date received</span></span>   | <span data-ttu-id="bbf62-122">System. Message. DateReceived</span><span class="sxs-lookup"><span data-stu-id="bbf62-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="bbf62-123">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-123">1</span></span>        |
| <span data-ttu-id="bbf62-124">Da nomi</span><span class="sxs-lookup"><span data-stu-id="bbf62-124">From names</span></span>      | <span data-ttu-id="bbf62-125">System. Message. FromName</span><span class="sxs-lookup"><span data-stu-id="bbf62-125">System.Message.FromName</span></span>                | <span data-ttu-id="bbf62-126">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-126">1</span></span>        |
| <span data-ttu-id="bbf62-127">Con allegati</span><span class="sxs-lookup"><span data-stu-id="bbf62-127">Has attachments</span></span> | <span data-ttu-id="bbf62-128">System. Message. HasAttachments</span><span class="sxs-lookup"><span data-stu-id="bbf62-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="bbf62-129">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-129">1</span></span>        |
| <span data-ttu-id="bbf62-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="bbf62-130">Mailbox</span></span>         | <span data-ttu-id="bbf62-131">System. Communication. storeddisplayname</span><span class="sxs-lookup"><span data-stu-id="bbf62-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="bbf62-132">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-132">1</span></span>        |
| <span data-ttu-id="bbf62-133">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-133">Name</span></span>            | <span data-ttu-id="bbf62-134">System. FileName</span><span class="sxs-lookup"><span data-stu-id="bbf62-134">System.FileName</span></span>                        | <span data-ttu-id="bbf62-135">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-135">1</span></span>        |
| <span data-ttu-id="bbf62-136">Oggetto</span><span class="sxs-lookup"><span data-stu-id="bbf62-136">Subject</span></span>         | <span data-ttu-id="bbf62-137">System. Subject</span><span class="sxs-lookup"><span data-stu-id="bbf62-137">System.Subject</span></span>                         | <span data-ttu-id="bbf62-138">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-138">1</span></span>        |
| <span data-ttu-id="bbf62-139">Ai nomi</span><span class="sxs-lookup"><span data-stu-id="bbf62-139">To names</span></span>        | <span data-ttu-id="bbf62-140">System. Message. toName</span><span class="sxs-lookup"><span data-stu-id="bbf62-140">System.Message.ToName</span></span>                  | <span data-ttu-id="bbf62-141">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-141">1</span></span>        |
| <span data-ttu-id="bbf62-142">Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-142">Category</span></span>        | <span data-ttu-id="bbf62-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-143">System.Category</span></span>                        | <span data-ttu-id="bbf62-144">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-144">2</span></span>        |
| <span data-ttu-id="bbf62-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf62-145">Type</span></span>            | <span data-ttu-id="bbf62-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="bbf62-146">System.PerceivedType</span></span>                   | <span data-ttu-id="bbf62-147">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="bbf62-148">Contatti</span><span class="sxs-lookup"><span data-stu-id="bbf62-148">Contacts</span></span>



| <span data-ttu-id="bbf62-149">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-149">Name</span></span>             | <span data-ttu-id="bbf62-150">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-150">Property</span></span>                           | <span data-ttu-id="bbf62-151">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="bbf62-152">Nome account</span><span class="sxs-lookup"><span data-stu-id="bbf62-152">Account Name</span></span>     | <span data-ttu-id="bbf62-153">System. Communication. AccountName</span><span class="sxs-lookup"><span data-stu-id="bbf62-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="bbf62-154">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-154">1</span></span>        |
| <span data-ttu-id="bbf62-155">Telefono ufficio</span><span class="sxs-lookup"><span data-stu-id="bbf62-155">Business Phone</span></span>   | <span data-ttu-id="bbf62-156">System. Contact. BusinessTelephone</span><span class="sxs-lookup"><span data-stu-id="bbf62-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="bbf62-157">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-157">1</span></span>        |
| <span data-ttu-id="bbf62-158">Company</span><span class="sxs-lookup"><span data-stu-id="bbf62-158">Company</span></span>          | <span data-ttu-id="bbf62-159">System. Company</span><span class="sxs-lookup"><span data-stu-id="bbf62-159">System.Company</span></span>                     | <span data-ttu-id="bbf62-160">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-160">1</span></span>        |
| <span data-ttu-id="bbf62-161">Indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="bbf62-161">Email Address</span></span>    | <span data-ttu-id="bbf62-162">System. Contact. PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="bbf62-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="bbf62-163">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-163">1</span></span>        |
| <span data-ttu-id="bbf62-164">Importanza</span><span class="sxs-lookup"><span data-stu-id="bbf62-164">Importance</span></span>       | <span data-ttu-id="bbf62-165">System. ImportanceText</span><span class="sxs-lookup"><span data-stu-id="bbf62-165">System.ImportanceText</span></span>              | <span data-ttu-id="bbf62-166">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-166">1</span></span>        |
| <span data-ttu-id="bbf62-167">Cellulare</span><span class="sxs-lookup"><span data-stu-id="bbf62-167">Mobile Phone</span></span>     | <span data-ttu-id="bbf62-168">System. Contact. MobileTelephone</span><span class="sxs-lookup"><span data-stu-id="bbf62-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="bbf62-169">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-169">1</span></span>        |
| <span data-ttu-id="bbf62-170">Indirizzo aziendale</span><span class="sxs-lookup"><span data-stu-id="bbf62-170">Business address</span></span> | <span data-ttu-id="bbf62-171">System. Contact. BusinessAddress</span><span class="sxs-lookup"><span data-stu-id="bbf62-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="bbf62-172">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-172">2</span></span>        |
| <span data-ttu-id="bbf62-173">Fax aziendale</span><span class="sxs-lookup"><span data-stu-id="bbf62-173">Business fax</span></span>     | <span data-ttu-id="bbf62-174">System. Contact. BusinessFaxNumber</span><span class="sxs-lookup"><span data-stu-id="bbf62-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="bbf62-175">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-175">2</span></span>        |
| <span data-ttu-id="bbf62-176">Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-176">Category</span></span>         | <span data-ttu-id="bbf62-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-177">System.Category</span></span>                    | <span data-ttu-id="bbf62-178">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-178">2</span></span>        |
| <span data-ttu-id="bbf62-179">Indirizzo abitazione</span><span class="sxs-lookup"><span data-stu-id="bbf62-179">Home address</span></span>     | <span data-ttu-id="bbf62-180">System. Contact. HomeAddress</span><span class="sxs-lookup"><span data-stu-id="bbf62-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="bbf62-181">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-181">2</span></span>        |
| <span data-ttu-id="bbf62-182">Telefono abitazione</span><span class="sxs-lookup"><span data-stu-id="bbf62-182">Home phone</span></span>       | <span data-ttu-id="bbf62-183">System. Contact. HomeTelephone</span><span class="sxs-lookup"><span data-stu-id="bbf62-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="bbf62-184">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-184">2</span></span>        |
| <span data-ttu-id="bbf62-185">Titolo</span><span class="sxs-lookup"><span data-stu-id="bbf62-185">Title</span></span>            | <span data-ttu-id="bbf62-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="bbf62-186">System.Title</span></span>                       | <span data-ttu-id="bbf62-187">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="bbf62-188">Documenti</span><span class="sxs-lookup"><span data-stu-id="bbf62-188">Documents</span></span>



| <span data-ttu-id="bbf62-189">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-189">Name</span></span>      | <span data-ttu-id="bbf62-190">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-190">Property</span></span>             | <span data-ttu-id="bbf62-191">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="bbf62-192">Autori</span><span class="sxs-lookup"><span data-stu-id="bbf62-192">Authors</span></span>   | <span data-ttu-id="bbf62-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="bbf62-193">System.Author</span></span>        | <span data-ttu-id="bbf62-194">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-194">1</span></span>        |
| <span data-ttu-id="bbf62-195">Full-text</span><span class="sxs-lookup"><span data-stu-id="bbf62-195">Full Text</span></span> | <span data-ttu-id="bbf62-196">System. FullText</span><span class="sxs-lookup"><span data-stu-id="bbf62-196">System.FullText</span></span>      | <span data-ttu-id="bbf62-197">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-197">1</span></span>        |
| <span data-ttu-id="bbf62-198">Tag</span><span class="sxs-lookup"><span data-stu-id="bbf62-198">Tags</span></span>      | <span data-ttu-id="bbf62-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="bbf62-199">System.Keywords</span></span>      | <span data-ttu-id="bbf62-200">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-200">1</span></span>        |
| <span data-ttu-id="bbf62-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf62-201">Type</span></span>      | <span data-ttu-id="bbf62-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="bbf62-202">System.PerceivedType</span></span> | <span data-ttu-id="bbf62-203">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-203">1</span></span>        |
| <span data-ttu-id="bbf62-204">Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-204">Category</span></span>  | <span data-ttu-id="bbf62-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-205">System.Category</span></span>      | <span data-ttu-id="bbf62-206">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-206">2</span></span>        |
| <span data-ttu-id="bbf62-207">Titolo</span><span class="sxs-lookup"><span data-stu-id="bbf62-207">Title</span></span>     | <span data-ttu-id="bbf62-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="bbf62-208">System.Title</span></span>         | <span data-ttu-id="bbf62-209">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="bbf62-210">Generico</span><span class="sxs-lookup"><span data-stu-id="bbf62-210">Generic</span></span>



| <span data-ttu-id="bbf62-211">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-211">Name</span></span>     | <span data-ttu-id="bbf62-212">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-212">Property</span></span>             | <span data-ttu-id="bbf62-213">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="bbf62-214">Autori</span><span class="sxs-lookup"><span data-stu-id="bbf62-214">Authors</span></span>  | <span data-ttu-id="bbf62-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="bbf62-215">System.Author</span></span>        | <span data-ttu-id="bbf62-216">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-216">1</span></span>        |
| <span data-ttu-id="bbf62-217">Titolo</span><span class="sxs-lookup"><span data-stu-id="bbf62-217">Title</span></span>    | <span data-ttu-id="bbf62-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="bbf62-218">System.Title</span></span>         | <span data-ttu-id="bbf62-219">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-219">1</span></span>        |
| <span data-ttu-id="bbf62-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf62-220">Type</span></span>     | <span data-ttu-id="bbf62-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="bbf62-221">System.PerceivedType</span></span> | <span data-ttu-id="bbf62-222">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-222">1</span></span>        |
| <span data-ttu-id="bbf62-223">Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-223">Category</span></span> | <span data-ttu-id="bbf62-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="bbf62-224">System.Category</span></span>      | <span data-ttu-id="bbf62-225">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-225">2</span></span>        |
| <span data-ttu-id="bbf62-226">Tag</span><span class="sxs-lookup"><span data-stu-id="bbf62-226">Tags</span></span>     | <span data-ttu-id="bbf62-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="bbf62-227">System.Keywords</span></span>      | <span data-ttu-id="bbf62-228">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="bbf62-229">Musica</span><span class="sxs-lookup"><span data-stu-id="bbf62-229">Music</span></span>



| <span data-ttu-id="bbf62-230">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-230">Name</span></span>         | <span data-ttu-id="bbf62-231">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-231">Property</span></span>                     | <span data-ttu-id="bbf62-232">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="bbf62-233">System. Music. numero</span><span class="sxs-lookup"><span data-stu-id="bbf62-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="bbf62-234">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-234">1</span></span>        |
| <span data-ttu-id="bbf62-235">Album</span><span class="sxs-lookup"><span data-stu-id="bbf62-235">Album</span></span>        | <span data-ttu-id="bbf62-236">System. Music. AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="bbf62-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="bbf62-237">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-237">1</span></span>        |
| <span data-ttu-id="bbf62-238">Gli artisti</span><span class="sxs-lookup"><span data-stu-id="bbf62-238">Artists</span></span>      | <span data-ttu-id="bbf62-239">System. Music. Artist</span><span class="sxs-lookup"><span data-stu-id="bbf62-239">System.Music.Artist</span></span>          | <span data-ttu-id="bbf62-240">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-240">1</span></span>        |
| <span data-ttu-id="bbf62-241">Genre</span><span class="sxs-lookup"><span data-stu-id="bbf62-241">Genre</span></span>        | <span data-ttu-id="bbf62-242">System. Music. Genre</span><span class="sxs-lookup"><span data-stu-id="bbf62-242">System.Music.Genre</span></span>           | <span data-ttu-id="bbf62-243">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-243">1</span></span>        |
| <span data-ttu-id="bbf62-244">Classificazione</span><span class="sxs-lookup"><span data-stu-id="bbf62-244">Rating</span></span>       | <span data-ttu-id="bbf62-245">System. rating</span><span class="sxs-lookup"><span data-stu-id="bbf62-245">System.Rating</span></span>                | <span data-ttu-id="bbf62-246">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-246">1</span></span>        |
| <span data-ttu-id="bbf62-247">Titolo</span><span class="sxs-lookup"><span data-stu-id="bbf62-247">Title</span></span>        | <span data-ttu-id="bbf62-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="bbf62-248">System.Title</span></span>                 | <span data-ttu-id="bbf62-249">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-249">1</span></span>        |
| <span data-ttu-id="bbf62-250">Artista album</span><span class="sxs-lookup"><span data-stu-id="bbf62-250">Album Artist</span></span> | <span data-ttu-id="bbf62-251">System. Music. AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="bbf62-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="bbf62-252">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-252">2</span></span>        |
| <span data-ttu-id="bbf62-253">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="bbf62-253">Bit Rate</span></span>     | <span data-ttu-id="bbf62-254">System. audio. EncodingBitrate</span><span class="sxs-lookup"><span data-stu-id="bbf62-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="bbf62-255">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-255">2</span></span>        |
| <span data-ttu-id="bbf62-256">Conduttori</span><span class="sxs-lookup"><span data-stu-id="bbf62-256">Conductors</span></span>   | <span data-ttu-id="bbf62-257">System. Music. Conductor</span><span class="sxs-lookup"><span data-stu-id="bbf62-257">System.Music.Conductor</span></span>       | <span data-ttu-id="bbf62-258">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-258">2</span></span>        |
| <span data-ttu-id="bbf62-259">Length</span><span class="sxs-lookup"><span data-stu-id="bbf62-259">Length</span></span>       | <span data-ttu-id="bbf62-260">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="bbf62-260">System.Media.Duration</span></span>        | <span data-ttu-id="bbf62-261">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-261">2</span></span>        |
| <span data-ttu-id="bbf62-262">Protetta</span><span class="sxs-lookup"><span data-stu-id="bbf62-262">Protected</span></span>    | <span data-ttu-id="bbf62-263">System. DRM. protected</span><span class="sxs-lookup"><span data-stu-id="bbf62-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="bbf62-264">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-264">2</span></span>        |
| <span data-ttu-id="bbf62-265">Year</span><span class="sxs-lookup"><span data-stu-id="bbf62-265">Year</span></span>         | <span data-ttu-id="bbf62-266">System. Media. Year</span><span class="sxs-lookup"><span data-stu-id="bbf62-266">System.Media.Year</span></span>            | <span data-ttu-id="bbf62-267">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="bbf62-268">Immagini</span><span class="sxs-lookup"><span data-stu-id="bbf62-268">Pictures</span></span>



| <span data-ttu-id="bbf62-269">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-269">Name</span></span>          | <span data-ttu-id="bbf62-270">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-270">Property</span></span>                        | <span data-ttu-id="bbf62-271">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="bbf62-272">Data importazione</span><span class="sxs-lookup"><span data-stu-id="bbf62-272">Date imported</span></span> | <span data-ttu-id="bbf62-273">System. DateImported</span><span class="sxs-lookup"><span data-stu-id="bbf62-273">System.DateImported</span></span>             | <span data-ttu-id="bbf62-274">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-274">1</span></span>        |
| <span data-ttu-id="bbf62-275">Data di inizio</span><span class="sxs-lookup"><span data-stu-id="bbf62-275">Date Taken</span></span>    | <span data-ttu-id="bbf62-276">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="bbf62-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="bbf62-277">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-277">1</span></span>        |
| <span data-ttu-id="bbf62-278">Classificazione</span><span class="sxs-lookup"><span data-stu-id="bbf62-278">Rating</span></span>        | <span data-ttu-id="bbf62-279">System. rating</span><span class="sxs-lookup"><span data-stu-id="bbf62-279">System.Rating</span></span>                   | <span data-ttu-id="bbf62-280">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-280">1</span></span>        |
| <span data-ttu-id="bbf62-281">Tag</span><span class="sxs-lookup"><span data-stu-id="bbf62-281">Tags</span></span>          | <span data-ttu-id="bbf62-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="bbf62-282">System.Keywords</span></span>                 | <span data-ttu-id="bbf62-283">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-283">1</span></span>        |
| <span data-ttu-id="bbf62-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf62-284">Type</span></span>          | <span data-ttu-id="bbf62-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="bbf62-285">System.PerceivedType</span></span>            | <span data-ttu-id="bbf62-286">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-286">1</span></span>        |
| <span data-ttu-id="bbf62-287">Autori</span><span class="sxs-lookup"><span data-stu-id="bbf62-287">Authors</span></span>       | <span data-ttu-id="bbf62-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="bbf62-288">System.Author</span></span>                   | <span data-ttu-id="bbf62-289">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-289">2</span></span>        |
| <span data-ttu-id="bbf62-290">Produttore di fotocamere</span><span class="sxs-lookup"><span data-stu-id="bbf62-290">Camera maker</span></span>  | <span data-ttu-id="bbf62-291">System. Photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="bbf62-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="bbf62-292">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-292">2</span></span>        |
| <span data-ttu-id="bbf62-293">Modello di fotocamera</span><span class="sxs-lookup"><span data-stu-id="bbf62-293">Camera model</span></span>  | <span data-ttu-id="bbf62-294">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="bbf62-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="bbf62-295">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-295">2</span></span>        |
| <span data-ttu-id="bbf62-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="bbf62-296">Comments</span></span>      | <span data-ttu-id="bbf62-297">System. Comment</span><span class="sxs-lookup"><span data-stu-id="bbf62-297">System.Comment</span></span>                  | <span data-ttu-id="bbf62-298">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-298">2</span></span>        |
| <span data-ttu-id="bbf62-299">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="bbf62-299">Dimensions</span></span>    | <span data-ttu-id="bbf62-300">System. image. Dimensions</span><span class="sxs-lookup"><span data-stu-id="bbf62-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="bbf62-301">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="bbf62-302">Video</span><span class="sxs-lookup"><span data-stu-id="bbf62-302">Videos</span></span>



| <span data-ttu-id="bbf62-303">Nome</span><span class="sxs-lookup"><span data-stu-id="bbf62-303">Name</span></span>         | <span data-ttu-id="bbf62-304">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-304">Property</span></span>                 | <span data-ttu-id="bbf62-305">Priorità</span><span class="sxs-lookup"><span data-stu-id="bbf62-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="bbf62-306">Length</span><span class="sxs-lookup"><span data-stu-id="bbf62-306">Length</span></span>       | <span data-ttu-id="bbf62-307">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="bbf62-307">System.Media.Duration</span></span>    | <span data-ttu-id="bbf62-308">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-308">1</span></span>        |
| <span data-ttu-id="bbf62-309">Classificazione</span><span class="sxs-lookup"><span data-stu-id="bbf62-309">Rating</span></span>       | <span data-ttu-id="bbf62-310">System. rating</span><span class="sxs-lookup"><span data-stu-id="bbf62-310">System.Rating</span></span>            | <span data-ttu-id="bbf62-311">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-311">1</span></span>        |
| <span data-ttu-id="bbf62-312">Tag</span><span class="sxs-lookup"><span data-stu-id="bbf62-312">Tags</span></span>         | <span data-ttu-id="bbf62-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="bbf62-313">System.Keywords</span></span>          | <span data-ttu-id="bbf62-314">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-314">1</span></span>        |
| <span data-ttu-id="bbf62-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf62-315">Type</span></span>         | <span data-ttu-id="bbf62-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="bbf62-316">System.PerceivedType</span></span>     | <span data-ttu-id="bbf62-317">1</span><span class="sxs-lookup"><span data-stu-id="bbf62-317">1</span></span>        |
| <span data-ttu-id="bbf62-318">Altezza frame</span><span class="sxs-lookup"><span data-stu-id="bbf62-318">Frame height</span></span> | <span data-ttu-id="bbf62-319">System. video. FrameHeight</span><span class="sxs-lookup"><span data-stu-id="bbf62-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="bbf62-320">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-320">2</span></span>        |
| <span data-ttu-id="bbf62-321">Larghezza frame</span><span class="sxs-lookup"><span data-stu-id="bbf62-321">Frame width</span></span>  | <span data-ttu-id="bbf62-322">System. video. FrameWidth</span><span class="sxs-lookup"><span data-stu-id="bbf62-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="bbf62-323">2</span><span class="sxs-lookup"><span data-stu-id="bbf62-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bbf62-324">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbf62-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bbf62-325">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="bbf62-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf62-326">Sviluppo di gestori di proprietà per Windows Search</span><span class="sxs-lookup"><span data-stu-id="bbf62-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="bbf62-327">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="bbf62-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf62-328">Sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="bbf62-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="bbf62-329">[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="bbf62-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
