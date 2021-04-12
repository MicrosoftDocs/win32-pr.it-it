---
description: In Microsoft Media Foundation, una coda di lavoro è un modo efficiente per eseguire operazioni asincrone su un altro thread.
ms.assetid: f886d096-b1f5-42e4-8888-501b58bffd50
title: Code di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b1e5e8a0a3776f718f645550813bf008b38aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231768"
---
# <a name="work-queues"></a><span data-ttu-id="2bb9b-103">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="2bb9b-103">Work Queues</span></span>

<span data-ttu-id="2bb9b-104">In Microsoft Media Foundation, una coda di lavoro è un modo efficiente per eseguire operazioni asincrone su un altro thread.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-104">In Microsoft Media Foundation, a work queue is an efficient way to perform asynchronous operations on another thread.</span></span>

<span data-ttu-id="2bb9b-105">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-105">This section contains the following topics.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bb9b-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="2bb9b-106">Topic</span></span></th>
<th><span data-ttu-id="2bb9b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bb9b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bb9b-108"><a href="using-work-queues.md">Uso delle code di lavoro</a></span><span class="sxs-lookup"><span data-stu-id="2bb9b-108"><a href="using-work-queues.md">Using Work Queues</a></span></span></td>
<td><span data-ttu-id="2bb9b-109">Viene descritto come un'applicazione o un componente può utilizzare le code di lavoro per eseguire operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-109">Describes how an application or component can use work queues to perform asynchronous operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bb9b-110"><a href="writing-an-asynchronous-method.md">Scrittura di un metodo asincrono</a></span><span class="sxs-lookup"><span data-stu-id="2bb9b-110"><a href="writing-an-asynchronous-method.md">Writing an Asynchronous Method</a></span></span></td>
<td><span data-ttu-id="2bb9b-111">Viene descritto come scrivere un metodo asincrono che segue il modello Begin/End descritto in <a href="asynchronous-callback-methods.md">metodi di callback asincroni</a>.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-111">Describes how to write an asynchronous method that follows the Begin/End pattern described in <a href="asynchronous-callback-methods.md">Asynchronous Callback Methods</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bb9b-112"><a href="custom-asynchronous-result-objects.md">Oggetti risultato asincrono personalizzati</a></span><span class="sxs-lookup"><span data-stu-id="2bb9b-112"><a href="custom-asynchronous-result-objects.md">Custom Asynchronous Result Objects</a></span></span></td>
<td><span data-ttu-id="2bb9b-113">Viene descritto come creare un'implementazione personalizzata dell'interfaccia <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2bb9b-113">Describes how to create a custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2bb9b-114">La maggior parte delle applicazioni deve usare l'implementazione di stock fornita da <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-114">Most applications should use the stock implementation provided by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>.</span></span> <span data-ttu-id="2bb9b-115">Questo argomento è relativo alle applicazioni con requisiti avanzati.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-115">This topic is for applications with advanced requirements.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bb9b-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Miglioramenti della coda di lavoro e del threading</a></span><span class="sxs-lookup"><span data-stu-id="2bb9b-116"><a href="media-foundation-work-queue-and-threading-improvements.md">Work Queue and Threading Improvements</a></span></span></td>
<td><span data-ttu-id="2bb9b-117">Vengono descritti i miglioramenti apportati a Windows 8 per le code di lavoro e il threading nella piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2bb9b-117">Describes improvements in Windows 8 for work queues and threading in the Media Foundation platform.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2bb9b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bb9b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bb9b-119">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bb9b-119">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




