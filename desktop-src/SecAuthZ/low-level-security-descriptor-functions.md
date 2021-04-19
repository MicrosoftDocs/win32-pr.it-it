---
description: Funzioni per l'impostazione e il recupero di un descrittore di sicurezza degli oggetti.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Funzioni descrittore di sicurezza di basso livello '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319398"
---
# <a name="low-level-security-descriptor-functions"></a><span data-ttu-id="d9dab-103">Funzioni descrittore di sicurezza di basso livello </span><span class="sxs-lookup"><span data-stu-id="d9dab-103">Low-level Security Descriptor Functions</span></span>

<span data-ttu-id="d9dab-104">Sono disponibili diverse coppie di funzioni di basso livello per l'impostazione e il recupero del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d9dab-104">There are several pairs of low-level functions for setting and retrieving an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="d9dab-105">Ognuna di queste coppie funziona solo con un set limitato di oggetti di Windows.</span><span class="sxs-lookup"><span data-stu-id="d9dab-105">Each of these pairs works only with a limited set of Windows objects.</span></span> <span data-ttu-id="d9dab-106">Ad esempio, una coppia funziona con gli oggetti file e l'altra funziona con le chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d9dab-106">For example, one pair works with file objects and another works with registry keys.</span></span> <span data-ttu-id="d9dab-107">Nella tabella seguente vengono illustrate le funzioni di basso livello da utilizzare con i diversi tipi di oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="d9dab-107">The following table shows the low-level functions to use with the different types of securable objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9dab-108">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="d9dab-108">Object type</span></span></th>
<th><span data-ttu-id="d9dab-109">Funzioni di basso livello</span><span class="sxs-lookup"><span data-stu-id="d9dab-109">Low-level functions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d9dab-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">File</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-110"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Files</a></span></span></li>
<li><span data-ttu-id="d9dab-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directory</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-111"><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directories</a></span></span></li>
<li><span data-ttu-id="d9dab-112">Mailslot</span><span class="sxs-lookup"><span data-stu-id="d9dab-112">Mailslots</span></span></li>
<li><span data-ttu-id="d9dab-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipe</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-113"><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipes</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-114">Usare le funzioni <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> e <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-114">Use the <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> and <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> functions.</span></span> <span data-ttu-id="d9dab-115">Queste funzioni utilizzano stringhe di caratteri per identificare l'oggetto a protezione diretta anziché utilizzare gli handle.</span><span class="sxs-lookup"><span data-stu-id="d9dab-115">These functions use character strings to identify the securable object, instead of using handles.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="d9dab-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processi</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-116"><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processes</a></span></span></li>
<li><span data-ttu-id="d9dab-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-117"><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></span></span></li>
<li><span data-ttu-id="d9dab-118"><a href="access-rights-for-access-token-objects.md">Token di accesso</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-118"><a href="access-rights-for-access-token-objects.md">Access tokens</a></span></span></li>
<li><span data-ttu-id="d9dab-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Oggetti di mapping di file</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-119"><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File-mapping objects</a></span></span></li>
<li><span data-ttu-id="d9dab-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semafori</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-120"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphores</a></span></span></li>
<li><span data-ttu-id="d9dab-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventi</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-121"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Events</a></span></span></li>
<li><span data-ttu-id="d9dab-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutex</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-122"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></span></span></li>
<li><span data-ttu-id="d9dab-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Timer in attesa</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-123"><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Waitable timers</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-124">Usare le funzioni <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-124">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d9dab-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Stazioni finestra</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-125"><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window stations</a></span></span></li>
<li><span data-ttu-id="d9dab-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-126"><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-127">Usare le funzioni <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-127">Use the <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="d9dab-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Chiavi del Registro di sistema</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-128"><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry keys</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-129">Usare le funzioni <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> e <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-129">Use the <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> and <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d9dab-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Oggetti servizio Windows</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-130"><a href="/windows/desktop/Services/service-security-and-access-rights">Windows service objects</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-131">Usare le funzioni <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-131">Use the <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> and <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="d9dab-132">Oggetti Printer</span><span class="sxs-lookup"><span data-stu-id="d9dab-132">Printer objects</span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-133">Utilizzare la struttura <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> con le funzioni <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> e <a href="/windows/desktop/printdocs/setprinter"><strong>seprinter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-133">Use the <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> structure with the <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> and <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> functions.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d9dab-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Condivisioni di rete</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-134"><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Network shares</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-135">Usare il livello 502 con le funzioni <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> e <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-135">Use level 502 with the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> and <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> functions.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="d9dab-136"><a href="acl-based-access-control.md">Oggetti privati (oggetti privati dell'applicazione di creazione)</a></span><span class="sxs-lookup"><span data-stu-id="d9dab-136"><a href="acl-based-access-control.md">Private objects (objects private to the creating application)</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d9dab-137">Usare le funzioni <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9dab-137">Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> functions.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
