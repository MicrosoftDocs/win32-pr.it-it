---
description: impostazioni locali \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128118"
---
# <a name="locale_idigitsubstitution"></a>impostazioni locali \_ IDIGITSUBSTITUTION

**Windows 2000:** Forma delle cifre. Ad esempio, le cifre arabe, tailandesi e indiane hanno forme classiche diverse dalle cifre europee. Per le impostazioni locali con [ \_ SNATIVEDIGITS delle impostazioni locali](locale-snative-constants.md) specificate come valori diversi da ASCII 0-9, questo valore specifica se è necessario assegnare la preferenza a tali cifre a scopo di visualizzazione. Se, ad esempio, si sceglie un valore pari a 2, vengono sempre utilizzate le cifre specificate dalle impostazioni locali \_ SNATIVEDIGITS. Se si sceglie 1, vengono sempre utilizzate le cifre ASCII 0-9. Se si sceglie 0, viene usato ASCII in alcune circostanze e le cifre specificate dalle impostazioni locali \_ SNATIVEDIGITS vengono usate in altre, a seconda del contesto.



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
<td>0</td>
<td>Sostituzione basata sul contesto. Le cifre vengono visualizzate in base al testo precedente nello stesso output. Le cifre europee seguono gli alfabeti latini, Arabic-Indic cifre seguono il testo arabo e altre cifre nazionali seguono il testo scritto in diversi altri script. Quando non è presente un testo precedente, le impostazioni locali e l'ordine di lettura visualizzato determinano la sostituzione dei numeri, come illustrato nella tabella seguente.
<table>
<thead>
<tr class="header">
<th>Locale</th>
<th>Ordine di lettura</th>
<th>Cifre utilizzate</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arabo</td>
<td>Da destra a sinistra</td>
<td>Arabic-Indic</td>
</tr>
<tr class="even">
<td>Thai</td>
<td>Da sinistra a destra</td>
<td>Cifre tailandesi</td>
</tr>
<tr class="odd">
<td>Tutti gli altri</td>
<td>Qualsiasi</td>
<td>Nessuna sostituzione utilizzata</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>Nessuna sostituzione utilizzata. Compatibilità completa con Unicode.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Sostituzione delle cifre native. Le forme nazionali vengono visualizzate in base LOCALE_SNATIVEDIGITS.</td>
</tr>
</tbody>
</table>



 

 

 



