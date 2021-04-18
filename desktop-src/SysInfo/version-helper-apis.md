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
# <a name="version-helper-functions"></a><span data-ttu-id="93135-103">Funzioni helper versione</span><span class="sxs-lookup"><span data-stu-id="93135-103">Version Helper functions</span></span>

<span data-ttu-id="93135-104">Le funzioni seguenti possono essere utilizzate per determinare la versione corrente del sistema operativo o per stabilire se si tratta di una versione di Windows o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="93135-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="93135-105">Queste funzioni forniscono semplici test che usano la funzione [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) e i confronti consigliati maggiori o uguali a quelli che sono stati comprovati come mezzi affidabili per determinare la versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="93135-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="93135-106">Queste API sono definite da **versionhelpers. h**, incluso nel Software Development Kit Windows 8.1 (SDK).</span><span class="sxs-lookup"><span data-stu-id="93135-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="93135-107">Questo file può essere usato con altre versioni di Microsoft Visual Studio per implementare la stessa funzionalità per le versioni di Windows precedenti al Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="93135-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="93135-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="93135-108">Function</span></span></th>
<th><span data-ttu-id="93135-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93135-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93135-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-111">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP.</span><span class="sxs-lookup"><span data-stu-id="93135-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-113">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="93135-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93135-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-115">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="93135-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-117">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows XP con Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="93135-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93135-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-119">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="93135-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-121">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="93135-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93135-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-123">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows Vista con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="93135-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-125">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="93135-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93135-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-127">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows 7 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="93135-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-129">Indica se la versione corrente del sistema operativo corrisponde, o è maggiore di, la versione di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="93135-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93135-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-131">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione del Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="93135-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="93135-132">Per Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> restituisce false, a meno che l'applicazione non contenga un manifesto che include una sezione di compatibilità contenente i GUID che definiscono Windows 8.1 e/o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="93135-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="93135-134">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, la versione di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="93135-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="93135-135">Per Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> restituisce false, a meno che l'applicazione non contenga un manifesto che include una sezione di compatibilità che contiene il GUID che designa Windows 10.</span><span class="sxs-lookup"><span data-stu-id="93135-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93135-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="93135-137">Indica se il sistema operativo corrente è una versione di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="93135-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="93135-138">Le applicazioni che devono distinguere tra le versioni server e client di Windows devono chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="93135-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93135-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="93135-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="93135-140">Utilizzare questa funzione solo se le altre funzioni di supporto della versione fornite non rientrano nello scenario.</span><span class="sxs-lookup"><span data-stu-id="93135-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="93135-141">Indica se la versione corrente del sistema operativo corrisponde o è maggiore di, le informazioni sulla versione fornite.</span><span class="sxs-lookup"><span data-stu-id="93135-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="93135-142">Questa funzione è utile per confermare una versione di Windows Server che non condivide un numero di versione con una versione client.</span><span class="sxs-lookup"><span data-stu-id="93135-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="93135-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="93135-143">Example</span></span>

<span data-ttu-id="93135-144">Le funzioni inline definite nel file di intestazione **VersionHelpers. h** consentono di verificare la versione del sistema operativo restituendo un valore **booleano** durante il test di una versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="93135-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="93135-145">Se, ad esempio, l'applicazione richiede Windows 8 o versione successiva, usare il test seguente.</span><span class="sxs-lookup"><span data-stu-id="93135-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="93135-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93135-146">Related topics</span></span>

- [<span data-ttu-id="93135-147">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="93135-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
