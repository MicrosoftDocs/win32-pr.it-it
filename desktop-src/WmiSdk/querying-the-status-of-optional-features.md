---
description: In Windows 7, WMI ha implementato la \_ classe Win32 OptionalFeature. Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Esecuzione di query sullo stato delle funzionalità facoltative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755335"
---
# <a name="querying-the-status-of-optional-features"></a>Esecuzione di query sullo stato delle funzionalità facoltative

In Windows 7, WMI ha implementato la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.

È possibile utilizzare i cmdlet di Windows PowerShell per eseguire una query sullo stato delle funzionalità facoltative. Tutti gli esempi in questo argomento usano il cmdlet Get-WmiObject. Per ulteriori informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Per recuperare tutte le istanze delle funzionalità facoltative presenti in un computer**

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
    > La proprietà **Name** distingue tra maiuscole e minuscole.

     

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

    

    Per ulteriori informazioni sui possibili valori per la proprietà **InstallState** , vedere [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_OptionalFeature Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
