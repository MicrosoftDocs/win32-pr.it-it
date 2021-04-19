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
# <a name="low-level-security-descriptor-functions"></a>Funzioni descrittore di sicurezza di basso livello 

Sono disponibili diverse coppie di funzioni di basso livello per l'impostazione e il recupero del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)di un oggetto. Ognuna di queste coppie funziona solo con un set limitato di oggetti di Windows. Ad esempio, una coppia funziona con gli oggetti file e l'altra funziona con le chiavi del registro di sistema. Nella tabella seguente vengono illustrate le funzioni di basso livello da utilizzare con i diversi tipi di oggetti a protezione diretta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di oggetto</th>
<th>Funzioni di basso livello</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">File</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Directory</a></li>
<li>Mailslot</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named pipe</a></li>
</ul></td>
<td>Usare le funzioni <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> e <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> . Queste funzioni utilizzano stringhe di caratteri per identificare l'oggetto a protezione diretta anziché utilizzare gli handle.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processi</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread</a></li>
<li><a href="access-rights-for-access-token-objects.md">Token di accesso</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Oggetti di mapping di file</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semafori</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventi</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutex</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Timer in attesa</a></li>
</ul></td>
<td>Usare le funzioni <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Stazioni finestra</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop</a></li>
</ul></td>
<td>Usare le funzioni <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Chiavi del Registro di sistema</a></li>
</ul></td>
<td>Usare le funzioni <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> e <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Oggetti servizio Windows</a></li>
</ul></td>
<td>Usare le funzioni <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li>Oggetti Printer</li>
</ul></td>
<td>Utilizzare la struttura <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> con le funzioni <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> e <a href="/windows/desktop/printdocs/setprinter"><strong>seprinter</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Condivisioni di rete</a></li>
</ul></td>
<td>Usare il livello 502 con le funzioni <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> e <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">Oggetti privati (oggetti privati dell'applicazione di creazione)</a></li>
</ul></td>
<td>Usare le funzioni <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</td>
</tr>
</tbody>
</table>



 

 

 
