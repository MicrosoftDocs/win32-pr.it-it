---
title: Funzioni di Windows Defender
description: Funzioni chiamate dalle app per richiedere analisi, aggiornamenti delle firme o informazioni da Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398496"
---
# <a name="windows-defender-functions"></a><span data-ttu-id="c2514-103">Funzioni di Windows Defender</span><span class="sxs-lookup"><span data-stu-id="c2514-103">Windows Defender Functions</span></span>

<span data-ttu-id="c2514-104">Funzioni chiamate dalle app per richiedere analisi, aggiornamenti delle firme o informazioni da Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="c2514-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2514-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="c2514-105">Function</span></span></th>
<th><span data-ttu-id="c2514-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2514-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2514-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="c2514-108">Restituisce un messaggio di errore formattato basato su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="c2514-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="c2514-110">Libera la memoria per malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="c2514-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="c2514-112">Chiude l'handle restituito da <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>o <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2514-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="c2514-114">Stabilisce una connessione a malware Protection Manager nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c2514-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="c2514-116"><strong>Non supportato.</strong></span><span class="sxs-lookup"><span data-stu-id="c2514-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="c2514-117">Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="c2514-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="c2514-119">Restituisce informazioni sullo stato dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="c2514-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="c2514-121">Restituisce le informazioni sulla versione dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="c2514-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="c2514-123">Consente il controllo di un'analisi che è stata avviata in modo asincrono tramite <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2514-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="c2514-125">Avvia un'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="c2514-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="c2514-127">Restituisce informazioni sulla minaccia successiva nell'elenco di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c2514-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="c2514-128">Questa funzione può essere chiamata ripetutamente fino al completamento dell'enumerazione di tutte le minacce.</span><span class="sxs-lookup"><span data-stu-id="c2514-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="c2514-130">Restituisce un handle di enumerazione allo scopo di recuperare le minacce.</span><span class="sxs-lookup"><span data-stu-id="c2514-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="c2514-131">Questa funzione può essere utilizzata per aprire le minacce rilevate da un'analisi specifica, tutte le minacce attive nel sistema, la cronologia della disinfezione da minacce o tutte le minacce presenti nel database di firma.</span><span class="sxs-lookup"><span data-stu-id="c2514-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="c2514-133">Utilizzato per eseguire una query su una particolare minaccia, ad esempio la gravità e la categoria, o localizzata, ad esempio una descrizione della categoria e consigli.</span><span class="sxs-lookup"><span data-stu-id="c2514-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="c2514-135">Consente il controllo di un'operazione di aggiornamento della firma avviata in modo asincrono tramite <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c2514-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="c2514-137">Avvia un'operazione di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="c2514-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2514-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="c2514-139">Modifica lo stato di Windows Defender su on o off.</span><span class="sxs-lookup"><span data-stu-id="c2514-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c2514-140">A partire da Windows 10, versione 1607 e Windows Server 2016, la funzione <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> restituisce sempre <strong>E_NOTIMPL</strong>.</span><span class="sxs-lookup"><span data-stu-id="c2514-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2514-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2514-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="c2514-142">Restituisce lo stato corrente di Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="c2514-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





