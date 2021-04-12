---
description: Costanti di \_ restituzione delle impostazioni locali \*
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Costanti LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233308"
---
# <a name="locale_return-constants"></a>Costanti di \_ restituzione delle impostazioni locali \*

Questo argomento definisce le \_ costanti di restituzione delle impostazioni locali \* usate da NLS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 e versioni successive:</strong> Recuperare i nomi di genitive dei mesi, ovvero i nomi usati quando i nomi dei mesi vengono combinati con altri elementi. Ad esempio, in ucraino l'equivalente di gennaio viene scritto &quot; Січень &quot; quando il mese è denominato da solo. Tuttavia, quando il nome del mese viene usato in combinazione, ad esempio, in una data, ad esempio il 5 gennaio 2003, viene usata la forma genitiva del nome. Per l'esempio ucraino, il nome del mese del genico viene visualizzato come &quot; 5 січня 2003 &quot; . L'elenco dei nomi dei mesi di genitive inizia con gennaio e è delimitato da punti e virgola. Se non è presente alcun tredicesimo mese, utilizzare un punto e virgola al suo posto alla fine dell'elenco.
<blockquote>
[!Note]<br />
I nomi dei mesi di genitive non esistono in tutte le lingue.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows Me/98, Windows NT 4,0 e versioni successive:</strong> Recuperare un numero. Questa costante fa in modo che <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperi un valore come numero anziché come stringa. Il buffer che riceve il valore deve essere almeno la lunghezza di un valore DWORD. Questa costante può essere combinata con qualsiasi altra costante con un nome che inizia con &quot; LOCALE_I &quot; .</td>
</tr>
</tbody>
</table>



 

 

 




