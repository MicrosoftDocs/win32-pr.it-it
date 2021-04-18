---
description: Un numero di factoids descrive l'input comune a tutti i riconoscitori del linguaggio e non deve avere formati diversi per le diverse lingue. La tabella seguente elenca factoids comuni in tutti i linguaggi.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids comuni tra lingue diverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307492"
---
# <a name="factoids-common-across-languages"></a>Factoids comuni tra lingue diverse

Un numero di factoids descrive l'input comune a tutti i riconoscitori del linguaggio e non deve avere formati diversi per le diverse lingue. La tabella seguente elenca factoids comuni in tutti i linguaggi.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Factoid</th>
<th>Definizione</th>
<th>Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Cifre</strong></td>
<td>Imposta la distorsione per una singola cifra. Il riconoscimento è distorto per restituire solo le cifre singole quando questo controllo è impostato.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>Posta elettronica</strong></td>
<td>Imposta la distorsione per un indirizzo di posta elettronica.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Imposta la distorsione per diversi formati di URL.<br/>
<blockquote>
[!Note]<br />
Le impostazioni predefinite per il riconoscimento includono il controllo <strong>Web</strong> . Per questo motivo, è possibile che non si noti una grande differenza tra il controllo dell'oggetto <strong>Web</strong> e l'impostazione predefinita. Tuttavia, il controllo <strong>Web</strong> consente di eliminare gli spazi tra le parole in un URL.
</blockquote>
<br/></td>
<td>http: \\ Microsoft.NET<br/> https://microsoft.us/<br/> https: \\ www.Microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world. com<br/> www.microsoft.us \<br/> http: \\www.microsoft.com\myfile.htm<br/> http: \\www.microsoft.com\myfile.html<br/> http: \\ www. Microsoft. com\myfile.asp<br/> http: \\ www.Microsoft.uk<br/> http: \\ www.Microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>Default</strong></td>
<td>Restituisce le impostazioni predefinite del riconoscimento.<br/></td>
<td>L'impostazione predefinita per factoids per le lingue occidentali include il dizionario di sistema, il dizionario utenti, le varie punteggiatura e il factoids <strong>Web</strong> e il <strong>numero</strong> .<br/> L'impostazione predefinita per factoids per le lingue asiatiche orientali include tutti i caratteri supportati dal riconoscimento.<br/></td>
</tr>
<tr class="odd">
<td><strong>Nessuno</strong></td>
<td>Disabilita tutti factoids, dizionari e il modello di linguaggio.<br/></td>
<td>Questo controllo del controllo deve essere usato solo quando non si vuole che il riconoscimento usi alcuna regola di grammatica o dizionari, incluso il dizionario di sistema. Questo controllo è utile per l'input di stringhe casuali, ad esempio codici prodotto. Non usare il flag di coercizione con questo controllo del controllo.<br/></td>
</tr>
</tbody>
</table>



 

 

 




