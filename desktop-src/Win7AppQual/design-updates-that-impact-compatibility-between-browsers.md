---
description: Progettare aggiornamenti che influiscono sulla compatibilità tra browser
ms.assetid: F2C13FEC-5537-4B0D-BFDB-E17A42A289CB
title: Progettare aggiornamenti che influiscono sulla compatibilità tra browser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a306a64cb03bce8b466f6367339302522109619a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088479"
---
# <a name="design-updates-that-impact-compatibility-between-browsers"></a><span data-ttu-id="958e5-103">Progettare aggiornamenti che influiscono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="958e5-103">Design Updates that Impact Compatibility between Browsers</span></span>

<span data-ttu-id="958e5-104">Questa sezione e la tabella seguente illustrano le quattro principali aree di compatibilità (non in ordine di incidenza o di classificazione della priorità).</span><span class="sxs-lookup"><span data-stu-id="958e5-104">This section and the following table show the four major areas of compatibility (not in order of incidence or ranking of priority).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="958e5-105">Modifiche da Internet Explorer 6 a Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="958e5-105">Changes from Internet Explorer 6 to Internet Explorer 7</span></span></th>
<th><span data-ttu-id="958e5-106">Modifiche da Internet Explorer 7 a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="958e5-106">Changes from Internet Explorer 7 to Internet Explorer 8</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="958e5-107"><a href="versioning.md">Versioning</a></span><span class="sxs-lookup"><span data-stu-id="958e5-107"><a href="versioning.md">Versioning</a></span></span></td>
<td><ul>
<li><span data-ttu-id="958e5-108">Vettori di versione</span><span class="sxs-lookup"><span data-stu-id="958e5-108">Version Vectors</span></span></li>
<li><span data-ttu-id="958e5-109">Stringa agente utente</span><span class="sxs-lookup"><span data-stu-id="958e5-109">User Agent String</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="958e5-110">Vettori di versione</span><span class="sxs-lookup"><span data-stu-id="958e5-110">Version Vectors</span></span></li>
<li><span data-ttu-id="958e5-111">Stringa agente utente</span><span class="sxs-lookup"><span data-stu-id="958e5-111">User Agent String</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="958e5-112"><a href="standards.md">Standard</a></span><span class="sxs-lookup"><span data-stu-id="958e5-112"><a href="standards.md">Standards</a></span></span></td>
<td><ul>
<li><span data-ttu-id="958e5-113">Miglioramenti HTML 4.01</span><span class="sxs-lookup"><span data-stu-id="958e5-113">HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="958e5-114">Miglioramenti CSS 2.1</span><span class="sxs-lookup"><span data-stu-id="958e5-114">CSS 2.1 improvements</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="958e5-115">Miglioramenti aggiuntivi HTML 4.01</span><span class="sxs-lookup"><span data-stu-id="958e5-115">Additional HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="958e5-116">Conformità completa CSS 2.1</span><span class="sxs-lookup"><span data-stu-id="958e5-116">Full CSS 2.1 compliance</span></span></li>
<li><span data-ttu-id="958e5-117">Supporto HTML 5.0</span><span class="sxs-lookup"><span data-stu-id="958e5-117">Some HTML 5.0 support</span></span></li>
<li><span data-ttu-id="958e5-118">Supporto della terza versione di ECMAScript e supporto della quinta versione di ECMAScript (incluso JSON nativo)</span><span class="sxs-lookup"><span data-stu-id="958e5-118">ECMAScript 3rd edition support and some ECMAScript 5th edition support (including native JSON)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="958e5-119"><a href="security.md">Sicurezza</a></span><span class="sxs-lookup"><span data-stu-id="958e5-119"><a href="security.md">Security</a></span></span></td>
<td><ul>
<li><span data-ttu-id="958e5-120">Miglioramenti HTTPS</span><span class="sxs-lookup"><span data-stu-id="958e5-120">HTTPS improvements</span></span></li>
<li><span data-ttu-id="958e5-121">Script più sicuro</span><span class="sxs-lookup"><span data-stu-id="958e5-121">More secure scripting</span></span></li>
<li><span data-ttu-id="958e5-122">Modalità protetta (Windows Vista e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="958e5-122">Protected Mode (Windows Vista and later versions)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="958e5-123">Migliore protezione da malware</span><span class="sxs-lookup"><span data-stu-id="958e5-123">Better protection from malware</span></span></li>
<li><span data-ttu-id="958e5-124">Filtro DEP/NX & XSS abilitato per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="958e5-124">DEP/NX & XSS filter on by default</span></span></li>
<li><span data-ttu-id="958e5-125">Modalità mista HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="958e5-125">HTTP/HTTPS mixed mode</span></span></li>
<li><span data-ttu-id="958e5-126">AJAX più sicuro</span><span class="sxs-lookup"><span data-stu-id="958e5-126">AJAX more secure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="958e5-127"><a href="architecture.md">Architettura</a></span><span class="sxs-lookup"><span data-stu-id="958e5-127"><a href="architecture.md">Architecture</a></span></span></td>

<td><ul>
<li><span data-ttu-id="958e5-128">Coppie di Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="958e5-128">Loosely coupled Internet Explorer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="958e5-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="958e5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="958e5-130">Gestione della compatibilità delle applicazioni durante la migrazione a Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="958e5-130">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



