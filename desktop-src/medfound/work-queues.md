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
# <a name="work-queues"></a>Code di lavoro

In Microsoft Media Foundation, una coda di lavoro è un modo efficiente per eseguire operazioni asincrone su un altro thread.

In questa sezione vengono trattati gli argomenti seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="using-work-queues.md">Uso delle code di lavoro</a></td>
<td>Viene descritto come un'applicazione o un componente può utilizzare le code di lavoro per eseguire operazioni asincrone.</td>
</tr>
<tr class="even">
<td><a href="writing-an-asynchronous-method.md">Scrittura di un metodo asincrono</a></td>
<td>Viene descritto come scrivere un metodo asincrono che segue il modello Begin/End descritto in <a href="asynchronous-callback-methods.md">metodi di callback asincroni</a>.</td>
</tr>
<tr class="odd">
<td><a href="custom-asynchronous-result-objects.md">Oggetti risultato asincrono personalizzati</a></td>
<td>Viene descritto come creare un'implementazione personalizzata dell'interfaccia <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a> .<br/>
<blockquote>
[!Note]<br />
La maggior parte delle applicazioni deve usare l'implementazione di stock fornita da <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult"><strong>MFCreateAsyncResult</strong></a>. Questo argomento è relativo alle applicazioni con requisiti avanzati.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="media-foundation-work-queue-and-threading-improvements.md">Miglioramenti della coda di lavoro e del threading</a></td>
<td>Vengono descritti i miglioramenti apportati a Windows 8 per le code di lavoro e il threading nella piattaforma Media Foundation.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 




