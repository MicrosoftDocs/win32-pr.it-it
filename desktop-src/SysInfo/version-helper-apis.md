---
description: Le funzioni seguenti possono essere utilizzate per determinare la versione corrente del sistema operativo o per stabilire se si tratta di una versione di Windows o Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Funzioni helper versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/23/2021
ms.locfileid: "106333987"
---
# <a name="version-helper-functions"></a>Funzioni helper versione

Le funzioni seguenti possono essere utilizzate per determinare la versione corrente del sistema operativo o per stabilire se si tratta di una versione di Windows o Windows Server. Queste funzioni forniscono semplici test che usano la funzione [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) e i confronti consigliati maggiori o uguali a quelli che sono stati comprovati come mezzi affidabili per determinare la versione del sistema operativo.

> [!Note]  
> Queste API sono definite da **versionhelpers. h**, incluso nel Software Development Kit Windows 8.1 (SDK). Questo file può essere usato con altre versioni di Microsoft Visual Studio per implementare la stessa funzionalità per le versioni di Windows precedenti al Windows 8.1.

<table>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP con Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP con Service Pack 3 (SP3).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows Vista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows Vista con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows Vista con Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows 7 con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde, o è maggiore di, la versione di Windows 8.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione del Windows 8.1.<br/> Per Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> restituisce false, a meno che l'applicazione non contenga un manifesto che include una sezione di compatibilità contenente i GUID che definiscono Windows 8.1 e/o Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows 10.<br/> Per Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> restituisce false, a meno che l'applicazione non contenga un manifesto che include una sezione di compatibilità che contiene il GUID che designa Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>Indica se il sistema operativo corrente è una versione di Windows Server. Le applicazioni che devono distinguere tra le versioni server e client di Windows devono chiamare questa funzione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>Utilizzare questa funzione solo se le altre funzioni di supporto della versione fornite non rientrano nello scenario.</blockquote>
<br/>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, le informazioni sulla versione fornite. Questa funzione è utile per confermare una versione di Windows Server che non condivide un numero di versione con una versione client.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Esempio

Le funzioni inline definite nel file di intestazione **VersionHelpers. h** consentono di verificare la versione del sistema operativo restituendo un valore **booleano** durante il test di una versione di Windows.

Se, ad esempio, l'applicazione richiede Windows 8 o versione successiva, usare il test seguente.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Argomenti correlati

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
