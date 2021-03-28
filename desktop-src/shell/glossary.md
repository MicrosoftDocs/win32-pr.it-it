---
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
title: Glossario della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345396"
---
# <a name="shell-glossary"></a><span data-ttu-id="4de60-103">Glossario della shell</span><span class="sxs-lookup"><span data-stu-id="4de60-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="4de60-104">A</span><span class="sxs-lookup"><span data-stu-id="4de60-104">A</span></span>

<dl> <dt>

<span data-ttu-id="4de60-105">**associazione**</span><span class="sxs-lookup"><span data-stu-id="4de60-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-106">Mapping di un'estensione di file (ad esempio,. mp3) o di un protocollo (ad esempio, http) a un identificatore a livello di codice (ProgID).</span><span class="sxs-lookup"><span data-stu-id="4de60-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="4de60-107">Questo mapping viene archiviato nel registro di sistema come impostazione per utente con fallback per computer.</span><span class="sxs-lookup"><span data-stu-id="4de60-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="4de60-108">Le applicazioni che fanno parte del sistema di programmi predefiniti impostano il mapping di associazione per l'estensione o il protocollo del nome di file in modo che punti alle chiavi ProgID di loro proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de60-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-109">**array di associazioni**</span><span class="sxs-lookup"><span data-stu-id="4de60-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-110">Elenco ordinato di percorsi del registro di sistema utilizzati per archiviare informazioni su un tipo di elemento, inclusi gestori, verbi e altri attributi, come l'icona e il nome visualizzato del tipo.</span><span class="sxs-lookup"><span data-stu-id="4de60-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="4de60-111">Ad esempio, un file con estensione jpg presenta la seguente matrice di associazioni in un sistema Windows predefinito: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "HKCR \\ SystemFileAssociations \\ image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".</span><span class="sxs-lookup"><span data-stu-id="4de60-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="4de60-112">B</span><span class="sxs-lookup"><span data-stu-id="4de60-112">B</span></span>

<dl> <dt>

<span data-ttu-id="4de60-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="4de60-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-114">Per caricare o associare il codice ai dati.</span><span class="sxs-lookup"><span data-stu-id="4de60-114">To load or associate code with data.</span></span> <span data-ttu-id="4de60-115">Ad esempio, un gestore può essere associato a un'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="4de60-116">C</span><span class="sxs-lookup"><span data-stu-id="4de60-116">C</span></span>

<dl> <dt>

<span data-ttu-id="4de60-117">**nome canonico**</span><span class="sxs-lookup"><span data-stu-id="4de60-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-118">Nome univoco di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="4de60-118">The unique name of a resource.</span></span> <span data-ttu-id="4de60-119">"Canonical" indica "secondo le regole".</span><span class="sxs-lookup"><span data-stu-id="4de60-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="4de60-120">Vedere anche: nome del verbo canonico.</span><span class="sxs-lookup"><span data-stu-id="4de60-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-121">**nome del verbo canonico**</span><span class="sxs-lookup"><span data-stu-id="4de60-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-122">Nome indipendente dalla lingua che può essere utilizzato a livello di codice per fare riferimento a un verbo, indipendentemente dalla stringa localizzata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4de60-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="4de60-123">Vedere anche: nome canonico, verbo.</span><span class="sxs-lookup"><span data-stu-id="4de60-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-124">**container**</span><span class="sxs-lookup"><span data-stu-id="4de60-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-125">Tipo di elemento della shell che può contenere altri elementi.</span><span class="sxs-lookup"><span data-stu-id="4de60-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="4de60-126">Gli elementi in un contenitore vengono esposti allo spazio dei nomi della shell utilizzando un'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="4de60-127">Gli esempi includono cartelle, unità, server di rete e file compressi con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="4de60-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="4de60-128">Vedere anche: origine dati della shell, cartella, elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-129">**content**</span><span class="sxs-lookup"><span data-stu-id="4de60-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-130">Testo e proprietà associati a un elemento della shell o a un'origine di contenuto che può essere indicizzata.</span><span class="sxs-lookup"><span data-stu-id="4de60-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-131">**origine contenuto**</span><span class="sxs-lookup"><span data-stu-id="4de60-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-132">Elemento a cui è possibile accedere dall'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="4de60-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="4de60-133">Le origini di contenuto sono indirizzabili da un URL e vengono fornite all'indicizzatore da un gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="4de60-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="4de60-134">Gli esempi includono: file system file e cartelle, elementi e cartelle di Microsoft Outlook, record del database e elementi archiviati di Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4de60-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="4de60-135">Un'origine di contenuto può essere esposta come elementi della shell implementando un'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="4de60-136">Vedere anche: contenuto, elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-137">**content view (visualizzazione contenuto)**</span><span class="sxs-lookup"><span data-stu-id="4de60-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-138">Visualizzazione in Esplora risorse (disponibile in Windows 7 e versioni successive) che Visualizza il contenuto più rilevante per ogni elemento nell'elenco in base all'estensione del nome file o all'associazione di tipo.</span><span class="sxs-lookup"><span data-stu-id="4de60-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="4de60-139">La visualizzazione contenuto usa una logica di ridimensionamento che elimina le proprietà quando le dimensioni della finestra diminuiscono per garantire che le proprietà più importanti abbiano ancora spazio per essere leggibili in modo chiaro.</span><span class="sxs-lookup"><span data-stu-id="4de60-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="4de60-140">Vedere anche: modello di layout, tipo, associazione di tipo.</span><span class="sxs-lookup"><span data-stu-id="4de60-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-141">**modalità di visualizzazione contenuto**</span><span class="sxs-lookup"><span data-stu-id="4de60-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-142">Vedere la definizione di: visualizzazione contenuto.</span><span class="sxs-lookup"><span data-stu-id="4de60-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-143">**menu di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="4de60-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-144">Questo termine viene talvolta usato per indicare il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="4de60-145">Vedere definizione per: menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-146">**gestore menu di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="4de60-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-147">Questo termine viene talvolta usato per indicare il gestore dei menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="4de60-148">Vedere definizione per: gestore del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="4de60-149">D</span><span class="sxs-lookup"><span data-stu-id="4de60-149">D</span></span>

<dl> <dt>

<span data-ttu-id="4de60-150">**gestore dell'oggetto dati**</span><span class="sxs-lookup"><span data-stu-id="4de60-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-151">Gestore che fornisce altri formati degli Appunti per l'oggetto dati (IDataObject) di un elemento.</span><span class="sxs-lookup"><span data-stu-id="4de60-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="4de60-152">Gli oggetti dati vengono usati negli scenari di trascinamento della selezione e di copia e incolla.</span><span class="sxs-lookup"><span data-stu-id="4de60-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-153">**origine dati**</span><span class="sxs-lookup"><span data-stu-id="4de60-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-154">Questo termine viene talvolta usato per indicare l'origine dati dell'archivio dati o della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="4de60-155">Vedere la definizione per: archivio dati, origine dati Shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-156">**archivio dati**</span><span class="sxs-lookup"><span data-stu-id="4de60-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-157">Repository di dati.</span><span class="sxs-lookup"><span data-stu-id="4de60-157">A repository of data.</span></span> <span data-ttu-id="4de60-158">Un archivio dati può essere esposto al modello di programmazione della shell come contenitore usando un'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="4de60-159">Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="4de60-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-160">**composizione del desktop**</span><span class="sxs-lookup"><span data-stu-id="4de60-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-161">Funzionalità di Windows Vista che consente di disegnare singole finestre per le superfici fuori schermo nella memoria video anziché il disegno direttamente sul dispositivo di visualizzazione principale.</span><span class="sxs-lookup"><span data-stu-id="4de60-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-162">**document**</span><span class="sxs-lookup"><span data-stu-id="4de60-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-163">Elemento della shell che contiene testo e per il quale è possibile implementare l'interfaccia IFilter.</span><span class="sxs-lookup"><span data-stu-id="4de60-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-164">**gestore di trascinamento**</span><span class="sxs-lookup"><span data-stu-id="4de60-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-165">Gestore che consente a un particolare tipo di elemento di supportare gli scenari di trascinamento della selezione e di copia e incolla.</span><span class="sxs-lookup"><span data-stu-id="4de60-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-166">**destinazione di rilascio**</span><span class="sxs-lookup"><span data-stu-id="4de60-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-167">Oggetto dati trascinato e rilasciato su un file.</span><span class="sxs-lookup"><span data-stu-id="4de60-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="4de60-168">Vedere anche: gestore dati, Drop Handler.</span><span class="sxs-lookup"><span data-stu-id="4de60-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-169">**verbo dinamico**</span><span class="sxs-lookup"><span data-stu-id="4de60-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-170">Verbo che dipende dallo stato di un elemento della shell o del sistema; l'aspetto dell'elemento è basato sullo stato e richiede che il codice in esecuzione determini se l'elemento deve essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="4de60-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="4de60-171">Vedere anche: gestore del menu di scelta rapida, verbo statico, verbo.</span><span class="sxs-lookup"><span data-stu-id="4de60-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="4de60-172">E</span><span class="sxs-lookup"><span data-stu-id="4de60-172">E</span></span>

<dl> <dt>

<span data-ttu-id="4de60-173">**Comando Explorer**</span><span class="sxs-lookup"><span data-stu-id="4de60-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-174">Oggetto che può essere visualizzato come pulsante nella parte superiore della finestra di Esplora risorse che fornisce la funzionalità per gli elementi e i contenitori in tale finestra.</span><span class="sxs-lookup"><span data-stu-id="4de60-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="4de60-175">Un'origine dati della shell fornisce gli oggetti comando di Esplora risorse per un elemento contenitore specifico.</span><span class="sxs-lookup"><span data-stu-id="4de60-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="4de60-176">I comandi vengono talvolta usati come verbi.</span><span class="sxs-lookup"><span data-stu-id="4de60-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="4de60-177">F</span><span class="sxs-lookup"><span data-stu-id="4de60-177">F</span></span>

<dl> <dt>

<span data-ttu-id="4de60-178">**associazione file**</span><span class="sxs-lookup"><span data-stu-id="4de60-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-179">Vedere definizione per: associazione tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-180">**formato file**</span><span class="sxs-lookup"><span data-stu-id="4de60-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-181">Formato per i dati archiviati in un file con una specifica di formato documentata.</span><span class="sxs-lookup"><span data-stu-id="4de60-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="4de60-182">Gli esempi includono OLE DocFile, OPC, XML, ZIP e altre specifiche del formato di file noto.</span><span class="sxs-lookup"><span data-stu-id="4de60-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="4de60-183">Gli autori dei tipi di file usano in genere un formato di file esistente come base di un nuovo tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="4de60-184">Un formato di file può essere semplicemente una definizione di cui non viene creata un'istanza come tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-185">**gestore formato file**</span><span class="sxs-lookup"><span data-stu-id="4de60-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-186">Questo termine è un sinonimo del gestore dei tipi di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="4de60-187">Vedere definizione per: gestore tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-188">**estensione del nome file**</span><span class="sxs-lookup"><span data-stu-id="4de60-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-189">L'indicatore principale di un tipo di file per file system elementi è la parte del nome file che segue il punto finale.</span><span class="sxs-lookup"><span data-stu-id="4de60-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="4de60-190">L'estensione del nome file non può contenere spazi o caratteri non ASCII e si applica solo ai file (non alle cartelle).</span><span class="sxs-lookup"><span data-stu-id="4de60-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="4de60-191">Le estensioni di file vengono confrontate utilizzando una funzione di confronto che non è sensibile a case o impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="4de60-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="4de60-192">Vedere anche: formato di file, tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-193">**tipo di file**</span><span class="sxs-lookup"><span data-stu-id="4de60-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-194">Un particolare valore di estensione del nome di file, ad esempio ". htm" o ". jpg", che definisce una classe di file che sono dello stesso tipo e hanno un set comune di associazioni.</span><span class="sxs-lookup"><span data-stu-id="4de60-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="4de60-195">Vedere anche: tipo, associazione del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-196">**associazione di tipi di file**</span><span class="sxs-lookup"><span data-stu-id="4de60-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-197">Per un'estensione di file particolare, gli elementi di matrice di associazione che definiscono dove possono essere registrati i gestori e altri attributi.</span><span class="sxs-lookup"><span data-stu-id="4de60-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="4de60-198">Vedere anche: array di associazioni, tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-199">**personalizzazione del tipo di file**</span><span class="sxs-lookup"><span data-stu-id="4de60-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-200">Un'associazione che consente a Shell di personalizzare il modo in cui la shell considera un tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="4de60-201">Le personalizzazioni dei tipi di file includono: specificando l'applicazione utilizzata per aprire il file quando si fa doppio clic su di esso, aggiungendo comandi al menu di scelta rapida per un tipo di file, specificando un'icona personalizzata, specificando un tipo di contenuto MIME da associare a un tipo di file, specificando un tipo percepito e specificando una o più applicazioni associate dal tipo di file con</span><span class="sxs-lookup"><span data-stu-id="4de60-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="4de60-202">Vedere anche: PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="4de60-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-203">**gestore tipo di file**</span><span class="sxs-lookup"><span data-stu-id="4de60-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-204">Gestore registrato per un tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-204">A handler registered for a file type.</span></span> <span data-ttu-id="4de60-205">Vedere anche: handler.</span><span class="sxs-lookup"><span data-stu-id="4de60-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-206">**cartella**</span><span class="sxs-lookup"><span data-stu-id="4de60-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-207">Vedere la definizione per: container.</span><span class="sxs-lookup"><span data-stu-id="4de60-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-208">**PIDL completo**</span><span class="sxs-lookup"><span data-stu-id="4de60-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-209">PIDL che descrive in modo univoco un oggetto relativo alla cartella desktop.</span><span class="sxs-lookup"><span data-stu-id="4de60-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="4de60-210">H</span><span class="sxs-lookup"><span data-stu-id="4de60-210">H</span></span>

<dl> <dt>

<span data-ttu-id="4de60-211">**gestore**</span><span class="sxs-lookup"><span data-stu-id="4de60-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-212">Oggetto COM che fornisce la funzionalità per un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="4de60-213">La maggior parte delle origini dati della Shell offre un sistema estensibile per l'associazione di gestori agli elementi.</span><span class="sxs-lookup"><span data-stu-id="4de60-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="4de60-214">Ad esempio, la cartella file system usa il sistema di associazione per cercare i gestori per un tipo di file specifico.</span><span class="sxs-lookup"><span data-stu-id="4de60-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="4de60-215">Vedere anche: associazione di file, tipo di file, personalizzazione del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="4de60-216">I</span><span class="sxs-lookup"><span data-stu-id="4de60-216">I</span></span>

<dl> <dt>

<span data-ttu-id="4de60-217">**gestore icone**</span><span class="sxs-lookup"><span data-stu-id="4de60-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-218">Gestore che fornisce le informazioni necessarie per generare e memorizzare nella cache un'icona per un elemento.</span><span class="sxs-lookup"><span data-stu-id="4de60-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="4de60-219">L'archivio dati file system supporta il caricamento di un gestore di icone per un elemento in base al tipo di file, consentendo a tale gestore di fornire un'icona utilizzata per tutte le istanze del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-220">**gestore infotip**</span><span class="sxs-lookup"><span data-stu-id="4de60-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-221">Gestore che fornisce il testo popup quando l'utente posiziona il puntatore del mouse su un oggetto dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4de60-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-222">**item**</span><span class="sxs-lookup"><span data-stu-id="4de60-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-223">Vedere la definizione di: elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-224">**classe Item**</span><span class="sxs-lookup"><span data-stu-id="4de60-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-225">Vedere definizione per: tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-226">**elenco degli identificatori di elemento**</span><span class="sxs-lookup"><span data-stu-id="4de60-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-227">Sequenza di una o più strutture SHITEMID che definiscono in modo univoco un oggetto relativo a un oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="4de60-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="4de60-228">K</span><span class="sxs-lookup"><span data-stu-id="4de60-228">K</span></span>

<dl> <dt>

<span data-ttu-id="4de60-229">**Tipologia**</span><span class="sxs-lookup"><span data-stu-id="4de60-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-230">Proprietà che fornisce un nome descrittivo per l'utente e può essere associata a un elenco di proprietà e a un modello di layout.</span><span class="sxs-lookup"><span data-stu-id="4de60-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="4de60-231">Il tipo è stato introdotto in Windows Vista per esprimere una nozione di tipo file più intuitiva per l'utente finale ed è stata definita come una proprietà di stringa multivalore (valori stringa canonici), pertanto è possibile avere un valore Kind "audio; video" o "link; Document".</span><span class="sxs-lookup"><span data-stu-id="4de60-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="4de60-232">Alcuni nomi descrittivi dei tipi sono già associati a proprietà e modelli di layout.</span><span class="sxs-lookup"><span data-stu-id="4de60-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="4de60-233">Ad esempio, gli elementi associati a kind. Picture e gli elementi associati a Kind.Document visualizzano proprietà diverse anche quando si trovano nella stessa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4de60-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="4de60-234">Ogni tipo di elemento può essere associato a uno dei quattro modelli di layout univoci che definiscono il numero di proprietà visualizzate per ogni elemento e il relativo layout.</span><span class="sxs-lookup"><span data-stu-id="4de60-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="4de60-235">Vedere anche: associazione di tipo, visualizzazione contenuto, modello di layout.</span><span class="sxs-lookup"><span data-stu-id="4de60-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="4de60-236">L</span><span class="sxs-lookup"><span data-stu-id="4de60-236">L</span></span>

<dl> <dt>

<span data-ttu-id="4de60-237">**modello layout**</span><span class="sxs-lookup"><span data-stu-id="4de60-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-238">Uno dei diversi accordi per la visualizzazione delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de60-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="4de60-239">In Windows 7 e versioni successive, quando si registra un nuovo tipo di file, è possibile usare la visualizzazione contenuto per registrare un elenco di proprietà e un modello di layout personalizzati per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="4de60-240">È possibile scegliere tra quattro diversi modelli di layout: Alpha (per i risultati della ricerca di documenti contenenti frammenti di codice), beta (per i risultati della ricerca tramite posta elettronica con frammenti di codice), gamma (simile ad Alpha ma con layout a due righe anziché quattro) e Delta (per visualizzare molte proprietà più brevi, ad esempio con musica e immagini).</span><span class="sxs-lookup"><span data-stu-id="4de60-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="4de60-241">Vedere anche: visualizzazione del contenuto, tipo, associazione di tipo.</span><span class="sxs-lookup"><span data-stu-id="4de60-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="4de60-242">M</span><span class="sxs-lookup"><span data-stu-id="4de60-242">M</span></span>

<dl> <dt>

<span data-ttu-id="4de60-243">**gestore di metadati**</span><span class="sxs-lookup"><span data-stu-id="4de60-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-244">Questo termine viene talvolta usato per indicare il gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de60-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="4de60-245">Vedere la definizione di: gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de60-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="4de60-246">N</span><span class="sxs-lookup"><span data-stu-id="4de60-246">N</span></span>

<dl> <dt>

<span data-ttu-id="4de60-247">**estensione dello spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="4de60-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-248">Vedere la definizione di: origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="4de60-249">O</span><span class="sxs-lookup"><span data-stu-id="4de60-249">O</span></span>

<dl> <dt>

<span data-ttu-id="4de60-250">**Collegamento di oggetti e database di incorporamento (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="4de60-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-251">Un set standard di interfacce che fornisce accesso eterogeneo a origini diverse di informazioni situate ovunque, ad esempio file System, cartelle di posta elettronica e database.</span><span class="sxs-lookup"><span data-stu-id="4de60-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="4de60-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-253">Vedere la definizione per: collegamento di oggetti e database di incorporamento.</span><span class="sxs-lookup"><span data-stu-id="4de60-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="4de60-254">P</span><span class="sxs-lookup"><span data-stu-id="4de60-254">P</span></span>

<dl> <dt>

<span data-ttu-id="4de60-255">**PerceivedType**</span><span class="sxs-lookup"><span data-stu-id="4de60-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-256">Ampia categoria di tipi di formato di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-256">A broad category of file format types.</span></span> <span data-ttu-id="4de60-257">PerceivedType è stato introdotto in Windows XP e supporta un set limitato di tipi di file noti, ad esempio immagini, testo, audio e tipi di file compressi.</span><span class="sxs-lookup"><span data-stu-id="4de60-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="4de60-258">I tipi di file, generalmente i tipi di file pubblici, possono anche avere un tipo percepito.</span><span class="sxs-lookup"><span data-stu-id="4de60-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="4de60-259">Ad esempio, i tipi di file di immagine. bmp,. png,. jpg e. gif sono anche di tipo percepito, image.</span><span class="sxs-lookup"><span data-stu-id="4de60-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="4de60-260">A livello di programmazione, PerceivedType viene espresso come numero intero.</span><span class="sxs-lookup"><span data-stu-id="4de60-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="4de60-261">Poiché è presente codice che usa Kind e PerceivedType, i proprietari del formato di file devono registrarsi entrambi.</span><span class="sxs-lookup"><span data-stu-id="4de60-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="4de60-262">Ad esempio, "Play All" dipende da PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="4de60-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="4de60-263">Vedere anche: tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-264">**gestore di anteprime**</span><span class="sxs-lookup"><span data-stu-id="4de60-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-265">Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento della shell da visualizzare nel riquadro di anteprima di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="4de60-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-266">**Gestore proprietà**</span><span class="sxs-lookup"><span data-stu-id="4de60-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-267">Gestore che converte i dati archiviati in un file in uno schema strutturato riconosciuto da e a cui è possibile accedere da Esplora risorse, da Windows Search e da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4de60-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="4de60-268">Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà da e verso il file.</span><span class="sxs-lookup"><span data-stu-id="4de60-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="4de60-269">I dati tradotti includono la visualizzazione dettagli, infotip, il riquadro dettagli, le pagine delle proprietà e così via.</span><span class="sxs-lookup"><span data-stu-id="4de60-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="4de60-270">Ogni gestore di proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="4de60-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="4de60-271">Vedere anche: sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de60-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-272">**gestore della finestra delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="4de60-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-273">Gestore utilizzato per creare finestre delle proprietà personalizzate con le immagini e i controlli dell'interfaccia utente che consentono l'interazione personalizzata con un tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-274">**sistema di proprietà**</span><span class="sxs-lookup"><span data-stu-id="4de60-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-275">Sistema di lettura/scrittura estendibile di definizioni di dati che utilizza proprietà implementate come coppie nome-valore.</span><span class="sxs-lookup"><span data-stu-id="4de60-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="4de60-276">Vedere anche: gestore della proprietà, elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-277">**valore proprietà**</span><span class="sxs-lookup"><span data-stu-id="4de60-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-278">Valore associato a un nome di proprietà per un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="4de60-279">Ad esempio, "Author", "size" e "date taked" sono proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de60-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="4de60-280">I valori delle proprietà vengono espressi come una struttura PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="4de60-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-281">**gestore di protocollo**</span><span class="sxs-lookup"><span data-stu-id="4de60-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-282">Gestore che accede a origini contenuto e fornisce un oggetto IUrlAccessor per un protocollo e un URL specificati.</span><span class="sxs-lookup"><span data-stu-id="4de60-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="4de60-283">I gestori di protocollo estendono la funzionalità di ricerca di Windows e possono fornire notifiche delle modifiche agli indicizzatori.</span><span class="sxs-lookup"><span data-stu-id="4de60-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="4de60-284">Per indicizzare tipi specifici di archivi dati sono necessari gestori di protocollo diversi.</span><span class="sxs-lookup"><span data-stu-id="4de60-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="4de60-285">Per garantire un'esperienza utente ragionevole, è necessario specificare anche un'origine dati della Shell per l'archivio dati, oltre a implementare il gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="4de60-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="4de60-286">Il gestore di protocollo espone gli elementi nell'archivio dati all'indicizzatore, mentre l'origine dati della shell espone gli elementi nell'archivio dati alla Shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="4de60-287">R</span><span class="sxs-lookup"><span data-stu-id="4de60-287">R</span></span>

<dl> <dt>

<span data-ttu-id="4de60-288">**PIDL relativo**</span><span class="sxs-lookup"><span data-stu-id="4de60-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-289">Un PIDL relativo a un oggetto radice nello spazio dei nomi della shell diverso dalla cartella desktop.</span><span class="sxs-lookup"><span data-stu-id="4de60-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="4de60-290">Si tratta in genere della cartella padre dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4de60-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="4de60-291">S</span><span class="sxs-lookup"><span data-stu-id="4de60-291">S</span></span>

<dl> <dt>

<span data-ttu-id="4de60-292">**Origine dati Shell**</span><span class="sxs-lookup"><span data-stu-id="4de60-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-293">Componente utilizzato per estendere lo spazio dei nomi della shell ed esporre gli elementi in un archivio dati.</span><span class="sxs-lookup"><span data-stu-id="4de60-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="4de60-294">In passato, l'origine dati della shell era denominata estensione dello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="4de60-295">Vedere anche: contenitore, gestore, elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-296">**Estensione della shell**</span><span class="sxs-lookup"><span data-stu-id="4de60-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-297">Questo termine viene talvolta usato per indicare il gestore del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="4de60-298">Vedere definizione per: gestore tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-299">**Gestore dell'estensione della shell**</span><span class="sxs-lookup"><span data-stu-id="4de60-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-300">Questo termine viene talvolta usato per indicare il gestore del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="4de60-301">Vedere definizione per: gestore tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-302">**Gestore Shell**</span><span class="sxs-lookup"><span data-stu-id="4de60-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-303">Questo termine viene talvolta usato per indicare il gestore del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="4de60-304">Vedere definizione per: gestore tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-305">**Elemento della shell**</span><span class="sxs-lookup"><span data-stu-id="4de60-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-306">Una singola parte di contenuto.</span><span class="sxs-lookup"><span data-stu-id="4de60-306">A single piece of content.</span></span> <span data-ttu-id="4de60-307">Alcuni elementi della shell sono origini di contenuto e altri no.</span><span class="sxs-lookup"><span data-stu-id="4de60-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="4de60-308">Una cartella è un'origine di contenuto, ad esempio, ma non è presente un file con estensione jpg.</span><span class="sxs-lookup"><span data-stu-id="4de60-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="4de60-309">I gestori di tipi di file espongono gli elementi della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="4de60-310">In alcuni contesti "Item" viene usato per distinguere i contenitori da non contenitori.</span><span class="sxs-lookup"><span data-stu-id="4de60-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="4de60-311">Vedere anche: contenitore, origine del contenuto, gestore del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="4de60-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-312">**Estensione dello spazio dei nomi shell**</span><span class="sxs-lookup"><span data-stu-id="4de60-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-313">Questo termine viene talvolta usato per indicare l'origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="4de60-314">Vedere la definizione di: origine dati della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-315">**menu di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="4de60-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-316">Interfaccia utente utilizzata per presentare una raccolta di verbi associati a un elemento dell'interfaccia utente, ad esempio un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="4de60-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-317">**Gestore del menu di scelta rapida**</span><span class="sxs-lookup"><span data-stu-id="4de60-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-318">Gestore che aggiunge verbi per un elemento o elementi.</span><span class="sxs-lookup"><span data-stu-id="4de60-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="4de60-319">Questi verbi vengono in genere visualizzati in un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="4de60-320">Vedere anche: menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-321">**PIDL semplice**</span><span class="sxs-lookup"><span data-stu-id="4de60-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-322">PIDL analizzato senza verifica del disco.</span><span class="sxs-lookup"><span data-stu-id="4de60-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-323">**verbo statico**</span><span class="sxs-lookup"><span data-stu-id="4de60-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-324">Verbo che si applica a un elemento della shell senza che sia necessario controllare lo stato corrente di un elemento o di un sistema.</span><span class="sxs-lookup"><span data-stu-id="4de60-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="4de60-325">Un verbo statico si basa su una registrazione statica degli elementi associati di un elemento e non cambia.</span><span class="sxs-lookup"><span data-stu-id="4de60-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="4de60-326">T</span><span class="sxs-lookup"><span data-stu-id="4de60-326">T</span></span>

<dl> <dt>

<span data-ttu-id="4de60-327">**gestore anteprime**</span><span class="sxs-lookup"><span data-stu-id="4de60-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-328">Gestore che fornisce un'immagine statica per rappresentare un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-329">**provider di anteprime**</span><span class="sxs-lookup"><span data-stu-id="4de60-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-330">Questo termine viene talvolta usato per indicare il gestore di anteprime.</span><span class="sxs-lookup"><span data-stu-id="4de60-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="4de60-331">Vedere la definizione per: gestore anteprime.</span><span class="sxs-lookup"><span data-stu-id="4de60-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="4de60-332">U</span><span class="sxs-lookup"><span data-stu-id="4de60-332">U</span></span>

<dl> <dt>

<span data-ttu-id="4de60-333">**nome descrittivo del tipo**</span><span class="sxs-lookup"><span data-stu-id="4de60-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-334">Vedere la definizione per: Kind.</span><span class="sxs-lookup"><span data-stu-id="4de60-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="4de60-335">V</span><span class="sxs-lookup"><span data-stu-id="4de60-335">V</span></span>

<dl> <dt>

<span data-ttu-id="4de60-336">**verb**</span><span class="sxs-lookup"><span data-stu-id="4de60-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-337">Singola azione che può essere chiamata da un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="4de60-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="4de60-338">Gli esempi includono Open e Print.</span><span class="sxs-lookup"><span data-stu-id="4de60-338">Examples include open and print.</span></span> <span data-ttu-id="4de60-339">I verbi sono talvolta denominati comandi o attività.</span><span class="sxs-lookup"><span data-stu-id="4de60-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="4de60-340">Vedere anche: verbo dinamico, gestore del menu di scelta rapida, verbo statico.</span><span class="sxs-lookup"><span data-stu-id="4de60-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="4de60-341">**gestore di verbi**</span><span class="sxs-lookup"><span data-stu-id="4de60-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="4de60-342">Questo termine viene talvolta usato per indicare il gestore dei menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="4de60-343">Vedere definizione per: gestore del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4de60-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



