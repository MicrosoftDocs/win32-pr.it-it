---
description: Prima di iniziare a sviluppare un'applicazione di servizi HTTP di Microsoft Windows (WinHTTP), è necessario innanzitutto decidere se utilizzare l'API C/C++ o l'interfaccia COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Scelta di un'interfaccia WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313233"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="6a115-103">Scelta di un'interfaccia WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6a115-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="6a115-104">Prima di iniziare a sviluppare un'applicazione di servizi HTTP di Microsoft Windows (WinHTTP), è necessario innanzitutto decidere se utilizzare l'API C/C++ o l'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="6a115-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="6a115-105">Nella tabella seguente vengono riepilogati i vantaggi e gli svantaggi associati a ognuno di questi approcci.</span><span class="sxs-lookup"><span data-stu-id="6a115-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6a115-106">API C/C++</span><span class="sxs-lookup"><span data-stu-id="6a115-106">C/C++ API</span></span></th>
<th><span data-ttu-id="6a115-107">Interfaccia COM</span><span class="sxs-lookup"><span data-stu-id="6a115-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a115-108">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="6a115-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="6a115-109">Le risposte possono essere elaborate in blocchi, che risultano più efficienti.</span><span class="sxs-lookup"><span data-stu-id="6a115-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="6a115-110">Le operazioni POST possono anche essere elaborate in blocchi, velocizzando il tempo di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6a115-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="6a115-111">Supporto del proxy AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="6a115-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="6a115-112">Accesso al set completo di funzionalità di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6a115-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="6a115-113">I dati binari possono essere facilmente gestiti.</span><span class="sxs-lookup"><span data-stu-id="6a115-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6a115-114">La creazione di un'applicazione è semplice e richiede un minor numero di righe di codice rispetto all'API C/C++.</span><span class="sxs-lookup"><span data-stu-id="6a115-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="6a115-115">L'interfaccia può essere utilizzata dai linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="6a115-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a115-116">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="6a115-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="6a115-117">L'elaborazione è più complessa.</span><span class="sxs-lookup"><span data-stu-id="6a115-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="6a115-118">L'API C/C++ richiede più passaggi rispetto all'interfaccia COM per eseguire le stesse azioni.</span><span class="sxs-lookup"><span data-stu-id="6a115-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="6a115-119">La configurazione di una richiesta richiede più codice.</span><span class="sxs-lookup"><span data-stu-id="6a115-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6a115-120">L'interfaccia COM non fornisce l'accesso al set completo di funzionalità di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="6a115-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="6a115-121">È difficile gestire i tipi di dati binari in alcuni linguaggi di scripting, ad esempio VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="6a115-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="6a115-122">L'interfaccia COM non supporta il proxy AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="6a115-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="6a115-123">Le applicazioni devono utilizzare il modello di APARTMENT_THREADED COM.</span><span class="sxs-lookup"><span data-stu-id="6a115-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="6a115-124">Prima che una risposta possa iniziare a essere elaborata, l'intera risposta deve prima essere ricevuta e memorizzata nel buffer.</span><span class="sxs-lookup"><span data-stu-id="6a115-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



