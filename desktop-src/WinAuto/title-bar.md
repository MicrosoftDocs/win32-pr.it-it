---
title: Barra del titolo (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: La barra del titolo nella parte superiore di una finestra visualizza un'icona definita dall'applicazione e una riga di testo.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9183e4c4f5364fb45ba2a73dd2d40509c03c7838bbb248e1d95765b675f50cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994001"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barra del titolo (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

> [!Note]  
> Questo argomento descrive gli oggetti **barra del titolo** ai fini del riferimento agli elementi dell'interfaccia utente MSAA. La procedura per creare **oggetti barra del** titolo in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il framework dell'interfaccia utente in uso.

 

La barra del titolo nella parte superiore di una finestra visualizza un'icona definita dall'applicazione e una riga di testo. Il testo specifica il nome dell'applicazione e indica lo scopo della finestra. La barra del titolo consente anche all'utente di spostare la finestra usando un mouse o un altro dispositivo di puntamento.

Le barre del titolo contengono almeno tre piccoli pulsanti che riducono a icona, ingrandisce o ripristinano e chiudono la finestra associata alla barra del titolo. Le barre del titolo contengono anche un pulsante della Guida sensibile al contesto. Anche le applicazioni in Far-East versione precedente del sistema operativo Windows possono contenere pulsanti IME (Input Method Editor). Microsoft Active Accessibility questi pulsanti vengono esposti come elementi figlio della barra del titolo.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Le barre del titolo supportano i [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Le barre del titolo supportano le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



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
<td>La <strong>proprietà ChildCount</strong> è cinque. La <strong>proprietà ChildCount</strong> include i pulsanti IME e della Guida sensibile al contesto anche quando non vengono visualizzati. I pulsanti non visualizzati hanno la <strong>proprietà State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>La <strong>proprietà Description</strong> della barra del titolo stessa è: visualizza il nome della finestra e contiene i controlli per &quot; modificarla. &quot; I pulsanti figlio nella barra del titolo hanno le descrizioni seguenti:<br/>
<ul>
<li>&quot;Sposta la finestra all'uscita da</li>
<li>&quot;Rende la finestra piena</li>
<li>&quot;Inserisce un oggetto ridotto a icona o</li>
<li>&quot;Chiude la finestra&quot;</li>
<li>&quot;Immette o lascia il contesto.</li>
<li>&quot;Apre la tastiera quando viene premuta&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>La barra del titolo non supporta la <strong>proprietà</strong> Name. I pulsanti figlio nella barra del titolo hanno i nomi seguenti:
<ul>
<li>&quot;Riduci&quot;</li>
<li>&quot;Ingrandire &quot; o &quot; ripristinare &quot; ,</li>
<li>&quot;Close&quot;</li>
<li>&quot;Guida al contesto&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>La <strong>proprietà Parent</strong> della barra del titolo è la finestra principale dell'applicazione ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) con lo stesso nome della classe di finestra definita dall'applicazione della barra del titolo.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>La <strong>proprietà Role</strong> è <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. I pulsanti figlio nella barra del titolo hanno la <strong>proprietà Role</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>La <strong>proprietà State</strong> per la barra del titolo e i pulsanti figlio può essere una combinazione di uno o più dei valori <a href="object-state-constants.md">seguenti:</a> <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>La <strong>proprietà Value</strong> è una stringa uguale al testo visualizzato nella barra del titolo.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Note

-   Anche se la barra del titolo di un'applicazione ha il flag STATE [**\_ SYSTEM \_ FOCUSABLE**](object-state-constants.md)della proprietà **State** , non ha mai il flag **STATE** [**\_ SYSTEM \_ FOCUSED**](object-state-constants.md). L'impostazione dello stato attivo su un oggetto barra del titolo attiva la finestra dell'applicazione.
-   Poiché l'oggetto della barra del titolo non supporta [**il metodo \_ get accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), i pulsanti sulla barra del titolo sono elementi semplici. Non supportano [**l'interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) L'oggetto barra del titolo fornisce informazioni su questi pulsanti figlio.
-   Poiché le barre del titolo non ottengono lo stato attivo e non hanno alcuna azione predefinita, i metodi [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) e [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) non sono supportati per questo controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfaccia IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





