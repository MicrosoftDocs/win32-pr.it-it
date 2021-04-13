---
title: Barra del titolo (riferimento all'elemento MSAA UI)
description: La barra del titolo nella parte superiore di una finestra Visualizza un'icona definita dall'applicazione e una riga di testo.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398492"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barra del titolo (riferimento all'elemento MSAA UI)

> [!Note]  
> Questo argomento descrive gli oggetti della **barra del titolo** a scopo di riferimento all'elemento dell'interfaccia utente MSAA. La creazione di oggetti della **barra del titolo** in diversi framework dell'interfaccia utente non è descritta qui. Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.

 

La barra del titolo nella parte superiore di una finestra Visualizza un'icona definita dall'applicazione e una riga di testo. Il testo specifica il nome dell'applicazione e indica lo scopo della finestra. La barra del titolo consente inoltre all'utente di spostare la finestra utilizzando un mouse o un altro dispositivo di puntamento.

Le barre del titolo contengono almeno tre piccoli pulsanti che consentono di ridurre al minimo, ingrandire o ripristinare e chiudere la finestra associata alla barra del titolo. Le barre del titolo contengono anche un pulsante della Guida sensibile al contesto. Le applicazioni in esecuzione nella versione Far-East del sistema operativo Windows possono contenere anche pulsanti input Method Editor (IME). Microsoft Active Accessibility espone questi pulsanti come elementi figlio della barra del titolo.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Le barre del titolo supportano i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Le barre del titolo supportano le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



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
<td>La proprietà <strong>childCount</strong> è cinque. La proprietà <strong>childCount</strong> include i pulsanti IME e Guida sensibile al contesto anche quando non sono visualizzati. I pulsanti che non sono visualizzati hanno la proprietà <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>La proprietà <strong>Description</strong> della barra del titolo è: &quot; Visualizza il nome della finestra e contiene i controlli per modificarla. &quot; I pulsanti figlio nella barra del titolo presentano le descrizioni seguenti:<br/>
<ul>
<li>&quot;Sposta la finestra da</li>
<li>&quot;Rende la finestra completa</li>
<li>&quot;Inserisce un oggetto ridotto a icona o</li>
<li>&quot;Chiude la finestra&quot;</li>
<li>&quot;Entra o lascia il contesto-</li>
<li>&quot;Visualizza la tastiera quando viene premuto&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>La barra del titolo non supporta la proprietà <strong>Name</strong> . I pulsanti figlio nella barra del titolo hanno i nomi seguenti:
<ul>
<li>&quot;Riduci&quot;</li>
<li>&quot;Ingrandisci &quot; o &quot; Ripristina &quot; ,</li>
<li>&quot;Close&quot;</li>
<li>&quot;Guida del contesto&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>La proprietà <strong>Parent</strong> della barra del titolo è la finestra principale dell'applicazione ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) con lo stesso nome della classe di finestra definito dall'applicazione della barra del titolo.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>La proprietà <strong>Role</strong> è <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. I pulsanti figlio nella barra del titolo hanno la <strong></strong> proprietà Role <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>La proprietà <strong>state</strong> per la barra del titolo e i pulsanti figlio possono essere una combinazione di uno o più dei <a href="object-state-constants.md">valori</a>seguenti: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>La proprietà <strong>value</strong> è una stringa uguale al testo visualizzato nella barra del titolo.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Note

-   Anche se la **barra del titolo** di un'applicazione ha lo stato del sistema di stato del flag di stato, lo **stato del flag di stato è** non [**\_ \_ attivo**](object-state-constants.md) [**\_ \_ .**](object-state-constants.md) L'impostazione dello stato attivo su un oggetto della barra del titolo attiva la finestra dell'applicazione.
-   Poiché l'oggetto barra del titolo non supporta [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), i pulsanti sulla barra del titolo sono elementi semplici. Non supportano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . L'oggetto barra del titolo fornisce informazioni su questi pulsanti figlio.
-   Poiché le barre del titolo non ottengono lo stato attivo e non hanno un'azione predefinita, i metodi [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) e [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) non sono supportati per questo controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible (interfaccia)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





