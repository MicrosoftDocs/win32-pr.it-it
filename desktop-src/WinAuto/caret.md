---
title: Accento circonflesso (riferimento all'elemento MSAA UI)
description: Il punto di inserimento è una linea lampeggiante, un blocco o una bitmap nell'area client di una finestra o in un controllo che accetta input da tastiera.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857945"
---
# <a name="caret-msaa-ui-element-reference"></a>Accento circonflesso (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli elementi di interesse per i riferimenti agli elementi dell'interfaccia utente MSAA. L'uso di un punto di inserimento in diversi framework dell'interfaccia utente non è descritto qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

Il punto di inserimento è una linea lampeggiante, un blocco o una bitmap nell'area client di una finestra o in un controllo che accetta input da tastiera. Indica la posizione in cui vengono inseriti testo o grafica. Poiché solo una finestra alla volta ha lo stato attivo della tastiera, c'è un solo punto di inserimento nel sistema.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Il punto di inserimento supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Il punto di inserimento supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Commenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>La proprietà <strong>childCount</strong> è zero.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></td>
<td>La proprietà <strong>Name</strong> è &quot; Edit &quot; .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></td>
<td>La proprietà <strong>Role</strong> è <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></td>
<td>I valori possibili per la proprietà <strong>state</strong> includono:
<ul>
<li>Zero, che indica che il punto di inserimento è visibile</li>
<li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Note

-   A differenza di altri elementi dell'interfaccia utente, all'oggetto cursore non è associato un handle di finestra. Per ottenere l'accesso all'oggetto del cursore, i client devono impostare un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e attendere che l'oggetto del cursore generi gli eventi.
-   L'oggetto del punto di inserimento nel controllo Rich Edit fornito da Riched20.dll (usato negli editor di testo, ad esempio Microsoft WordPad in Windows 98), non invia alcun [winEvents](winevents-infrastructure.md) quando la relativa posizione viene modificata durante la selezione del testo. Quando gli utenti preme MAIUSC e tasti di direzione per selezionare il testo, l'oggetto del cursore non attiva l' [**\_ oggetto evento \_ posizioneCambia**](event-constants.md) WinEvent. Analogamente, quando la selezione viene impostata a livello di programmazione tramite messaggi Rich Edit, l'oggetto cursore non invia alcun evento per indicare la nuova posizione.

    Tutte le applicazioni che utilizzano Riched20.dll presentano questo problema. Le applicazioni che usano versioni precedenti del controllo Rich Edit inviano correttamente gli eventi in base alla selezione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




