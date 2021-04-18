---
title: Diritti di accesso e sicurezza desktop
description: Sicurezza consente di controllare l'accesso agli oggetti desktop. Per ulteriori informazioni sulla sicurezza, vedere Access-Control Model.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399347"
---
# <a name="desktop-security-and-access-rights"></a><span data-ttu-id="fe2ea-104">Diritti di accesso e sicurezza desktop</span><span class="sxs-lookup"><span data-stu-id="fe2ea-104">Desktop Security and Access Rights</span></span>

<span data-ttu-id="fe2ea-105">Sicurezza consente di controllare l'accesso agli oggetti desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-105">Security enables you to control access to desktop objects.</span></span> <span data-ttu-id="fe2ea-106">Per altre informazioni sulla sicurezza, vedere [modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="fe2ea-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="fe2ea-107">È possibile specificare un [descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) per un oggetto desktop quando si chiama la funzione [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) o [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) .</span><span class="sxs-lookup"><span data-stu-id="fe2ea-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a desktop object when you call the [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function.</span></span> <span data-ttu-id="fe2ea-108">Se si specifica NULL, il desktop ottiene un descrittore di sicurezza predefinito.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-108">If you specify NULL, the desktop gets a default security descriptor.</span></span> <span data-ttu-id="fe2ea-109">Gli ACL nel descrittore di sicurezza predefinito per un desktop provengono dalla relativa stazione padre della finestra.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-109">The ACLs in the default security descriptor for a desktop come from its parent window station.</span></span>

<span data-ttu-id="fe2ea-110">Per ottenere o impostare il descrittore di sicurezza di un oggetto della stazione della finestra, chiamare le funzioni [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="fe2ea-110">To get or set the security descriptor of a window station object, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

<span data-ttu-id="fe2ea-111">Quando si chiama la funzione [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) o [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-111">When you call the [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) or [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) function, the system checks the requested access rights against the object's security descriptor.</span></span>

<span data-ttu-id="fe2ea-112">I diritti di accesso validi per gli oggetti desktop includono i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) e alcuni diritti di accesso specifici per gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-112">The valid access rights for desktop objects include the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) and some object-specific access rights.</span></span> <span data-ttu-id="fe2ea-113">La tabella seguente elenca i diritti di accesso standard usati da tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-113">The following table lists the standard access rights used by all objects.</span></span>

| <span data-ttu-id="fe2ea-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fe2ea-114">Value</span></span>                       | <span data-ttu-id="fe2ea-115">Significato</span><span class="sxs-lookup"><span data-stu-id="fe2ea-115">Meaning</span></span>                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2ea-116">Elimina (0x00010000L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-116">DELETE (0x00010000L)</span></span>        | <span data-ttu-id="fe2ea-117">Obbligatorio per eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-117">Required to delete the object.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fe2ea-118">\_Controllo Read (0x00020000L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-118">READ\_CONTROL (0x00020000L)</span></span> | <span data-ttu-id="fe2ea-119">Obbligatorio per leggere le informazioni nel descrittore di sicurezza per l'oggetto, escluse le informazioni nell'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-119">Required to read information in the security descriptor for the object, not including the information in the SACL.</span></span> <span data-ttu-id="fe2ea-120">Per leggere o scrivere il SACL, è necessario richiedere il diritto di accesso alla sicurezza del sistema di accesso \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fe2ea-120">To read or write the SACL, you must request the ACCESS\_SYSTEM\_SECURITY access right.</span></span> <span data-ttu-id="fe2ea-121">Per ulteriori informazioni, vedere il [diritto di accesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="fe2ea-121">For more information, see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span> |
| <span data-ttu-id="fe2ea-122">Sincronizza (0x00100000L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-122">SYNCHRONIZE (0x00100000L)</span></span>   | <span data-ttu-id="fe2ea-123">Non supportato per oggetti desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-123">Not supported for desktop objects.</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="fe2ea-124">SCRITTURA \_ DAC (0x00040000L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-124">WRITE\_DAC (0x00040000L)</span></span>    | <span data-ttu-id="fe2ea-125">Obbligatorio per modificare l'elenco DACL nel descrittore di sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-125">Required to modify the DACL in the security descriptor for the object.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="fe2ea-126">\_Proprietario scrittura (0x00080000L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-126">WRITE\_OWNER (0x00080000L)</span></span>  | <span data-ttu-id="fe2ea-127">Obbligatorio per modificare il proprietario nel descrittore di sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-127">Required to change the owner in the security descriptor for the object.</span></span>                                                                                                                                                                                                              |



 

<span data-ttu-id="fe2ea-128">Nella tabella seguente sono elencati i diritti di accesso specifici dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-128">The following table lists the object-specific access rights.</span></span>



| <span data-ttu-id="fe2ea-129">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="fe2ea-129">Access right</span></span>                       | <span data-ttu-id="fe2ea-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe2ea-130">Description</span></span>                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2ea-131">DESKTOP \_ CREATEMENU (0x0004L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-131">DESKTOP\_CREATEMENU (0x0004L)</span></span>      | <span data-ttu-id="fe2ea-132">Necessario per creare un menu sul desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-132">Required to create a menu on the desktop.</span></span>                                                   |
| <span data-ttu-id="fe2ea-133">DESKTOP \_ CREATEWINDOW (0x0002L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-133">DESKTOP\_CREATEWINDOW (0x0002L)</span></span>    | <span data-ttu-id="fe2ea-134">Obbligatorio per creare una finestra sul desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-134">Required to create a window on the desktop.</span></span>                                                 |
| <span data-ttu-id="fe2ea-135">\_Enumerazione desktop (0x0040L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-135">DESKTOP\_ENUMERATE (0x0040L)</span></span>       | <span data-ttu-id="fe2ea-136">Obbligatorio per l'enumerazione del desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-136">Required for the desktop to be enumerated.</span></span>                                                  |
| <span data-ttu-id="fe2ea-137">DESKTOP \_ HOOKCONTROL (0x0008L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-137">DESKTOP\_HOOKCONTROL (0x0008L)</span></span>     | <span data-ttu-id="fe2ea-138">Obbligatorio per stabilire uno degli hook di finestra.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-138">Required to establish any of the window hooks.</span></span>                                              |
| <span data-ttu-id="fe2ea-139">DESKTOP \_ JOURNALPLAYBACK (0x0020L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-139">DESKTOP\_JOURNALPLAYBACK (0x0020L)</span></span> | <span data-ttu-id="fe2ea-140">Necessario per eseguire la riproduzione Journal su un desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-140">Required to perform journal playback on a desktop.</span></span>                                          |
| <span data-ttu-id="fe2ea-141">DESKTOP \_ JOURNALRECORD (0x0010L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-141">DESKTOP\_JOURNALRECORD (0x0010L)</span></span>   | <span data-ttu-id="fe2ea-142">Obbligatorio per eseguire la registrazione Journal su un desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-142">Required to perform journal recording on a desktop.</span></span>                                         |
| <span data-ttu-id="fe2ea-143">DESKTOP \_ READOBJECTS (0x0001L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-143">DESKTOP\_READOBJECTS (0x0001L)</span></span>     | <span data-ttu-id="fe2ea-144">Obbligatorio per leggere gli oggetti sul desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-144">Required to read objects on the desktop.</span></span>                                                    |
| <span data-ttu-id="fe2ea-145">DESKTOP \_ SWITCHDESKTOP (0x0100L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-145">DESKTOP\_SWITCHDESKTOP (0x0100L)</span></span>   | <span data-ttu-id="fe2ea-146">Obbligatorio per attivare il desktop mediante la funzione [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) .</span><span class="sxs-lookup"><span data-stu-id="fe2ea-146">Required to activate the desktop using the [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) function.</span></span> |
| <span data-ttu-id="fe2ea-147">DESKTOP \_ WRITEOBJECTS (0x0080L)</span><span class="sxs-lookup"><span data-stu-id="fe2ea-147">DESKTOP\_WRITEOBJECTS (0x0080L)</span></span>    | <span data-ttu-id="fe2ea-148">Obbligatorio per scrivere oggetti sul desktop.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-148">Required to write objects on the desktop.</span></span>                                                   |



 

<span data-ttu-id="fe2ea-149">Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un oggetto desktop contenuto nella stazione finestra interattiva della sessione di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-149">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a desktop object contained in the interactive window station of the user's logon session.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe2ea-150">Diritto di accesso</span><span class="sxs-lookup"><span data-stu-id="fe2ea-150">Access right</span></span></th>
<th><span data-ttu-id="fe2ea-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe2ea-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe2ea-152">GENERIC_READ</span><span class="sxs-lookup"><span data-stu-id="fe2ea-152">GENERIC_READ</span></span></td>
<td><dl> <span data-ttu-id="fe2ea-153">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="fe2ea-153">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="fe2ea-154">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2ea-154">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="fe2ea-155">STANDARD_RIGHTS_READ</span><span class="sxs-lookup"><span data-stu-id="fe2ea-155">STANDARD_RIGHTS_READ</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe2ea-156">GENERIC_WRITE</span><span class="sxs-lookup"><span data-stu-id="fe2ea-156">GENERIC_WRITE</span></span></td>
<td><dl> <span data-ttu-id="fe2ea-157">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="fe2ea-157">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="fe2ea-158">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="fe2ea-158">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="fe2ea-159">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="fe2ea-159">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="fe2ea-160">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="fe2ea-160">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="fe2ea-161">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="fe2ea-161">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="fe2ea-162">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2ea-162">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="fe2ea-163">STANDARD_RIGHTS_WRITE</span><span class="sxs-lookup"><span data-stu-id="fe2ea-163">STANDARD_RIGHTS_WRITE</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe2ea-164">GENERIC_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="fe2ea-164">GENERIC_EXECUTE</span></span></td>
<td><dl> <span data-ttu-id="fe2ea-165">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="fe2ea-165">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="fe2ea-166">STANDARD_RIGHTS_EXECUTE</span><span class="sxs-lookup"><span data-stu-id="fe2ea-166">STANDARD_RIGHTS_EXECUTE</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe2ea-167">GENERIC_ALL</span><span class="sxs-lookup"><span data-stu-id="fe2ea-167">GENERIC_ALL</span></span></td>
<td><dl> <span data-ttu-id="fe2ea-168">DESKTOP_CREATEMENU</span><span class="sxs-lookup"><span data-stu-id="fe2ea-168">DESKTOP_CREATEMENU</span></span><br />
<span data-ttu-id="fe2ea-169">DESKTOP_CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="fe2ea-169">DESKTOP_CREATEWINDOW</span></span><br />
<span data-ttu-id="fe2ea-170">DESKTOP_ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="fe2ea-170">DESKTOP_ENUMERATE</span></span><br />
<span data-ttu-id="fe2ea-171">DESKTOP_HOOKCONTROL</span><span class="sxs-lookup"><span data-stu-id="fe2ea-171">DESKTOP_HOOKCONTROL</span></span><br />
<span data-ttu-id="fe2ea-172">DESKTOP_JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="fe2ea-172">DESKTOP_JOURNALPLAYBACK</span></span><br />
<span data-ttu-id="fe2ea-173">DESKTOP_JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="fe2ea-173">DESKTOP_JOURNALRECORD</span></span><br />
<span data-ttu-id="fe2ea-174">DESKTOP_READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2ea-174">DESKTOP_READOBJECTS</span></span><br />
<span data-ttu-id="fe2ea-175">DESKTOP_SWITCHDESKTOP</span><span class="sxs-lookup"><span data-stu-id="fe2ea-175">DESKTOP_SWITCHDESKTOP</span></span><br />
<span data-ttu-id="fe2ea-176">DESKTOP_WRITEOBJECTS</span><span class="sxs-lookup"><span data-stu-id="fe2ea-176">DESKTOP_WRITEOBJECTS</span></span><br />
<span data-ttu-id="fe2ea-177">STANDARD_RIGHTS_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="fe2ea-177">STANDARD_RIGHTS_REQUIRED</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fe2ea-178">È possibile richiedere il \_ \_ diritto di accesso di sicurezza del sistema di accesso a un oggetto desktop se si desidera leggere o scrivere il SACL dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fe2ea-178">You can request the ACCESS\_SYSTEM\_SECURITY access right to a desktop object if you want to read or write the object's SACL.</span></span> <span data-ttu-id="fe2ea-179">Per altre informazioni, vedere [elenchi di controllo di accesso (ACL)](/windows/desktop/SecAuthZ/access-control-lists) e [accesso SACL diritto](/windows/desktop/SecAuthZ/sacl-access-right).</span><span class="sxs-lookup"><span data-stu-id="fe2ea-179">For more information, see [Access-Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right).</span></span>

 

 