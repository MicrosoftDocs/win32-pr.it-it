---
title: Diritti di accesso e sicurezza di Windows Station
description: Sicurezza consente di controllare l'accesso agli oggetti di Windows Station. Per ulteriori informazioni sulla sicurezza, vedere Access-Control Model.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299880"
---
# <a name="window-station-security-and-access-rights"></a><span data-ttu-id="3d13e-104">Diritti di accesso e sicurezza di Windows Station</span><span class="sxs-lookup"><span data-stu-id="3d13e-104">Window Station Security and Access Rights</span></span>

<span data-ttu-id="3d13e-105">Sicurezza consente di controllare l'accesso agli oggetti di Windows Station.</span><span class="sxs-lookup"><span data-stu-id="3d13e-105">Security enables you to control access to window station objects.</span></span> <span data-ttu-id="3d13e-106">Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="3d13e-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="3d13e-107">È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un oggetto della stazione della finestra quando si chiama la funzione [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) .</span><span class="sxs-lookup"><span data-stu-id="3d13e-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a window station object when you call the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function.</span></span> <span data-ttu-id="3d13e-108">Se si specifica NULL, la finestra stazione ottiene un descrittore di sicurezza predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d13e-108">If you specify NULL, the window station gets a default security descriptor.</span></span> <span data-ttu-id="3d13e-109">Gli ACL nel descrittore di sicurezza predefinito per una stazione della finestra provengono dal token primario o di rappresentazione del creatore.</span><span class="sxs-lookup"><span data-stu-id="3d13e-109">The ACLs in the default security descriptor for a window station come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="3d13e-110">Per ottenere o impostare il descrittore di sicurezza di un oggetto della stazione della finestra, chiamare le funzioni [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="3d13e-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="3d13e-111">Quando si chiama la funzione [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d13e-111">When you call the [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="3d13e-112">I diritti di accesso validi per gli oggetti Window Station includono i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) e alcuni diritti di accesso specifici per gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="3d13e-112">The valid access rights for window station objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="3d13e-113">La tabella seguente elenca i diritti di accesso standard usati da tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="3d13e-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="3d13e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="3d13e-114">Value</span></span>                       | <span data-ttu-id="3d13e-115">Significato</span><span class="sxs-lookup"><span data-stu-id="3d13e-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d13e-116">Elimina (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="3d13e-117">Obbligatorio per eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d13e-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3d13e-118">\_Controllo Read (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="3d13e-119">Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, escluse le informazioni nell'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="3d13e-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="3d13e-120">Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso alla sicurezza del sistema di accesso \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3d13e-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="3d13e-121">Per ulteriori informazioni, vedere il [diritto di accesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="3d13e-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="3d13e-122">Sincronizza (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="3d13e-123">Non supportato per gli oggetti di Windows Station.</span><span class="sxs-lookup"><span data-stu-id="3d13e-123">Not supported for window station objects.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="3d13e-124">SCRITTURA \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="3d13e-125">Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d13e-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="3d13e-126">\_Proprietario scrittura (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="3d13e-127">Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d13e-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="3d13e-128">Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3d13e-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="3d13e-129">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="3d13e-129">Access right</span></span>                        | <span data-ttu-id="3d13e-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d13e-130">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d13e-131">WINSTA \_ tutti gli \_ accessi (0x37F)</span><span class="sxs-lookup"><span data-stu-id="3d13e-131">WINSTA\_ALL\_ACCESS (0x37F)</span></span>         | <span data-ttu-id="3d13e-132">Tutti i diritti di accesso possibili per la stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d13e-132">All possible access rights for the window station.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="3d13e-133">WINSTA \_ ACCESSCLIPBOARD (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-133">WINSTA\_ACCESSCLIPBOARD (0x0004L)</span></span>   | <span data-ttu-id="3d13e-134">Obbligatorio per utilizzare gli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3d13e-134">Required to use the clipboard.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="3d13e-135">WINSTA \_ ACCESSGLOBALATOMS (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-135">WINSTA\_ACCESSGLOBALATOMS (0x0020L)</span></span> | <span data-ttu-id="3d13e-136">Obbligatorio per modificare gli atomi globali.</span><span class="sxs-lookup"><span data-stu-id="3d13e-136">Required to manipulate global atoms.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="3d13e-137">WINSTA \_ CREATEDESKTOP (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-137">WINSTA\_CREATEDESKTOP (0x0008L)</span></span>     | <span data-ttu-id="3d13e-138">Obbligatorio per creare nuovi oggetti desktop sulla stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d13e-138">Required to create new desktop objects on the window station.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="3d13e-139">WINSTA \_ ENUMDESKTOPS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-139">WINSTA\_ENUMDESKTOPS (0x0001L)</span></span>      | <span data-ttu-id="3d13e-140">Obbligatorio per enumerare gli oggetti desktop esistenti.</span><span class="sxs-lookup"><span data-stu-id="3d13e-140">Required to enumerate existing desktop objects.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3d13e-141">\_Enumerazione winsta (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-141">WINSTA\_ENUMERATE (0x0100L)</span></span>         | <span data-ttu-id="3d13e-142">Obbligatorio perché la stazione della finestra venga enumerata.</span><span class="sxs-lookup"><span data-stu-id="3d13e-142">Required for the window station to be enumerated.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="3d13e-143">WINSTA \_ EXITWINDOWS (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-143">WINSTA\_EXITWINDOWS (0x0040L)</span></span>       | <span data-ttu-id="3d13e-144">Obbligatorio per chiamare correttamente la funzione [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="3d13e-144">Required to successfully call the [**ExitWindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span> <span data-ttu-id="3d13e-145">Le stazioni della finestra possono essere condivise dagli utenti e questo tipo di accesso può impedire ad altri utenti di una stazione di finestra di disconnettersi dal proprietario della stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d13e-145">Window stations can be shared by users and this access type can prevent other users of a window station from logging off the window station owner.</span></span> |
| <span data-ttu-id="3d13e-146">WINSTA \_ diritti ReadAttributes (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-146">WINSTA\_READATTRIBUTES (0x0002L)</span></span>    | <span data-ttu-id="3d13e-147">Obbligatorio per leggere gli attributi di un oggetto della stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d13e-147">Required to read the attributes of a window station object.</span></span> <span data-ttu-id="3d13e-148">Questo attributo include le impostazioni relative ai colori e ad altre proprietà della stazione della finestra globale.</span><span class="sxs-lookup"><span data-stu-id="3d13e-148">This attribute includes color settings and other global window station properties.</span></span>                                                                                                                                |
| <span data-ttu-id="3d13e-149">WINSTA \_ READSCREEN (0x0200L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-149">WINSTA\_READSCREEN (0x0200L)</span></span>        | <span data-ttu-id="3d13e-150">Obbligatorio per accedere al contenuto della schermata.</span><span class="sxs-lookup"><span data-stu-id="3d13e-150">Required to access screen contents.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="3d13e-151">WINSTA \_ WRITEATTRIBUTES (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="3d13e-151">WINSTA\_WRITEATTRIBUTES (0x0010L)</span></span>   | <span data-ttu-id="3d13e-152">Obbligatorio per modificare gli attributi di un oggetto della stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d13e-152">Required to modify the attributes of a window station object.</span></span> <span data-ttu-id="3d13e-153">Gli attributi includono impostazioni colore e altre proprietà globali della stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="3d13e-153">The attributes include color settings and other global window station properties.</span></span>                                                                                                                               |



 

<span data-ttu-id="3d13e-154">Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per l'oggetto Interactive Window Station, ovvero la stazione della finestra assegnata alla sessione di accesso dell'utente interattivo.</span><span class="sxs-lookup"><span data-stu-id="3d13e-154">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the interactive window station object, which is the window station assigned to the logon session of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3d13e-155">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="3d13e-155">Access right</span></span></th>
<th><span data-ttu-id="3d13e-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d13e-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d13e-157">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="3d13e-157">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="3d13e-158">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="3d13e-158">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="3d13e-159">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="3d13e-159">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="3d13e-160">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="3d13e-160">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="3d13e-161">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3d13e-161">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="3d13e-162">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="3d13e-162">WINSTA_READSCREEN</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d13e-163">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="3d13e-163">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="3d13e-164">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="3d13e-164">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="3d13e-165">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="3d13e-165">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="3d13e-166">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="3d13e-166">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="3d13e-167">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3d13e-167">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d13e-168">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="3d13e-168">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="3d13e-169">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="3d13e-169">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="3d13e-170">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="3d13e-170">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="3d13e-171">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="3d13e-171">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d13e-172">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="3d13e-172">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="3d13e-173">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="3d13e-173">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="3d13e-174">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="3d13e-174">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="3d13e-175">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="3d13e-175">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="3d13e-176">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="3d13e-176">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="3d13e-177">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="3d13e-177">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="3d13e-178">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="3d13e-178">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="3d13e-179">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="3d13e-179">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="3d13e-180">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3d13e-180">WINSTA_READATTRIBUTES</span></span><br />
<span data-ttu-id="3d13e-181">WINSTA_READSCREEN</span><span class="sxs-lookup"><span data-stu-id="3d13e-181">WINSTA_READSCREEN</span></span><br />
<span data-ttu-id="3d13e-182">WINSTA_WRITEATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3d13e-182">WINSTA_WRITEATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d13e-183">Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un oggetto finestra stazione non interattiva.</span><span class="sxs-lookup"><span data-stu-id="3d13e-183">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a noninteractive window station object.</span></span> <span data-ttu-id="3d13e-184">Il sistema assegna stazioni della finestra non interattive a tutte le sessioni di accesso diverse da quelle dell'utente interattivo.</span><span class="sxs-lookup"><span data-stu-id="3d13e-184">The system assigns noninteractive window stations to all logon sessions other than that of the interactive user.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3d13e-185">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="3d13e-185">Access right</span></span></th>
<th><span data-ttu-id="3d13e-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d13e-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d13e-187">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="3d13e-187">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="3d13e-188">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="3d13e-188">STANDARD_RIGHTS_READ</span></span><br />
<span data-ttu-id="3d13e-189">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="3d13e-189">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="3d13e-190">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="3d13e-190">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="3d13e-191">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3d13e-191">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d13e-192">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="3d13e-192">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="3d13e-193">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="3d13e-193">STANDARD_RIGHTS_WRITE</span></span><br />
<span data-ttu-id="3d13e-194">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="3d13e-194">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="3d13e-195">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="3d13e-195">WINSTA_CREATEDESKTOP</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d13e-196">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="3d13e-196">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="3d13e-197">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="3d13e-197">STANDARD_RIGHTS_EXECUTE</span></span><br />
<span data-ttu-id="3d13e-198">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="3d13e-198">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="3d13e-199">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="3d13e-199">WINSTA_EXITWINDOWS</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d13e-200">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="3d13e-200">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="3d13e-201">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="3d13e-201">STANDARD_RIGHTS_REQUIRED</span></span><br />
<span data-ttu-id="3d13e-202">WINSTA_ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="3d13e-202">WINSTA_ACCESSCLIPBOARD</span></span><br />
<span data-ttu-id="3d13e-203">WINSTA_ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="3d13e-203">WINSTA_ACCESSGLOBALATOMS</span></span><br />
<span data-ttu-id="3d13e-204">WINSTA_CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="3d13e-204">WINSTA_CREATEDESKTOP</span></span><br />
<span data-ttu-id="3d13e-205">WINSTA_ENUMDESKTOPS</span><span class="sxs-lookup"><span data-stu-id="3d13e-205">WINSTA_ENUMDESKTOPS</span></span><br />
<span data-ttu-id="3d13e-206">WINSTA_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="3d13e-206">WINSTA_ENUMERATE</span></span><br />
<span data-ttu-id="3d13e-207">WINSTA_EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="3d13e-207">WINSTA_EXITWINDOWS</span></span><br />
<span data-ttu-id="3d13e-208">WINSTA_READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3d13e-208">WINSTA_READATTRIBUTES</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d13e-209">\_ \_ Se si desidera leggere o scrivere il SACL dell'oggetto, è possibile richiedere il diritto di accesso alla sicurezza del sistema di accesso a un oggetto di Windows Station.</span><span class="sxs-lookup"><span data-stu-id="3d13e-209">You can request the ACCESS\_SYSTEM\_SECURITY access right to a window station object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="3d13e-210">Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [accesso SACL diritto](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="3d13e-210">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 