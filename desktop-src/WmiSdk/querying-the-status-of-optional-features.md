---
description: In Windows 7 WMI ha implementato la classe \_ OptionalFeature Win32. Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Esecuzione di query sullo stato delle funzionalità facoltative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecffe6ddbe9b860c6f49fe12d3fed500c169bef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476707"
---
# <a name="querying-the-status-of-optional-features"></a>Esecuzione di query sullo stato delle funzionalità facoltative

In Windows 7 WMI ha implementato la [**classe \_ OptionalFeature Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.

È possibile usare Windows PowerShell cmdlet per eseguire query sullo stato delle funzionalità facoltative. Tutti gli esempi in questo argomento usano il cmdlet Get-WmiObject. Per altre informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Per recuperare tutte le istanze di funzionalità facoltative presenti in un computer**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**Per eseguire una query per una funzionalità facoltativa specificando il nome della funzionalità**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**Per eseguire una query per le funzionalità facoltative specificando lo stato di installazione**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
