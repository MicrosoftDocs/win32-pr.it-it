---
description: Descrive i formati di data supportati per l'utilizzo nella clausola WHERE di WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: Formati di data WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882297"
---
# <a name="wql-supported-date-formats"></a>Formati di data WQL-Supported

Oltre al formato **DateTime** WMI, i formati di data seguenti sono supportati per l'utilizzo nella clausola **where** di WQL.

Il formato di ora visualizzato è diverso per le diverse impostazioni locali. Gli script che si connettono ai computer remoti devono specificare l'ora nel formato appropriato per le impostazioni locali del computer di destinazione.

Ad esempio, il formato di data e ora Stati Uniti è MM-gg-aaaa. Se uno script in un computer usa si connette a un computer di destinazione in impostazioni locali in cui il formato è GG-MM-AAAA, le query vengono elaborate nel computer di destinazione come GG-MM-AAAA. Per evitare risultati diversi tra le impostazioni locali, utilizzare il formato [**DateTime**](datetime.md) . Per altre informazioni, vedere [formato di data e ora](date-and-time-format.md).



<table>
<thead>
<tr class="header">
<th>Formato</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lun [TH] dd [,] [AA] AA</td>
<td>Mese (digitato o abbreviato in tre lettere), giorno, virgola facoltativa e anno a due o quattro cifre.<br/> <dl> 21 gennaio 1932<br />
21 gennaio 32<br />
Gennaio 21 1932<br />
Gennaio 21 32<br />
</dl></td>
</tr>
<tr class="even">
<td>Lun [TH] [,] aaaa</td>
<td>Mese (ortografico o abbreviato in tre lettere), virgola facoltativa e anno a quattro cifre.<br/> <dl> 1932 gennaio<br />
Gennaio 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>Lun [TH] [AA] aa gg</td>
<td>Mese (ortografico o abbreviato in tre lettere), anno a due o quattro cifre e giorno.<br/> <dl> 1932 21 gennaio<br />
Gennaio 32 21<br />
</dl></td>
</tr>
<tr class="even">
<td>DD Mon [TH] [,] [] [AA] AA</td>
<td>Giorno del mese, mese (ortografico o abbreviato in tre lettere), virgola facoltativa, spazio facoltativo e anno a due o quattro cifre.<br/> <dl> 21 gennaio, 1932<br />
21 Jan32<br />
</dl></td>
</tr>
<tr class="odd">
<td>DD [YY] YY lun [TH]</td>
<td>Giorno del mese, anno a due o quattro cifre e mese (digitato o abbreviato in tre lettere).<br/> <dl> 21 1932 gennaio<br />
</dl></td>
</tr>
<tr class="even">
<td>[YY] AA lun [TH] dd</td>
<td>Anno a due o quattro cifre, ovvero con ortografia o abbreviazione in tre lettere, e giorno.<br/> <dl> 1932 gennaio 21<br />
</dl></td>
</tr>
<tr class="odd">
<td>aaaa lun [TH]</td>
<td>Anno e mese a due o quattro cifre (digitato o abbreviato in tre lettere).<br/> <dl> 1932 gen<br />
</dl></td>
</tr>
<tr class="even">
<td>aaaa gg Mon [TH]</td>
<td>Anno, giorno e mese a due o quattro cifre (digitato o abbreviato in tre lettere).<br/> <dl> 1932 21 gennaio<br />
</dl></td>
</tr>
<tr class="odd">
<td>M M {/-.} gg {/-.} [YY] AA</td>
<td>Anno, mese, giorno e due o quattro cifre. Si noti che i separatori devono essere uguali.<br/></td>
</tr>
<tr class="even">
<td>gg {/-.} M M {/-.} [YY] AA</td>
<td>Giorno del mese, mese e anno a due o quattro cifre. Si noti che i separatori devono essere uguali.<br/></td>
</tr>
<tr class="odd">
<td>M M {/-.} [YY] AA {/-.} GG</td>
<td>Mese, anno a due o quattro cifre e giorno. Si noti che i separatori devono essere uguali.<br/></td>
</tr>
<tr class="even">
<td>gg {/-.} [YY] AA {/-.} M M</td>
<td>Giorno del mese, anno a due o quattro cifre e mese. Si noti che i separatori devono essere uguali.<br/></td>
</tr>
<tr class="odd">
<td>[YY] AA {/-.} gg {/-.} M M</td>
<td>Anno, giorno e mese di due o quattro cifre. Si noti che i separatori devono essere uguali.<br/></td>
</tr>
<tr class="even">
<td>[YY] AA {/-.} M M {/-.} GG</td>
<td>Anno, mese e giorno a due o quattro cifre. Si noti che i separatori devono essere uguali.<br/></td>
</tr>
<tr class="odd">
<td>[AA] AAMMGG</td>
<td>Anno, mese e giorno con due o quattro cifre senza spazi.<br/></td>
</tr>
<tr class="even">
<td>aaaa [MM [gg]]</td>
<td>Anno a due o quattro cifre, mese facoltativo e giorno facoltativo, senza spazi.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Clausola WHERE](where-clause.md)
</dt> </dl>

 

 




