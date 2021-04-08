---
title: Barra di scorrimento semplice
description: Questa sezione contiene informazioni sugli elementi di programmazione usati per controllare le barre di scorrimento flat.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855714"
---
# <a name="flat-scroll-bar"></a>Barra di scorrimento semplice

Questa sezione contiene informazioni sugli elementi di programmazione usati per controllare le barre di scorrimento flat.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                    | Contenuto                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barre di scorrimento Flat](flat-scroll-bars.md) | In Microsoft Internet Explorer 4,0 è stata introdotta una nuova tecnologia visiva denominata barre di scorrimento semplici. Dal punto di vista funzionale, le barre di scorrimento Flat funzionano esattamente come le barre di scorrimento standard. La differenza consiste nel fatto che è possibile personalizzare l'aspetto in modo più ampio rispetto alle barre di scorrimento standard.<br/> |



 

### <a name="functions"></a>Funzioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></td>
<td>Abilita o Disabilita uno o entrambi i pulsanti di direzione della barra di scorrimento flat. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> standard. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></td>
<td>Ottiene le informazioni per una barra di scorrimento piatta. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> standard. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></td>
<td>Ottiene la posizione del cursore in una barra di scorrimento piatta. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> standard. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></td>
<td>Ottiene le proprietà per una barra di scorrimento semplice. Questa funzione può essere usata anche per determinare se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> è stato chiamato per questa finestra. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></td>
<td>Ottiene le proprietà per una barra di scorrimento semplice. Questa funzione può essere usata anche per determinare se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> è stato chiamato per questa finestra.
<blockquote>
[!Note]<br />
Questo è identico a <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></td>
<td>Ottiene l'intervallo di scorrimento per una barra di scorrimento semplice. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> standard. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></td>
<td>Imposta le informazioni per una barra di scorrimento piatta. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> standard. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></td>
<td>Imposta la posizione corrente del cursore in una barra di scorrimento piatta. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> standard. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></td>
<td>Imposta le proprietà per una barra di scorrimento semplice. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></td>
<td>Imposta l'intervallo di scorrimento di una barra di scorrimento piatta. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> standard. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></td>
<td>Mostra o nasconde una barra di scorrimento semplice. Se le barre di scorrimento semplice non sono inizializzate per la finestra, questa funzione chiama la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> standard. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></td>
<td>Inizializza le barre di scorrimento flat per una particolare finestra. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></td>
<td>Consente di inizializzare le barre di scorrimento flat per una particolare finestra. La finestra specificata verrà ripristinata sulle barre di scorrimento standard. <br/></td>
</tr>
</tbody>
</table>



 

 

 





