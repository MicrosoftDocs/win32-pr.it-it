---
description: Durante un aggiornamento del computer o una migrazione da computer a computer, verrà eseguita la migrazione dei certificati in determinati archivi certificati.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migrazione dell'archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de694fc24433ce8db039dd677f52935da70cbf07d0a719b0871bd1e8f4b2d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771097"
---
# <a name="certificate-store-migration"></a>Migrazione dell'archivio certificati

Durante un aggiornamento del computer o una migrazione da computer a computer, verrà eseguita la migrazione dei certificati in determinati archivi certificati. Nella tabella seguente sono elencati gli archivi certificati di cui viene eseguita la migrazione per impostazione predefinita. Per l'archivio ACRS (Automatic Certificate Request Impostazioni) [](../secgloss/c-gly.md) di sistema, viene eseguita la migrazione solo degli elenchi di certificati attendibili (CCL). Per tutti gli altri archivi elencati di seguito, viene eseguita la migrazione solo dei certificati.

<table>
<thead>
<tr class="header">
<th>Sistema/utente</th>
<th>Archiviazione</th>
<th>Posizione di archiviazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>${ROWSPAN8}$System${REMOVE}$<br />
</td>
<td>RADICE</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Radice</strong> \ <strong>Certificati</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>My</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>Richiesta</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Richiesta</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>Non consentita</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Non consentito</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>ACRS</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CTE</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">User${REMOVE}$<br />
</td>
<td>RADICE</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Radice</strong> \ <strong>Certificati</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>file: \\ %APPDATA%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>Richiesta</td>
<td>file: \\ %APPDATA%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>Non consentita</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Non consentito</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificati</strong><br/></td>

</tr>
</tbody>
</table>



 

Gli altri archivi certificati creati dalle applicazioni non vengono migrati per impostazione predefinita. Le applicazioni che creano i propri archivi sono responsabili della migrazione degli archivi creati. Per creare archivi, è consigliabile definire una chiave del Registro di sistema nelle impostazioni dell'applicazione e creare un archivio all'interno delle impostazioni del Registro di sistema usando il provider di archivi **\_ REG CERT STORE \_ PROV. \_** Per altre informazioni sulla migrazione delle impostazioni dell'applicazione, vedere l'argomento *How To Create a Custom .xml File* nella guida Using USMT 3.0 (Uso di *USMT 3.0)* [Utilità di migrazione stato utente 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). Questa risorsa potrebbe non essere disponibile in alcune lingue, paesi o aree geografiche.

 

 
