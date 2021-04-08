---
description: Durante un aggiornamento del computer o una migrazione da computer a computer, verrà eseguita la migrazione dei certificati in determinati archivi certificati.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migrazione dell'archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058025"
---
# <a name="certificate-store-migration"></a>Migrazione dell'archivio certificati

Durante un aggiornamento del computer o una migrazione da computer a computer, verrà eseguita la migrazione dei certificati in determinati archivi certificati. Nella tabella seguente sono elencati gli archivi certificati per i quali viene eseguita la migrazione per impostazione predefinita. Per l'archivio impostazioni richiesta di certificato (ACRS) di sistema, viene eseguita la migrazione solo degli [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti). Per tutti gli altri archivi elencati di seguito, vengono migrati solo i certificati.

<table>
<thead>
<tr class="header">
<th>Sistema/utente</th>
<th>Archivio</th>
<th>Posizione di archiviazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$ {ROWSPAN8} $System $ {REMOVE} $<br />
</td>
<td>RADICE</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Radice</strong> \ <strong>Certificati</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>My</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>RICHIESTA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Richiesta</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>Non consentita</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>consentito</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>ACRS</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>Scopi consentiti</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">Utente $ {REMOVE} $<br />
</td>
<td>RADICE</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Radice</strong> \ <strong>Certificati</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>file: \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>RICHIESTA</td>
<td>file: \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="even">
<td>Non consentita</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Non <strong>consentito</strong> \ <strong>Certificati</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ di <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>CA</strong> \ <strong>Certificati</strong><br/></td>

</tr>
</tbody>
</table>



 

Per impostazione predefinita, non viene eseguita la migrazione di altri archivi certificati creati dalle applicazioni. Le applicazioni che creano i propri archivi sono responsabili della migrazione degli archivi creati. Per creare archivi, è consigliabile definire una chiave del registro di sistema nelle impostazioni dell'applicazione e creare un archivio all'interno delle impostazioni del registro di sistema usando il provider **CERT \_ Store prove \_ \_ reg** Store. Per ulteriori informazioni sulla migrazione delle impostazioni dell'applicazione, vedere l'argomento *How to create an Custom. xml file* nella Guida *using USMT 3,0* all' [utilità di migrazione stato utente 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.

 

 
