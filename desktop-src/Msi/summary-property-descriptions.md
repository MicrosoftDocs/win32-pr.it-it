---
description: Le proprietà di riepilogo per i pacchetti di installazione, le trasformazioni e le patch sono descritte nelle tabelle seguenti.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descrizioni delle proprietà di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318276"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="e0cda-103">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="e0cda-103">Summary Property Descriptions</span></span>

<span data-ttu-id="e0cda-104">Le proprietà di riepilogo per i pacchetti di installazione, le trasformazioni e le patch sono descritte nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0cda-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="e0cda-105">Si noti che il significato di una particolare proprietà di riepilogo può variare a seconda che il database appartenga a un pacchetto di installazione, una trasformazione o un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="e0cda-106">Per ulteriori informazioni sugli ID, i PID e i tipi di proprietà, vedere [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="e0cda-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="e0cda-107">Pacchetti di installazione</span><span class="sxs-lookup"><span data-stu-id="e0cda-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0cda-108">Proprietà Summary</span><span class="sxs-lookup"><span data-stu-id="e0cda-108">Summary property</span></span></th>
<th><span data-ttu-id="e0cda-109">Significato di questa proprietà in un database di installazione</span><span class="sxs-lookup"><span data-stu-id="e0cda-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0cda-110"><a href="title-summary.md"><strong>Titolo</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-111">Descrizione del file come pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-111">A description of this file as an installation package.</span></span> <span data-ttu-id="e0cda-112">La descrizione deve includere la frase &quot; <a href="about-the-installer-database.md">database di installazione</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="e0cda-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-113"><a href="subject-summary.md"><strong>Oggetto</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-114">Nome del prodotto installato da questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e0cda-114">The name of the product installed by this package.</span></span> <span data-ttu-id="e0cda-115">Deve corrispondere al nome della proprietà <a href="productname.md"><strong>ProductName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e0cda-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-116"><a href="author-summary.md"><strong>Autore</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-117">Nome del produttore di questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="e0cda-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="e0cda-118">Deve corrispondere al nome della proprietà del <a href="manufacturer.md"><strong>produttore</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e0cda-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-119"><a href="keywords-summary.md"><strong>Parole chiave</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-120">Un elenco di parole chiave che possono essere usate dai browser di file per cercare un file.</span><span class="sxs-lookup"><span data-stu-id="e0cda-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="e0cda-121">Le parole chiave devono includere il &quot; programma &quot; di installazione e le parole chiave specifiche del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e0cda-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-122"><a href="comments-summary.md"><strong>Commenti</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-123">Contiene la frase: il &quot; database del programma di installazione contiene la logica e i dati necessari per installare <<em>nome del prodotto</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="e0cda-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-124"><a href="template-summary.md"><strong>Modello</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-125">Piattaforma e linguaggi compatibili con questo pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="e0cda-126">Per la sintassi, vedere il <a href="template-summary.md"><strong>modello</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e0cda-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-127"><a href="last-saved-by-summary.md"><strong>Autore ultimo salvataggio</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-128">Gli sviluppatori di strumenti di modifica del database possono utilizzare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="e0cda-129">Questa proprietà deve essere impostata su null in un database di spedizione finale.</span><span class="sxs-lookup"><span data-stu-id="e0cda-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="e0cda-130">Il programma di installazione imposta questa proprietà sul valore della proprietà <a href="logonuser.md"><strong>LogonUser</strong></a> durante un' <a href="administrative-installation.md"><strong>installazione amministrativa</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e0cda-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="e0cda-131">Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla.</span><span class="sxs-lookup"><span data-stu-id="e0cda-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-132"><a href="revision-number-summary.md"><strong>Numero revisione</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-133">Contiene il <a href="package-codes.md">codice del pacchetto</a> del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-134"><a href="last-printed-summary.md"><strong>Ultima stampa</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-135">Può essere impostato sulla data e sull'ora durante un' <a href="administrative-installation.md">installazione amministrativa</a> per registrare il momento in cui è stata creata l'immagine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="e0cda-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-136"><a href="create-time-date-summary.md"><strong>Data/ora creazione</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-137">Data e ora in cui è stato creato il database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-138"><a href="last-saved-time-date-summary.md"><strong>Data/ora ultimo salvataggio</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-139">Data e ora di sistema correnti al momento dell'ultimo salvataggio del database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="e0cda-140">Inizialmente null.</span><span class="sxs-lookup"><span data-stu-id="e0cda-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-141"><a href="page-count-summary.md"><strong>Conteggio pagine</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-142">Contiene un valore utilizzato per identificare la versione minima del programma di installazione richiesta dal pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="e0cda-143">Se, ad esempio, il pacchetto richiede almeno la versione 2,0 del programma di installazione, questa proprietà deve essere impostata su un numero intero pari a 200.</span><span class="sxs-lookup"><span data-stu-id="e0cda-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0cda-144">Il valore di questa proprietà deve essere 200 o superiore con i <a href="64-bit-windows-installer-packages.md">pacchetti Windows Installer a 64 bit</a>.</span><span class="sxs-lookup"><span data-stu-id="e0cda-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-145"><a href="word-count-summary.md"><strong>Conteggio parole</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-146">Tipo di immagine del file di origine.</span><span class="sxs-lookup"><span data-stu-id="e0cda-146">The type of the source file image.</span></span> <span data-ttu-id="e0cda-147">Archiviato al posto della proprietà Count standard.</span><span class="sxs-lookup"><span data-stu-id="e0cda-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="e0cda-148">Questa proprietà è un campo di bit.</span><span class="sxs-lookup"><span data-stu-id="e0cda-148">This property is a bit field.</span></span> <span data-ttu-id="e0cda-149">Vedere l'argomento relativo al <a href="word-count-summary.md"><strong>conteggio delle parole</strong></a> per i valori.</span><span class="sxs-lookup"><span data-stu-id="e0cda-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="e0cda-150">A partire da Windows Installer versione 4,0 in Windows Vista, questa proprietà include BITS per specificare se sono necessari privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="e0cda-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-151"><a href="character-count-summary.md"><strong>Numero di caratteri</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-152">Null</span><span class="sxs-lookup"><span data-stu-id="e0cda-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-153"><a href="creating-application-summary.md"><strong>Creazione dell'applicazione</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-154">Contiene il nome del software utilizzato per creare il database di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-155"><a href="security-summary.md"><strong>Sicurezza</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-156">Il valore di questa proprietà deve essere di sola lettura consigliato.</span><span class="sxs-lookup"><span data-stu-id="e0cda-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-157"><a href="codepage-summary.md"><strong>CodePage</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-158">Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e0cda-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="e0cda-159">Questa proprietà deve essere impostata prima di impostare le proprietà di stringa nelle informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e0cda-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="e0cda-160">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="e0cda-160">Transforms</span></span>



| <span data-ttu-id="e0cda-161">Proprietà Summary</span><span class="sxs-lookup"><span data-stu-id="e0cda-161">Summary property</span></span>                                              | <span data-ttu-id="e0cda-162">Significato di questa proprietà in una trasformazione</span><span class="sxs-lookup"><span data-stu-id="e0cda-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0cda-163">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="e0cda-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="e0cda-164">Descrizione del file come trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-164">A description of this file as a transform.</span></span> <span data-ttu-id="e0cda-165">La descrizione deve includere la frase: "[Transform](database-transforms.md)".</span><span class="sxs-lookup"><span data-stu-id="e0cda-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="e0cda-166">**Oggetto**</span><span class="sxs-lookup"><span data-stu-id="e0cda-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="e0cda-167">Nome del prodotto installato dal pacchetto di installazione originale.</span><span class="sxs-lookup"><span data-stu-id="e0cda-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="e0cda-168">Deve corrispondere al valore della proprietà di [**Riepilogo dell'oggetto**](subject-summary.md) nel pacchetto di installazione originale.</span><span class="sxs-lookup"><span data-stu-id="e0cda-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="e0cda-169">**Autore**</span><span class="sxs-lookup"><span data-stu-id="e0cda-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="e0cda-170">Nome del produttore di questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="e0cda-171">**Parole chiave**</span><span class="sxs-lookup"><span data-stu-id="e0cda-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="e0cda-172">Un elenco di parole chiave che possono essere usate dai browser di file per cercare un file.</span><span class="sxs-lookup"><span data-stu-id="e0cda-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="e0cda-173">Le parole chiave devono includere "Installer", nonché parole chiave specifiche del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e0cda-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="e0cda-174">**Commenti**</span><span class="sxs-lookup"><span data-stu-id="e0cda-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="e0cda-175">Contiene la frase: "questa trasformazione contiene la logica e i dati necessari per installare <*nome prodotto*>".</span><span class="sxs-lookup"><span data-stu-id="e0cda-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="e0cda-176">[**Modello**](template-summary.md) (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="e0cda-177">Versioni della piattaforma e della lingua compatibili con questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="e0cda-178">Questo valore può essere lasciato vuoto se non sono presenti restrizioni.</span><span class="sxs-lookup"><span data-stu-id="e0cda-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="e0cda-179">È possibile specificare una sola lingua per una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="e0cda-180">Per ulteriori informazioni sulla sintassi, vedere [**template**](template-summary.md).</span><span class="sxs-lookup"><span data-stu-id="e0cda-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="e0cda-181">**Autore ultimo salvataggio**</span><span class="sxs-lookup"><span data-stu-id="e0cda-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="e0cda-182">ID della piattaforma e della lingua del database dopo che è stato trasformato.</span><span class="sxs-lookup"><span data-stu-id="e0cda-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="e0cda-183">È necessario impostare la proprietà di [**Riepilogo del modello**](template-summary.md) nel nuovo database sugli stessi valori.</span><span class="sxs-lookup"><span data-stu-id="e0cda-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="e0cda-184">[**Numero revisione**](revision-number-summary.md) (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="e0cda-185">Elenco dei GUID e della versione del codice prodotto dei prodotti nuovi e originali e del GUID del codice di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e0cda-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="e0cda-186">L'elenco è separato da punti e virgola come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="e0cda-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="e0cda-187">*Originale-prodotto-codice originale-versione prodotto*; *New-Product Code New-Product-Version*; *Aggiornamento-codice*</span><span class="sxs-lookup"><span data-stu-id="e0cda-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="e0cda-188">**Ultima stampa**</span><span class="sxs-lookup"><span data-stu-id="e0cda-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="e0cda-189">Null</span><span class="sxs-lookup"><span data-stu-id="e0cda-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e0cda-190">**Data/ora creazione**</span><span class="sxs-lookup"><span data-stu-id="e0cda-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="e0cda-191">Data e ora di creazione della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="e0cda-192">**Data/ora ultimo salvataggio**</span><span class="sxs-lookup"><span data-stu-id="e0cda-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="e0cda-193">Data e ora di sistema correnti nel momento in cui la trasformazione è stata salvata.</span><span class="sxs-lookup"><span data-stu-id="e0cda-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="e0cda-194">Inizialmente null.</span><span class="sxs-lookup"><span data-stu-id="e0cda-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="e0cda-195">[**Conteggio pagine**](page-count-summary.md) (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="e0cda-196">Valore utilizzato per indicare la versione minima del programma di installazione necessaria per elaborare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="e0cda-197">Il valore deve essere impostato sul valore maggiore dei due valori della proprietà [**conteggio pagine**](page-count-summary.md) che appartengono ai database utilizzati per generare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="e0cda-198">[**Conteggio parole**](word-count-summary.md) (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="e0cda-199">Null</span><span class="sxs-lookup"><span data-stu-id="e0cda-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="e0cda-200">**Numero di caratteri**</span><span class="sxs-lookup"><span data-stu-id="e0cda-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="e0cda-201">Questa parte del flusso di informazioni di riepilogo è divisa in parole a 2 16 bit.</span><span class="sxs-lookup"><span data-stu-id="e0cda-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="e0cda-202">Il termine superiore contiene i [*flag di convalida della trasformazione*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e0cda-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="e0cda-203">La parola più bassa contiene [*flag di condizione di errore di trasformazione*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e0cda-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="e0cda-204">**Creazione dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="e0cda-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="e0cda-205">Contiene il nome del software utilizzato per creare questa trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e0cda-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="e0cda-206">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="e0cda-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="e0cda-207">Il valore di questa proprietà deve essere di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e0cda-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="e0cda-208">**CodePage**</span><span class="sxs-lookup"><span data-stu-id="e0cda-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="e0cda-209">Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e0cda-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="e0cda-210">Questa proprietà deve essere impostata prima di poter impostare le proprietà di stringa nelle informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e0cda-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="e0cda-211">Pacchetti patch</span><span class="sxs-lookup"><span data-stu-id="e0cda-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0cda-212">Proprietà Summary</span><span class="sxs-lookup"><span data-stu-id="e0cda-212">Summary property</span></span></th>
<th><span data-ttu-id="e0cda-213">Significato di questa proprietà in un pacchetto di patch</span><span class="sxs-lookup"><span data-stu-id="e0cda-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0cda-214"><a href="title-summary.md"><strong>Titolo</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-215">Descrizione del file come pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-215">A description of this file as a patch package.</span></span> <span data-ttu-id="e0cda-216">La descrizione deve includere la frase: &quot; <a href="patch-packages.md">patch</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="e0cda-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-217"><a href="subject-summary.md"><strong>Oggetto</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-218">Descrizione della patch che include il nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e0cda-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-219"><a href="author-summary.md"><strong>Autore</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-220">Nome del produttore del pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-221"><a href="keywords-summary.md"><strong>Parole chiave</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-222">Elenco delimitato da punti e virgola delle origini della patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-223"><a href="comments-summary.md"><strong>Commenti</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-224">Contiene la frase: &quot; questa patch contiene la logica e i dati necessari per installare <<em>nome del prodotto</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="e0cda-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-225"><a href="template-summary.md"><strong>Modello</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-226">Elenco delimitato da punti e virgola dei codici prodotto che possono accettare questa patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-227"><a href="last-saved-by-summary.md"><strong>Autore ultimo salvataggio</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-228">Elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui sono applicati da questa patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-229"><a href="revision-number-summary.md"><strong>Numero revisione</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-230">Contiene il codice della patch GUID per la patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="e0cda-231">Questo può essere seguito da un elenco di GUID di codice patch per le patch che vengono rimosse quando viene applicata questa patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="e0cda-232">I codici patch sono concatenati senza delimitatori che separano i GUID nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e0cda-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0cda-233">Se il pacchetto di patch contiene una tabella <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , la patch non rimuove le patch elencate dopo il GUID della patch corrente.</span><span class="sxs-lookup"><span data-stu-id="e0cda-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-234"><a href="last-printed-summary.md"><strong>Ultima stampa</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-235">Null</span><span class="sxs-lookup"><span data-stu-id="e0cda-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-236"><a href="create-time-date-summary.md"><strong>Data/ora creazione</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-237">Data e ora in cui è stato creato il file di patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-238"><a href="last-saved-time-date-summary.md"><strong>Data/ora ultimo salvataggio</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-239">Data e ora di sistema correnti nel momento in cui è stato salvato il pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="e0cda-240">Questo valore è inizialmente null.</span><span class="sxs-lookup"><span data-stu-id="e0cda-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-241"><a href="page-count-summary.md"><strong>Conteggio pagine</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-242">Null</span><span class="sxs-lookup"><span data-stu-id="e0cda-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-243"><a href="word-count-summary.md"><strong>Conteggio parole</strong></a> (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="e0cda-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="e0cda-244">Contiene un valore che indica la versione minima di Windows Installer necessaria per installare la patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="e0cda-245">Per applicare una patch con un valore di conteggio delle parole pari a 4, è necessario Windows Installer versione 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e0cda-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="e0cda-246">Il valore 3 indica che è necessario Windows Installer versione 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e0cda-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="e0cda-247">Il valore 2 indica che è necessario Windows Installer versione 1,2 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e0cda-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="e0cda-248">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="e0cda-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-249"><a href="character-count-summary.md"><strong>Numero di caratteri</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-250">Null</span><span class="sxs-lookup"><span data-stu-id="e0cda-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-251"><a href="creating-application-summary.md"><strong>Creazione dell'applicazione</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-252">Nome del software utilizzato per creare la patch.</span><span class="sxs-lookup"><span data-stu-id="e0cda-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0cda-253"><a href="security-summary.md"><strong>Sicurezza</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-254">Il valore di questa proprietà deve essere di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e0cda-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0cda-255"><a href="codepage-summary.md"><strong>CodePage</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0cda-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="e0cda-256">Valore numerico della tabella codici ANSI utilizzata per visualizzare le informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e0cda-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="e0cda-257">Questa proprietà deve essere impostata prima di impostare le proprietà di stringa nelle informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e0cda-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




