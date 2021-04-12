---
description: Questo argomento definisce le impostazioni locali \_ INEG \* costanti usate da NLS.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: Costanti LOCALE_INEG *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b17c61f0ca769206f30b84aa73cc3548ad9b915
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343991"
---
# <a name="locale_ineg-constants"></a>Costanti INEG delle impostazioni locali \_ \*

Questo argomento definisce le impostazioni locali \_ INEG \* costanti usate da NLS.



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
<td>LOCALE_INEGCURR</td>
<td>Modalità valuta negativa. 
<table>
<thead>
<tr class="header">
<th>Modalità</th>
<th>Formato per la valuta negativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parentesi sinistra, simbolo di valuta, numero, parentesi chiusa; ad esempio, ($1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Segno negativo, simbolo di valuta, numero; ad esempio,-$1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Simbolo di valuta, segno negativo, numero; ad esempio, $-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Simbolo di valuta, numero, segno negativo; ad esempio, $1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Parentesi sinistra, numero, simbolo di valuta, parentesi chiusa; ad esempio, ($1,1)</td>
</tr>
<tr class="even">
<td>5</td>
<td>Segno negativo, numero, simbolo di valuta; ad esempio,-$1,1</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Numero, segno negativo, simbolo di valuta; ad esempio, 1,1-$</td>
</tr>
<tr class="even">
<td>7</td>
<td>Numero, simbolo di valuta, segno negativo; ad esempio, $1,1-</td>
</tr>
<tr class="odd">
<td>8</td>
<td>Segno negativo, numero, spazio, simbolo di valuta, ad esempio #5, ma con uno spazio prima del simbolo di valuta. ad esempio,-$1,1</td>
</tr>
<tr class="even">
<td>9</td>
<td>Segno negativo, simbolo di valuta, spazio, numero (ad esempio #1, ma con uno spazio dopo il simbolo di valuta); ad esempio,-$1,1</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Numero, spazio, simbolo monetario, segno negativo (ad esempio #7, ma con uno spazio prima del simbolo di valuta); ad esempio, $1,1-</td>
</tr>
<tr class="even">
<td>11</td>
<td>Simbolo di valuta, spazio, numero, segno negativo (ad esempio #3, ma con uno spazio dopo il simbolo di valuta); ad esempio, $1,1-</td>
</tr>
<tr class="odd">
<td>12</td>
<td>Simbolo di valuta, spazio, segno negativo, numero (ad esempio #2, ma con uno spazio dopo il simbolo di valuta); ad esempio, $-1,1</td>
</tr>
<tr class="even">
<td>13</td>
<td>Numero, segno negativo, spazio, simbolo di valuta, ad esempio #6, ma con uno spazio prima del simbolo di valuta. ad esempio, 1,1-$</td>
</tr>
<tr class="odd">
<td>14</td>
<td>Parentesi sinistra, simbolo di valuta, spazio, numero, parentesi chiusa (ad esempio #0, ma con uno spazio dopo il simbolo di valuta); ad esempio, ($1,1)</td>
</tr>
<tr class="even">
<td>15</td>
<td>Parentesi aperta, numero, spazio, simbolo di valuta, parentesi destra (ad esempio #4, ma con uno spazio prima del simbolo di valuta); ad esempio, ($1,1)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>LOCALE_INEGNUMBER</td>
<td>Modalità numerica negativa, ovvero il formato per un numero negativo. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Formato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Parentesi sinistra, numero, parentesi chiusa; ad esempio, (1,1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Segno negativo, numero; ad esempio,-1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Segno negativo, spazio, numero; ad esempio,-1,1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Numero, segno negativo; ad esempio, 1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Numero, spazio, segno negativo; ad esempio, 1,1-</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSEPBYSPACE</td>
<td>Separazione del segno negativo in un valore monetario. Questo valore è 1 se il simbolo di valuta è separato da uno spazio rispetto all'importo negativo oppure 0 in caso contrario.</td>
</tr>
<tr class="even">
<td>LOCALE_INEGSIGNPOSN</td>
<td>Indice di formattazione per il segno negativo nei valori di valuta. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Le parentesi racchiudono la quantità e il simbolo di valuta.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Il segno precede il numero.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Il segno segue il numero.</td>
</tr>
<tr class="even">
<td>3</td>
<td>Il segno precede il simbolo di valuta.</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Il segno segue il simbolo di valuta.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSYMPRECEDES</td>
<td>Posizione del simbolo di valuta in un valore monetario negativo. Questo valore è 1 se il simbolo di valuta precede l'importo negativo oppure 0 se il simbolo segue la quantità.</td>
</tr>
</tbody>
</table>



 

 

 



