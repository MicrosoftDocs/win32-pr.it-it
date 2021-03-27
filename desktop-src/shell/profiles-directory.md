---
description: 'Il sistema archivia le informazioni sul profilo utente in una directory specifica, che ha nomi diversi in versioni diverse di Windows: &\# 0034; Documents and Settings&\# 0034; in Windows XP e &\# 0034; Utenti&\# 0034; in Windows Vista e versioni successive.'
title: Directory profili
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979951"
---
# <a name="profiles-directory"></a><span data-ttu-id="7cfe0-103">Directory profili</span><span class="sxs-lookup"><span data-stu-id="7cfe0-103">Profiles Directory</span></span>

<span data-ttu-id="7cfe0-104">Il sistema archivia le informazioni sul profilo utente in una directory specifica, che ha nomi diversi in versioni diverse di Windows: "Documents and Settings" in Windows XP e "Users" in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="7cfe0-105">Per ottenere il percorso della directory dei profili, usare la funzione [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="7cfe0-106">La directory dei profili contiene le sottodirectory seguenti per i profili utente.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="7cfe0-107">Directory</span><span class="sxs-lookup"><span data-stu-id="7cfe0-107">Directory</span></span>                                      | <span data-ttu-id="7cfe0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cfe0-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cfe0-109">ProgramData (Windows Vista o versione successiva) utenti</span><span class="sxs-lookup"><span data-stu-id="7cfe0-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="7cfe0-110">Informazioni sul programma applicabili a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-110">Program information that applies to all users.</span></span> <span data-ttu-id="7cfe0-111">La directory tutti gli utenti è ancora presente in Windows Vista o versione successiva per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="7cfe0-112">Predefinito</span><span class="sxs-lookup"><span data-stu-id="7cfe0-112">Default</span></span>                                        | <span data-ttu-id="7cfe0-113">Informazioni sul profilo valide per l'utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="7cfe0-114">*Utente*</span><span class="sxs-lookup"><span data-stu-id="7cfe0-114">*User*</span></span>                                         | <span data-ttu-id="7cfe0-115">Informazioni sul profilo valide per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="7cfe0-116">Ogni utente dispone di una propria sottodirectory di profilo.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="7cfe0-117">Per ottenere il percorso della directory ProgramData/All Users, chiamare la funzione [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="7cfe0-118">La directory contiene le sottodirectory seguenti:</span><span class="sxs-lookup"><span data-stu-id="7cfe0-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="7cfe0-119">Directory</span><span class="sxs-lookup"><span data-stu-id="7cfe0-119">Directory</span></span>  | <span data-ttu-id="7cfe0-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cfe0-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="7cfe0-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="7cfe0-121">Desktop</span></span>    | <span data-ttu-id="7cfe0-122">Collegamenti da visualizzare sul desktop.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="7cfe0-123">Menu Start</span><span class="sxs-lookup"><span data-stu-id="7cfe0-123">Start Menu</span></span> | <span data-ttu-id="7cfe0-124">Voci di menu per il menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="7cfe0-125">Per ottenere il percorso della directory dell'utente predefinito, chiamare la funzione [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="7cfe0-126">Per ottenere il percorso della directory di un utente specifico, chiamare la funzione [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="7cfe0-127">Sia l'utente predefinito che le directory utente specifiche contengono le sottodirectory seguenti.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="7cfe0-128">Le directory in corsivo indicano directory nascoste per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="7cfe0-129">È possibile visualizzare queste directory selezionando l'opzione **Mostra i file nascosti, le cartelle e le unità** nell'elemento del pannello di controllo **Opzioni cartella** .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cfe0-130">Directory</span><span class="sxs-lookup"><span data-stu-id="7cfe0-130">Directory</span></span></th>
<th><span data-ttu-id="7cfe0-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cfe0-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cfe0-132">Dati applicazione</span><span class="sxs-lookup"><span data-stu-id="7cfe0-132">Application Data</span></span></td>
<td><span data-ttu-id="7cfe0-133">Dati specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cfe0-134">Cookie</span><span class="sxs-lookup"><span data-stu-id="7cfe0-134">Cookies</span></span></td>
<td><span data-ttu-id="7cfe0-135">Cookie di Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cfe0-136">Desktop</span><span class="sxs-lookup"><span data-stu-id="7cfe0-136">Desktop</span></span></td>
<td><span data-ttu-id="7cfe0-137">Collegamenti da visualizzare sul desktop.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cfe0-138">Preferiti</span><span class="sxs-lookup"><span data-stu-id="7cfe0-138">Favorites</span></span></td>
<td><span data-ttu-id="7cfe0-139">Collegamenti ai siti Web preferiti.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cfe0-140">Impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="7cfe0-140">Local Settings</span></span></td>
<td><span data-ttu-id="7cfe0-141">Impostazioni e dati dell'applicazione che non eseguono il roaming con il profilo.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="7cfe0-142">In genere le impostazioni o i dati in questa directory sono specifici del computer o sono troppo grandi per il roaming efficace.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="7cfe0-143">Questa directory contiene le sottocartelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="7cfe0-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="7cfe0-144">Dati applicazione</span><span class="sxs-lookup"><span data-stu-id="7cfe0-144">Application Data</span></span></li>
<li><span data-ttu-id="7cfe0-145">Cronologia</span><span class="sxs-lookup"><span data-stu-id="7cfe0-145">History</span></span></li>
<li><span data-ttu-id="7cfe0-146">Temp</span><span class="sxs-lookup"><span data-stu-id="7cfe0-146">Temp</span></span></li>
<li><span data-ttu-id="7cfe0-147">File temporanei di Internet</span><span class="sxs-lookup"><span data-stu-id="7cfe0-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cfe0-148">Documenti</span><span class="sxs-lookup"><span data-stu-id="7cfe0-148">My Documents</span></span></td>
<td><span data-ttu-id="7cfe0-149">Il percorso predefinito per i documenti creati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="7cfe0-150">Per impostazione predefinita, le applicazioni devono salvare i file di documento in questa directory.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cfe0-151"><em>NetHood</em></span><span class="sxs-lookup"><span data-stu-id="7cfe0-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="7cfe0-152">Collegamenti agli elementi del quartiere di rete.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cfe0-153"><em>PrintHood</em></span><span class="sxs-lookup"><span data-stu-id="7cfe0-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="7cfe0-154">Collegamenti agli elementi della cartella della stampante.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cfe0-155"><em>Origini</em></span><span class="sxs-lookup"><span data-stu-id="7cfe0-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="7cfe0-156">Collegamenti ai documenti utilizzati più di recente.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cfe0-157">SendTo</span><span class="sxs-lookup"><span data-stu-id="7cfe0-157">SendTo</span></span></td>
<td><span data-ttu-id="7cfe0-158">Collegamenti ai percorsi a cui l'utente invia spesso i file.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cfe0-159">Menu Start</span><span class="sxs-lookup"><span data-stu-id="7cfe0-159">Start Menu</span></span></td>
<td><span data-ttu-id="7cfe0-160">Voci di menu per il menu <strong>Start</strong> .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cfe0-161"><em>Modelli</em></span><span class="sxs-lookup"><span data-stu-id="7cfe0-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="7cfe0-162">Collegamenti agli elementi del modello.</span><span class="sxs-lookup"><span data-stu-id="7cfe0-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7cfe0-163">Per ottenere il percorso delle sottodirectory di queste directory, usare le funzioni [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) o [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .</span><span class="sxs-lookup"><span data-stu-id="7cfe0-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 



