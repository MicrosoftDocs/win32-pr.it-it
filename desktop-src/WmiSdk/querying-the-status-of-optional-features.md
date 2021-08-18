---
description: In Windows 7 WMI ha implementato la classe \_ OptionalFeature Win32. Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Esecuzione di query sullo stato delle funzionalità facoltative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996031"
---
# <a name="querying-the-status-of-optional-features"></a>Esecuzione di query sullo stato delle funzionalità facoltative

In Windows 7 WMI ha implementato la [**classe \_ OptionalFeature Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.

È possibile usare Windows PowerShell cmdlet per eseguire query sullo stato delle funzionalità facoltative. Tutti gli esempi in questo argomento usano il cmdlet Get-WmiObject. Per altre informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Per recuperare tutte le istanze di funzionalità facoltative presenti in un computer**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**Per eseguire una query per una funzionalità facoltativa specificando il nome della funzionalità**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > La **proprietà name** fa distinzione tra maiuscole e minuscole.

     

**Per eseguire una query per le funzionalità facoltative specificando lo stato di installazione**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    Per altre informazioni sui valori possibili per la **proprietà InstallState,** vedere [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
