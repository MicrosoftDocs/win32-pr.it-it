---
description: Le funzioni seguenti possono essere usate per determinare la versione corrente del sistema operativo o identificare se si tratta di una versione Windows o Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Funzioni dell'helper versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7156070e9c793e537d976c82a632142e04cd6669b110b7d0b9fc8da95671b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884172"
---
# <a name="version-helper-functions"></a>Funzioni dell'helper versione

Le funzioni seguenti possono essere usate per determinare la versione corrente del sistema operativo o identificare se si tratta di una versione Windows o Windows Server. Queste funzioni forniscono test semplici che usano la funzione [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) e i confronti consigliati maggiori o uguali a quelli dimostrati come strumenti affidabili per determinare la versione del sistema operativo.

> [!Note]  
> Queste API sono definite da **versionhelpers.h,** incluso in Windows 8.1 Software Development Kit (SDK). Questo file può essere usato con altre versioni Microsoft Visual Studio per implementare la stessa funzionalità per Windows versioni precedenti Windows 8.1.

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
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows versione XP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows XP con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows XP con Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows XP con Service Pack 3 (SP3).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore della versione Windows Vista.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows Vista con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows Vista con Service Pack 2 (SP2).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows versione 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows 7 con Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows 8 versione corrente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows 8.1 versione corrente.<br/> Ad Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> restituisce false a meno che l'applicazione non contenga un manifesto che include una sezione di compatibilità che contiene i GUID che designano Windows 8.1 e/o Windows 10.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></td>
<td>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di Windows 10 versione corrente.<br/> Ad Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> restituisce false a meno che l'applicazione non contenga un manifesto che include una sezione di compatibilità che contiene il GUID che definisce Windows 10.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></td>
<td>Indica se il sistema operativo corrente è una versione Windows Server. Le applicazioni che devono distinguere tra le versioni server e client Windows chiamare questa funzione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></td>
<td>
<blockquote>È consigliabile usare questa funzione solo se le altre funzioni dell'helper di versione fornite non sono adatte allo scenario.</blockquote>
<br/>Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, le informazioni sulla versione fornite. Questa funzione è utile per confermare una versione di Windows Server che non condivide un numero di versione con una versione client.
</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Esempio

Le funzioni inline definite nel file di intestazione **VersionHelpers.h** consentono di  verificare la versione del sistema operativo restituisce un valore booleano durante il test di una versione di Windows.

Ad esempio, se l'applicazione richiede Windows 8 versione successiva, usare il test seguente.

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a>Argomenti correlati

- [OSVERSIONINFOEX](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
