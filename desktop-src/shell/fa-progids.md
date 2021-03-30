---
description: La shell usa una sottochiave del registro di sistema ProgID (Programmatic Identifier) per associare un tipo di file a un'applicazione e per controllare il comportamento dell'associazione.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificatori a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993709"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="6ce52-103">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="6ce52-103">Programmatic Identifiers</span></span>

<span data-ttu-id="6ce52-104">La shell usa una sottochiave del registro di sistema ProgID (Programmatic Identifier) per associare un tipo di file a un'applicazione e per controllare il comportamento dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6ce52-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="6ce52-105">Le voci ProgID usate per le associazioni di file si trovano in **HKEY \_ classi \_ radice** nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6ce52-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="6ce52-106">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6ce52-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6ce52-107">Elementi identificatore a livello di codice usati dalle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="6ce52-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="6ce52-108">Utilizzo di identificatori a livello di codice con versione</span><span class="sxs-lookup"><span data-stu-id="6ce52-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="6ce52-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ce52-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="6ce52-110">Per ulteriori informazioni, vedere [come registrare un tipo di file per una nuova applicazione](how-to-register-a-file-type-for-a-new-application.md)</span><span class="sxs-lookup"><span data-stu-id="6ce52-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="6ce52-111">Elementi identificatore a livello di codice usati dalle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="6ce52-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="6ce52-112">Il formato corretto del nome di una chiave ProgID è \[ *vendor o Application* \] . \[ *Componente* \] . \[ *Versione* \] , separata da punti e senza spazi, come in Word.Document. 6.</span><span class="sxs-lookup"><span data-stu-id="6ce52-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="6ce52-113">La parte relativa alla *versione* è facoltativa ma fortemente consigliata.</span><span class="sxs-lookup"><span data-stu-id="6ce52-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="6ce52-114">Per ulteriori informazioni, vedere [utilizzo di identificatori a livello di codice con versione](#using-versioned-programmatic-identifiers).</span><span class="sxs-lookup"><span data-stu-id="6ce52-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="6ce52-115">Una sottochiave ProgID deve includere gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="6ce52-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="6ce52-116">Si noti che alcuni dati stringa in questa chiave richiedono una formattazione specifica.</span><span class="sxs-lookup"><span data-stu-id="6ce52-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ce52-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ce52-117">Element</span></span></th>
<th><span data-ttu-id="6ce52-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ce52-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ce52-119"><strong>Predefinita</strong></span><span class="sxs-lookup"><span data-stu-id="6ce52-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="6ce52-120">Impostare la voce predefinita della sottochiave ProgID su un nome descrittivo per il ProgID, adatto per la visualizzazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="6ce52-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="6ce52-121">L'uso di questa voce per conservare il nome descrittivo è deprecato dalla voce FriendlyTypeName nei sistemi che eseguono Windows 2000 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6ce52-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="6ce52-122">Tuttavia, è necessario impostare questo valore per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="6ce52-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ce52-123"><strong>AllowSilentDefaultTakeOver</strong> (introdotta in Windows 8)</span><span class="sxs-lookup"><span data-stu-id="6ce52-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="6ce52-124">Impostare questa voce facoltativa per segnalare che Windows deve ignorare questo ProgID quando si determina un gestore predefinito per un tipo di file pubblico.</span><span class="sxs-lookup"><span data-stu-id="6ce52-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="6ce52-125">Indipendentemente dall'impostazione di questo valore, il ProgID continuerà a essere visualizzato nel menu di scelta rapida e nella finestra di dialogo OpenWith.</span><span class="sxs-lookup"><span data-stu-id="6ce52-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="6ce52-126">Si tratta di un valore REG_NONE.</span><span class="sxs-lookup"><span data-stu-id="6ce52-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ce52-127"><strong>AppUserModelID</strong> (introdotta in Windows 7)</span><span class="sxs-lookup"><span data-stu-id="6ce52-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="6ce52-128">Impostare questa voce facoltativa sull'ID del modello utente dell'applicazione esplicita dell'applicazione (AppUserModelID) se l'applicazione usa un AppUserModelID esplicito e usa gli elenchi di salto <strong>recenti</strong> o <strong>frequenti</strong> generati automaticamente dal sistema oppure fornisce una Jump List personalizzata.</span><span class="sxs-lookup"><span data-stu-id="6ce52-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="6ce52-129">Se un'applicazione usa un AppUserModelID esplicito e non imposta questo valore, gli elementi non verranno visualizzati nelle Jump List dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ce52-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="6ce52-130">Si tratta di una stringa REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="6ce52-130">This is a REG_SZ string.</span></span> <span data-ttu-id="6ce52-131">Per ulteriori informazioni, vedere <a href="appids.md">ID modello utente applicazione (AppUserModelIDs)</a>.</span><span class="sxs-lookup"><span data-stu-id="6ce52-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ce52-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="6ce52-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="6ce52-133">Impostare questa voce facoltativa utilizzando i flag dell'enumerazione <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6ce52-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="6ce52-134">La voce flag controlla alcuni aspetti della gestione della shell dei tipi di file collegati a questo ProgID.</span><span class="sxs-lookup"><span data-stu-id="6ce52-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="6ce52-135">È anche possibile usare la voce flag per limitare la quantità di dati che l'utente può modificare per determinati aspetti di questi tipi di file usando la finestra delle proprietà di un file.</span><span class="sxs-lookup"><span data-stu-id="6ce52-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="6ce52-136">I valori <strong>FILETYPEATTRIBUTEFLAGS</strong> usati per flag sono valori binari progettati in modo da poter combinare più attributi in un singolo valore in un'operazione OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="6ce52-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="6ce52-137">Si tratta di un valore REG_DWORD o REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="6ce52-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ce52-138"><strong>FriendlyTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="6ce52-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="6ce52-139">Impostare questa voce su un nome descrittivo per il ProgID, adatto per la visualizzazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="6ce52-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="6ce52-140">Per coerenza, questa stringa deve contenere gli stessi dati della voce predefinita per la chiave ProgID.</span><span class="sxs-lookup"><span data-stu-id="6ce52-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="6ce52-141">Questa voce può essere una stringa REG_SZ o REG_EXPAND_SZ, ma deve essere formattata come stringa indiretta (un nome file completo e un valore di risorsa preceduto dal simbolo @), ad esempio <em>@% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="6ce52-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ce52-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="6ce52-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="6ce52-143">Impostare questa voce su un breve messaggio della Guida visualizzato dalla Shell per questo ProgID.</span><span class="sxs-lookup"><span data-stu-id="6ce52-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="6ce52-144">La voce InfoTip viene visualizzata in una finestra di dialogo del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="6ce52-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="6ce52-145">Questo valore può essere una stringa REG_SZ o REG_EXPAND_SZ ma, ad esempio FriendlyTypeName, deve essere formattata come stringa indiretta.</span><span class="sxs-lookup"><span data-stu-id="6ce52-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ce52-146"><strong>CurVer</strong></span><span class="sxs-lookup"><span data-stu-id="6ce52-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="6ce52-147">Impostare la voce (impostazione predefinita) di questa sottochiave sulla versione più recente di questo ProgID.</span><span class="sxs-lookup"><span data-stu-id="6ce52-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6ce52-148">A meno che non si disponga di versioni dell'applicazione side-by-Side, ovvero più versioni installate nello stesso sistema, è consigliabile evitare di utilizzare <strong>Curver</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ce52-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ce52-149"><strong>DefaultIcon</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ce52-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="6ce52-150">Impostare la voce (impostazione predefinita) di questa sottochiave sull'icona predefinita che si desidera visualizzare per i tipi di file associati a questo ProgID.</span><span class="sxs-lookup"><span data-stu-id="6ce52-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="6ce52-151">Questo valore può essere una stringa REG_SZ o REG_EXPAND_SZ, ma deve essere specificato come nome di file completo con il relativo valore di risorsa di supervisore, ad esempio <em>% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="6ce52-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6ce52-152">Nell'esempio di chiave del registro di sistema seguente viene illustrato un nodo chiave ProgID di associazione file:</span><span class="sxs-lookup"><span data-stu-id="6ce52-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="6ce52-153">Utilizzo di identificatori a livello di codice con versione</span><span class="sxs-lookup"><span data-stu-id="6ce52-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="6ce52-154">Un ProgID con versione è uno la cui versione è indicata nel nome.</span><span class="sxs-lookup"><span data-stu-id="6ce52-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="6ce52-155">Questa operazione viene in genere eseguita aggiungendo un punto e il numero di versione al nome.</span><span class="sxs-lookup"><span data-stu-id="6ce52-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="6ce52-156">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6ce52-156">For example:</span></span>

-   <span data-ttu-id="6ce52-157">Word.Document. 6</span><span class="sxs-lookup"><span data-stu-id="6ce52-157">Word.Document.6</span></span>
-   <span data-ttu-id="6ce52-158">Word.Document. 8</span><span class="sxs-lookup"><span data-stu-id="6ce52-158">Word.Document.8</span></span>

<span data-ttu-id="6ce52-159">Si tratta di ProgID con versione, rispettivamente con le versioni 6 e 8.</span><span class="sxs-lookup"><span data-stu-id="6ce52-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="6ce52-160">Se si dispone di un'applicazione side-by-Side, ovvero una che supporta più versioni dell'applicazione installate contemporaneamente, utilizzare i ProgID di curvar e della versione indipendenti.</span><span class="sxs-lookup"><span data-stu-id="6ce52-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="6ce52-161">In caso contrario, è consigliabile evitare i ProgID indipendenti dalla curva e dalla versione perché comporteranno un'inefficienza.</span><span class="sxs-lookup"><span data-stu-id="6ce52-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ce52-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ce52-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce52-163">Come registrare un tipo di file per una nuova applicazione</span><span class="sxs-lookup"><span data-stu-id="6ce52-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="6ce52-164">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="6ce52-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="6ce52-165">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="6ce52-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="6ce52-166">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="6ce52-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="6ce52-167">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="6ce52-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="6ce52-168">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="6ce52-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="6ce52-169">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="6ce52-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="6ce52-170">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="6ce52-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="6ce52-171">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="6ce52-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 




