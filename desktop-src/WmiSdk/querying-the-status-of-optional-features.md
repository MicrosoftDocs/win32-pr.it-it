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
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="7692f-104">Esecuzione di query sullo stato delle funzionalità facoltative</span><span class="sxs-lookup"><span data-stu-id="7692f-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="7692f-105">In Windows 7, WMI ha implementato la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="7692f-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="7692f-106">Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.</span><span class="sxs-lookup"><span data-stu-id="7692f-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="7692f-107">È possibile utilizzare i cmdlet di Windows PowerShell per eseguire una query sullo stato delle funzionalità facoltative.</span><span class="sxs-lookup"><span data-stu-id="7692f-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="7692f-108">Tutti gli esempi in questo argomento usano il cmdlet Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="7692f-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="7692f-109">Per ulteriori informazioni, vedere [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="7692f-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="7692f-110">**Per recuperare tutte le istanze delle funzionalità facoltative presenti in un computer**</span><span class="sxs-lookup"><span data-stu-id="7692f-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7692f-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7692f-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="7692f-112">**Per eseguire una query per una funzionalità facoltativa specificando il nome della funzionalità**</span><span class="sxs-lookup"><span data-stu-id="7692f-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7692f-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7692f-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="7692f-114">La proprietà **Name** distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7692f-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="7692f-115">**Per eseguire una query per le funzionalità facoltative specificando lo stato di installazione**</span><span class="sxs-lookup"><span data-stu-id="7692f-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="7692f-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7692f-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="7692f-117">Per ulteriori informazioni sui possibili valori per la proprietà **InstallState** , vedere [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span><span class="sxs-lookup"><span data-stu-id="7692f-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7692f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7692f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7692f-119">**\_OptionalFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="7692f-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
